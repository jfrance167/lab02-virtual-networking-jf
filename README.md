# Cloud Computing Architecture Lab 2 Virtual Networking

This repository preserves work from my **Cloud Computing Architecture** course, CISY 5183. The lab introduced Azure virtual networking concepts and the process of organizing cloud deployment artifacts in Git.

## Lab focus

- Azure resource groups and regional deployment planning.
- Virtual networks, address spaces, and subnets.
- ARM template and parameter-file export workflows.
- Reusing earlier storage-lab artifacts while progressing into networking.
- Source-control practice using branches and incremental commits.

## Repository status

This is an incomplete course archive. The default-branch `lab2-template.json` contains an export placeholder and `lab2-parameters.json` is empty. The `arm/lab01` directory preserves a valid storage template from the earlier lab. A separate feature branch also contains exported challenge-lab artifacts.

I am keeping the repository public because it shows the progression of my coursework, including where an Azure export workflow did not produce a complete artifact.

## Course context

- Course: Cloud Computing Architecture
- Course identifier: CISY 5183
- Original region: East US 2

The files are learning artifacts and should not be treated as a deployable or production-secure architecture without review and repair.

## Local review and safe reuse

Clone this repository and inspect the Markdown and JSON files locally; no cloud
subscription or deployment is needed to review the coursework. These exports are
historical evidence. Empty parameter files and export placeholders, where noted
above, are not deployable templates and are deliberately preserved.

Use only an isolated subscription you own or are authorized to administer, with
a cost limit and teardown plan, for any future exercise. Review actual network
access, identities, credentials, names and API versions before deploying. Never
commit local credentials or production resource exports. See [SECURITY.md](SECURITY.md).

The retained storage export permits public-network access; private containers
still require authorization and this does not prove anonymous data access.
For a new deployment, evaluate the following storage-account properties together
with private endpoint/DNS configuration and Microsoft Entra role assignments:

```json
{
  "publicNetworkAccess": "Disabled",
  "allowSharedKeyAccess": false,
  "defaultToOAuthAuthentication": true,
  "allowBlobPublicAccess": false,
  "supportsHttpsTrafficOnly": true,
  "minimumTlsVersion": "TLS1_2"
}
```

This is a proposed hardening excerpt, not a complete deployment. Validate clients
and management access before applying it; disabling shared keys can break older
clients. The original course exports have not been rewritten or redeployed.

## Repository map

```text
lab02-virtual-networking-jf/
|-- .gitignore
|-- README.md
|-- SECURITY.md
|-- arm/
|-- lab02-virtual-networking-jf
|-- lab2-parameters.json
`-- lab2-template.json
```

Follow the setup and safety boundaries above before running or deploying any code.
