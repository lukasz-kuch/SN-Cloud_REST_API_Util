
# Cloud-REST-API-Util
ServiceNow application for SN developers to debug the `MID Server script includes` in a very simple way. You just call `MID Server script include` and executes it using the available `MidServer`. This application allows you to send API Requests directly to the cloud client (as it works like for `POSTMAN` or `INSOMNIA`), so you can check all scripts and returned responses. It is very helpful when creating a new `MID Server script include`, checking what will return, compare the result with API's response.

MidServer Script Include functionality works based on OOTB ServiceNow Cloud API Base Script Include (e.g AzureCloudAPIBase, AWSCloudAPIBase, etc.)

## Instalation

* clone the repository
```powershel
git clone https://github.com/lukasz-kuch/MID-Server-API-Client.git
```
* push the code to your own repositorry
* in ServiceNow Studio use `Source Control integration` and Import applications from a Git repository

##  Requirements
* running MID Server that has access to a cloud environment
* Cloud Service Account (e.g. Azure AWS, VMWARE...)

## Usage of

### MID Server Script Includes

![alt text](https://github.com/lukasz-kuch/private-stuff/blob/main/api_client.png)

* populate your login credentials -> chooe provider and related cloud service account
* choose MID Server
* In MID Server Script Include tab put you line of code to call your intressted script

#### IMPORTANT
Please call the MID Server Script include using `params`as a parameter as it is required to pass login credential to MID Server CloudAPIBase script include. 
See following example:
```javascript
var req = new ExampleScriptInclude(params)
res = req.ExampleFunction()
```
### API Request

![alt text](https://github.com/lukasz-kuch/private-stuff/blob/main/script_include.png)

* populate your login credentials -> chooe provider and related cloud service account
* choose MID Server
* choose API Method
* paste Endpoint url 
* if your request require `RequestBody`, check RequestBody checkbox and provide body in JSON formatt (you can use `Prettify` button to formatt your JSON)
