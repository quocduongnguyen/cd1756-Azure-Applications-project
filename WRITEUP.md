# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*

|                | Virtual Machines                      | App Service                            | Application needs            |
| :------------- |:--------------------------------------| :--------------------------------------|:-----------------------------|
| Costs (Minimum)| 1 A0 (1 vCPU, 0.75 GB RAM). Monthly: $13.19| Free Tier; 1 F1 (0 Core(s), 1 GB RAM, 1 GB Storage). Monthly: $0.00, enough to deploy the application| As cheap as possible|
| Scalability    |                                       |                                        | Not a concern                |
|   Autoscaling  | Virtual machine scale sets            | Built-in service                       |                              |
|   Load balancer| Azure Load Balancer                   | Integrated                             |                              |
|   Scale limit  | Platform image: 1000 nodes per scale set, Custom image: 600 nodes per scale set| 30 instances, 100 with App Service Environment, maximum of 14GB of memory and 4 vCPU cores per instance|                              |
|                |                                       |                                        |                              |
|                |                                       |                                        |                              |
|                |                                       |                                        |                              |
|                |                                       |                                        |                              |
|                |                                       |                                        |                              |
|                |                                       |                                        |                              |

- Analyze costs: App Service is cheaper than VM, scalability: this web app is using small resources and is less scalable so it is not a concern now, availability: both are highly available, VM is slightly better but it is not a concern now, and workflow: using App Service is simpler and faster
- My solution is App Service for deploying the app
- App Service has the advantage of being cheaper, simpler and faster to deploy, scalability and available is not a concern.
- If the application has a high demand for availability, scalability, control the underlying OS, install software on the server or change languages, then VM is better.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

Link myWeb: https://duongnq9-project1-web.azurewebsites.net/
My images in images folder