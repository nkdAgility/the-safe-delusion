# The SAFe Delusion

Information for decision-makers considering the SAFe framework.

## Build and run locally

Use PowerShell 7.4+, Hugo Extended and Go. On Windows, enable Developer Mode (or clone with permission to create symbolic links), and configure Git before cloning:

```powershell
git config --global core.symlinks true
```

Install build prerequisites, validate the site, and start the local server:

```powershell
./build.ps1 Dependencies
./build.ps1 -Target preview
./build.ps1 Serve -Target local -BaseUrl http://localhost:1313/
```

The full build runs Prepare, Build and Validate. Reports are written under `.processing/guidesite/`. Local builds do not deploy unless explicitly requested.

## Update OpenGuidePlatform

On a review branch:

```powershell
./build.ps1 Update -PlatformRelease v2.2.0-Preview.1 -Ring preview
./build.ps1 -Target preview
git diff
```

This site selects OpenGuidePlatform `v2.2.0-Preview.1` with platform ring `preview` in `.OpenGuidePlatform/settings.yaml`. Review coordinated updates on a task branch before committing. The workflows and `.agents/site-instructions.md` remain site-owned. Preserve their delivery and editorial rules; do not edit the generated installation record to hide conflicts. The generated-text LF attributes preserve recorded managed-file bytes on Windows.

## Delivery

The workflow runs one Prepare → Build → Validate → Deploy → Verify chain. Prepare uses GitVersion to choose the site ring. Platform release selection is independent: local and hosted builds resolve the explicit preview-package selection in `.OpenGuidePlatform/settings.yaml`.

- Pull requests: temporary canary sites; the deployment adds the actual URL to the PR.
- Main: [preview site](https://purple-tree-00e22e403-preview.westeurope.5.azurestaticapps.net/).
- Production: [safedelusion.com](https://safedelusion.com/), triggered by pushing a stable version tag such as `v1.2.3` or `1.2.3`. Tag a commit containing this workflow. Prepare uses GitVersion to select the ring; prerelease tags retain their corresponding preview or canary ring.

Site-owned destinations are in the `delivery` section of `.OpenGuidePlatform/settings.yaml`. Closing a PR removes its temporary deployment.

## Editing

Read `.agents/site-instructions.md` for the protected guide and wrapper editorial rules. Root `AGENTS.md` and `CLAUDE.md` are symbolic links to `.agents/agents.md`.

The published guide and supplied PDF remain protected. Its `/safe-decision-makers/latest` alias belongs to the published edition, at the end of its front matter.

## Guide-local attribution

Guide credits are in `site/content/safe-decision-makers/data/contributors.yml`. The file moved without changing its records, roles or edition associations. Translation teams, when declared, use `data/translators.<language>.yml` in the same guide root. These records remain inside the protected guide area; changes require maintainer-authorised scope.

The adoption baseline captures the resolved credit selection and supplied PDF SHA-256. Validate both targets with `./build.ps1 -Target preview` and `./build.ps1 -Target production`; evidence is under `.processing/attribution-preview` and `.processing/attribution-production`. This package adoption does not approve production promotion or configure independent agent controls.

Use the matching [shared setup guide](https://github.com/nkdAgility/OpenGuidePlatform/blob/v2.2.0-Preview.1/system/OpenGuidePlatform.Agents.Integration/contributor-guide/setup.md) for supported contributor setup.
