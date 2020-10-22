# Workshop-CosmosDB

## Exercise 1 - Create CosmosDB Account
In this exercise we will use the Azure portal to create an Azure Cosmos DB SQL API account, create a document database and container and add data to the container.

You can refer ["Microsoft Docs - Create an Azure Cosmos account, container, and items"](https://docs.microsoft.com/en-us/azure/cosmos-db/create-cosmosdb-resources-portal) for this excercise.

### Steps

In the Azure portal...
1. Create an Azure Cosmos DB account. 
   * Click on **+ Create a resource** and search for `Azure Cosmos DB`. Click **Create**.
   * Select below options while creating Cosmos DB account
       * *Resource Group:* **Create new**
         * *Name:* `az{your_id}-cosmosdb-rg`
       * *Account Name*: `az{your_id}-cosmosdb`
       * *API*: `Core (SQL)`
       * *Location*: `West Europe`
       * *Capacity Mode*: `Provisioned throughput`
       * *Account Type*: `Non-Production`
       * *Geo-Redundancy*: `Disabled`
       * *Multi-region Writes*: `Disabled`
    
    **NOTE:** The database account will take approx. 5-10 minutes to be created.
2. Create a database in the Cosmos DB account. In the CosmosDB's select **Data Explorer** to open the data explorer blade.
    * From the drop dwon at the top of the blade, select **New Database**
    * *Database Id*: `DemoDatabase`
    * *Provision throughput*: `Enabled`
    * *Throughput*: `400 (Manual)`
3. Add a container. From the drop dwon at the top of the blade, select **New Container**
    * *Database Id*: **Use Existing** `DemoDatabase`
    * *Container Id*: `Families`
    * *Partition Key*: `/id`
4. Add data to your container.
    * Select the `ToDoList` container created, and from the menu at the top of the blade click **New Item**.
    * Paste the json snippet below, which represents a new item in our todo list.
    ```json
    {
        "id": "BD739417-E69A-41FB-BF7C-7C4D7D487B28",
        "category": "personal",
        "name": "groceries",
        "description": "Pick up apples and strawberries.",
        "isComplete": false
    }
    ```
    * Click **Save**
    
**Note:** After saving the document you will notice several fields have been automatically added by Cosmos DB. `_rid`, `_self`, `_etag`, `_attachments`, and `_ts`.
You can read more about these tags [here](https://docs.microsoft.com/en-us/rest/api/cosmos-db/collections).

## Exercise 2 - Create a blank ASP.NET Core MVC application
In this exercise we will create a ASP.NET Core MVC application with controllers and views.

You can refer ["Microsoft Docs - Get started with ASP.NET Core MVC"](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc) for this excercise.

## Exercise 3 - Set up the ASP.NET Core MVC application

### Steps
