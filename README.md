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
./build.ps1 Serve -Target local
```

The full build runs Prepare, Build and Validate. Reports are written under `.processing/guidesite/`. Local builds do not deploy unless explicitly requested.

## Update OpenGuidePlatform

On a review branch:

```powershell
./build.ps1 Update -PlatformRelease v1
./build.ps1 -Target preview
git diff
```

This site tracks stable OpenGuidePlatform v1 releases through `platform.version: v1` in `.OpenGuidePlatform/settings.yaml`. Builds resolve the latest stable v1 release; review coordinated adapter updates before committing. The workflows and the final site-specific paragraph in `.agents/agents.md` are deliberate local customizations; preserve them when reconciling an update conflict. Do not edit the installation record to hide conflicts.

## Delivery

The workflow runs one Prepare → Build → Validate → Deploy → Verify chain. Prepare uses GitVersion to choose the site ring. Platform release selection is independent: local and hosted builds resolve the stable v1 selection in `.OpenGuidePlatform/settings.yaml`.

- Pull requests: temporary canary sites; the deployment adds the actual URL to the PR.
- Main: [preview site](https://purple-tree-00e22e403-preview.westeurope.5.azurestaticapps.net/).
- Production: [safedelusion.com](https://safedelusion.com/), triggered by pushing a stable version tag such as `v1.2.3` or `1.2.3`. Tag a commit containing this workflow. Prepare uses GitVersion to select the ring; prerelease tags retain their corresponding preview or canary ring.

Site-owned destinations are in the `delivery` section of `.OpenGuidePlatform/settings.yaml`. Closing a PR removes its temporary deployment.

## Editing

Read `.agents/site-instructions.md` for the protected guide and wrapper editorial rules. Root `AGENTS.md` and `CLAUDE.md` are symbolic links to `.agents/agents.md`.

The published guide and supplied PDF remain protected. Its `/safe-decision-makers/latest` alias belongs to the published edition, at the end of its front matter.
