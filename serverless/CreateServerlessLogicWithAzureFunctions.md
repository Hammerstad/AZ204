# Create serverless logic with Azure Functions

## Decide if serverless computing is right for your business needs

### Benefits
 - Avoids over-allocation of infrastructure
 - Stateless logic
 - Event driven
 - Functions can be used in traditional compute envs

### Drawbacks
 - Execution time (timeout of 5 mins, max 10 min) Also option of durable function
 - Execution frequency: if called often, perhaps cheaper to host in VM

## Exercise

### Service plans:

Consumption service plan: Auto scaling and bills you when functions are running. Configurable timeout period (def: 5min, max 10 min)
Azure App Service plan: Avoid timeout periods by having function run on a VM you define. You have to manage the VM, so technically not functional.

Function app must be linked with storage account. Used for internal operations such as logging.

## Run your code on-demand with Azure Functions

### Triggers
An event which starts a function is called a trigger. A function needs exactly one trigger. Azure supports the following triggers:
 - Blob storage (new or updated blob detected)
 - Azure Cosmos DB (insert/update)
 - Event Grid (when events are received)
 - HTTP (start by request)
 - Microsoft Graph Events (Reponse to webhook from MGE. One trigger instance can react toe one MG resource type)
 - Queue storage (item received on queue. Message becomes input to function).
 - Service bus (in response to msg on queue)
 - Timer

### Bindings

Each function can have 0-many bindings to manage input/output. Azure supports lots of bindings.