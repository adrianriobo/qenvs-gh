# qenvs-gh

Sample PoC on how to use qenvs on gh actions

## Windows Basic Workflow

This project contains [a sample workflow](./.github/workflows/windows.yaml) for gh actions using qenvs for spinning a windows machine, the flow can be copy pasted and new steps can be added in the middle accessing the target host created by the workflow to run a workload on it. 

The flow will require setup some secrets within the project:

* ARM_TENANT_ID
* ARM_SUBSCRIPTION_ID
* ARM_CLIENT_ID
* ARM_CLIENT_SECRET

Those secrets are the credentials for an [SP](https://learn.microsoft.com/en-us/azure/developer/terraform/authenticate-to-azure?tabs=bash)  and they will be used to authtenticate within Azure, and create the resoruces on the provider.
