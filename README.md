# NewEgg Marketplace SDK for .Net

Newegg Marketplace SDK(C#) is a library to help .Net programmer easily integrates with Newegg Marketplace API. It provides the definition of the data objects models to help coder create the request and resolve the response. It also provides customize of logger and retry mechanism. 

To use the SDK to communicate with Newegg API, you need to be a registered seller and get the 'Authorization' and 'Secret Key' from https://sellerportal.newegg.com. You can put this information into a JSON file, and load the setting from it by APIConfig.FromJsonFile method.
Without the Authorization Token and Secret Key, you can run the test project with Simulation Mode. This mode is to help you understand the SDK before actual use.  

The solution contains 2 library projects: Newegg.Marketplace.SDK.Base and Newegg.Marketplace.SDK. The first one is the framework of the SDK, and the second one is the business logic model and interface to various API. The code is base on .NET Standard 2.0, you can build it with .Net framework 4.6 or .Net Core 2.1 too.


## Target Frameworks

* .NET Standard 2.0 

## Installation

Download the zip file according to your framework, then upzip it.
You can choose manually build it and link library from your project or direct include the project to your solution.
We recommend using Visual Studio 2017 or later. You can choose to build it with the command following too.


## build
- To build  
    `dotnet build Newegg.Marketplace.SDK`    
- Nuget library
    The library Dependents on 'Newtonsoft.Json(12.0.1)' and 'NLog(4.6.2)'.
    

## Q&A
- How to use the SDK?
1. We recommed setting these infomation in a json file as below. 
```json
{    
  "SellerID": "****",
  "Credentials": {
    "Authorization": "********************************",
    "SecretKey": "*******-****-****-****-************"
  },
  "Connection": {
    "RequestTimeoutMs": 30000,
    "AttemptsTimes": 5,
    "RetryIntervalMs": 1000
  },
  "APIFormat": "XML",
  "Platform": "CAN"
}
```

2. load the configuration to a APIConfig object.
```csharp
APIConfig config = APIConfig.FromJsonFile(PathOfTheJSONConfigFile);
```
3. Create a APIClient with the config.
```csharp
APIClient client = new APIClient(config);
```
4. Create the APICall object with the APIClien.
```csharp
OrderCall ordercall = new OrderCall(client);
```
5. Use the APICall object to call API.
```csharp
var orderstatus = await ordercall.GetOrderStatus("105137040", 304);
```    

- NLog configuration file location
    
Please refer https://github.com/NLog/NLog/wiki/Configuration-file#configuration-file-locations


## Modules

### Item
- Item Management

### Seller
- Seller Management

### Order
- Order Management

### Shipping
- Newegg Shipping Label Service

### Other
- Verify Service Status

### SBN
- Shipped by Newegg Management

### DataFeed
- DataFeed Management

### Report
- Reports Management

### RMA
- RMA(Return Merchandise Authorization) Management
