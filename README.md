# ProcFwk

## Author / Creator of ProcFwk
[Paul Andrew](https://github.com/mrpaulandrew)

[ProcFwk Home Page](https://mrpaulandrew.github.io/procfwk/)

[GitHub Project mrpauandrew/procfwk](https://github.com/mrpaulandrew/procfwk)

## Deploy to Azure
[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Foh22is%2FProcFwk%2Fmain%2FmainTemplate.json)  [![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](https://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Foh22is%2FProcFwk%2Fmain%2FmainTemplate.json)

## Resources
| Name                                    | DependsOn |
|-----------------------------------------|-----------|
| id-e2854d4f-806a-48ab-82f4-f3e410913fdd | none      |  
| ADF                                     | none      |  
| ADF Role Assignment                     | ADF, SQL  |   
| SQL Server / Database                   | none      |
| Function App / Consumption Service Plan | none      |
| Key Vault                               | ADF, Function, SQL|
