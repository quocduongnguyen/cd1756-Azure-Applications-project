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
| Availability   | For any Single Instance Virtual Machine using Standard HDD Managed Disks for Operating System Disks and Data Disks, we guarantee you will have Virtual Machine Connectivity of at least 95%| Guarantee that Apps running in a customer subscription will be available 99.95% of the time. No SLA is provided for Apps under either the Free or Shared tiers. | Not a concern|
| Workflow       | Configuration of the application server/framework in the VM | Instant deployment. Vertical scaling, without having to redeploy| Simpler and faster|
|                |                                       |                                        |                              |
- My solution is App Service for deploying the app
- App Service has the advantage of being cheaper, simpler and faster to deploy, scalability and available is not a concern.
- If the application has a high demand for availability, scalability, control the underlying OS, install software on the server or change languages, then VM is better.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

Link myWeb: https://duongnq9-project1-web.azurewebsites.net/
My images in images folder