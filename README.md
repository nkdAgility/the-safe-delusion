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
./build.ps1 Update -ring preview
./build.ps1 -Target preview
git diff
```

This adoption uses the preview platform ring. Review updates before committing. The workflows and the final site-specific paragraph in `.agents/agents.md` are deliberate local customizations; preserve them when reconciling an update conflict. Do not edit the installation record to hide conflicts.

## Delivery

The workflow runs one Prepare → Build → Validate → Deploy → Verify chain. Prepare uses GitVersion to choose the site ring. Platform release selection is independent and uses the latest preview release.

- Pull requests: temporary canary sites; the deployment adds the actual URL to the PR.
- Main: [preview site](https://purple-tree-00e22e403-preview.westeurope.5.azurestaticapps.net/).
- Production: [safedelusion.com](https://safedelusion.com/), only when the version selects production.

Site-owned destinations are in `.OpenGuidePlatform/delivery.yaml`. Closing a PR removes its temporary deployment.

## Editing

Read `.agents/site-instructions.md` for the protected guide and wrapper editorial rules. Root `AGENTS.md` and `CLAUDE.md` are symbolic links to `.agents/agents.md`.

The published guide and supplied PDF remain protected. Its `/safe-decision-makers/latest` alias belongs to the published edition, at the end of its front matter.
