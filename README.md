# ProcFwk

## Author / Creator of ProcFwk
[Paul Andrew](https://github.com/mrpaulandrew)

[ProcFwk Home Page](https://mrpaulandrew.github.io/procfwk/)

[GitHub Project mrpauandrew/procfwk](https://github.com/mrpaulandrew/procfwk)

## Deploy to Azure
[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Foh22is%2FProcFwk%2Fmain%2FmainTemplate.json)  [![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](https://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Foh22is%2FProcFwk%2Fmain%2FmainTemplate.json)

## Resources

The resources are created as described here: [ProcFwk Deployment Guide](https://mrpaulandrew.github.io/procfwk/deployprocfwk)

| ResourceName                            | DeploymentName | DependsOn |
|-----------------------------------------|----------------|-----------|
| pid-e2854d4f-806a-48ab-82f4-f3e410913fdd | same like resource name | none      |  
| ADF                                     | deploy_adf      | none      |  
| ADF Role Assignment                     | deploy_adf_roleAssignment| deploy_adf, deploy_sql |   
| SQL Server / Database                   | deploy_sql      | none      |
| Function App / Consumption Service Plan | deploy_func     | none      |
| Key Vault                               | deploy_akv      | deploy_adf, deploy_func, deploy_sql|

## Check the following after deployment
* The Data Factory should have MSI access to itself as an owner
* The Data Factory should be listed in the access policy of the key vault and have the secret permission "get"
* The Key Vault should contain following secrets: function app default key, sql databse user name, sql database user password, sql database connection string

## What's next?
At this point you have the underlying resources avaiable.

Time to [deploy the code](https://mrpaulandrew.github.io/procfwk/deployprocfwk#deploying-code), [create a service principal](https://mrpaulandrew.github.io/procfwk/deployprocfwk#service-principals), ...

[For further steps, please check Pauls deployment guide.](https://mrpaulandrew.github.io/procfwk/deployprocfwk)
