# Azure ML 2.0 Developer Experience
This is the private preview for the Azure ML 2.0 developer experience.
The 2.0 developer platform provides first class API / CLI / SDK support for model training and scoring scenarios.

# User Guide (WIP)
https://azure.github.io/azureml-v2-preview/docs/userguide/

# Key goals
[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fmldevplatv2.blob.core.windows.net%2Fcli%2Fazuredeploy.json)
## New CLI experience
- consistent job story
- consistent endpoint story
- all ML resources, assets and artifacts can be serialized and exported in a human readable format
- all jobs are now composable
- reduce concepts to fundamentals of: Job, Data, Environment, Model, Endpoint, LinkedService (Compute & Storage)

## ARM support
- Improved API surface area and clean APIs for ISVs and language SDKs to build on top of
- ARM for key use cases (job / endpoint creation), including batch scoring endpoints
- Consistent asset management experience (all assets can be registered via ARM now, enforces consistent behavior, etc.)
- Per-resource / per-asset / per-action RBAC and policy support
- X-workspace discovery, consumption and sharing (CI/CD) of assets and resources, proper git-flow support

## Current Timeline

November 2020 (committed): 
  - Cloud execution of job (command job and sweep job)
  - Support for Data / Code / Environment / Model assets in jobs

March 2021 (pending):
- Private preview of full feature set of end2end training flow captured in [private preview 2](specs/job.md)
 -- including the above plus:
  - local docker training (w/ local + data)
  - spark job support
  - Workflow - full support & alignment with jobs
  - Real time and batch Endpoint

