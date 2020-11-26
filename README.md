# az-rest-api-postman

This is an Azure REST API samples for Postman API collection import. 

This collection has as reference the [Azure REST API Reference](https://docs.microsoft.com/en-us/rest/api/azure/) here you can find the endpoints, options and properties descriptions - value ones 😁 to guide us through the ☁ mission. 

The collection will be updated (or at least that the plan), and maybe someday we'll have here all the Azure REST API mapped. This should be usefull if you're testing or make developments with the REST API. We love Powershell and of course, the [Azure-Cli](https://docs.microsoft.com/en-us/cli/azure/) ❤ commands that allow scripting pretty much everything. But for those that are breathing APIs and REST formats, we believe that this collection it's a must.


## Want to contribute?

Please 😁 the Azure REST API is pretty much extensive, and we don't have all resources type at our current hand to create the requests samples. Please feel free to contribute and open PR.

Thanks to [@JoaoPedroDinis](https://github.com/JoaoPedroDinis) for his inputs and contributions 👍



## How to import


1. Install Postman desktop app - [download it here](https://www.postman.com/downloads/)
2. Clone this repo or download the files
3. Open Postman app and proceed with the [manual import process](https://learning.postman.com/docs/getting-started/importing-and-exporting-data/#importing-postman-data) or you can fork this repo into your github account and import directlty from [the Postman Github plugin](https://learning.postman.com/docs/getting-started/importing-and-exporting-data/#importing-postman-data). 😎 way more cool

![github-plugin](/media/git-plugin-1.png)

After established/authorized connection to your github account, select forked repo and the branch

![github-plugin](/media/git-plugin-2.png)

Select the files that you want to import. You'll find the environment vars and the collection that contains the API requests per folder per Azure service:

![github-plugin](/media/git-plugin-3.png)

And after you should have a collection like this: <br/>
![github-plugin](/media/Imported_collection.png)



## How to start using this collection

You should get familiar with [Postman variables](https://learning.postman.com/docs/sending-requests/variables/) and how you can use and set your environment var and reuse them. To interact with the requests you must have a valid Beared token issued with your account/subscription that has the necessary permissions required for it. 
* Get your Azure [subscription Id](https://docs.microsoft.com/en-us/powershell/module/servicemanagement/azure.service/get-azuresubscription?view=azuresmps-4.0.0)
* Get your [tenant Id](https://docs.microsoft.com/en-us/azure/marketplace/find-tenant-object-id)
* To obtain the bearer token, you need to [register an app at your Azure AD app registration](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow), grab the client_id and the client_secret to use at the imported environment vars. 
* Execute the Authentication/Auth.Login to obtain the bearer token and after a successfull response, set the environment var **az.bearerToken** to save the value and be used on other requests that requires it.
* Set the other vars with your subcription resources data, i.e., API Management name, and so on, because these vars are required at their specific API requests.

> This is a working progress project, so expect updates and probably some issues 😁☁
