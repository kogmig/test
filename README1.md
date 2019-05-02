# NewEgg Marketplace SDK for Java

Newegg Marketplace SDK(Java) is a library to help Java programmer easily integrates with Newegg Marketplace API. It provides the definition of the data objects models to help coder create the request and resolve the response. It also provides customize of logger and retry mechanism.

To use the SDK to communicate with the Newegg API, you need to be a registered seller and get the 'API Key(Authorization)' and 'Secret Key'  by mail Datafeeds@newegg.com. You can put this information into a 'newegg.properties' file. Without the Authorization Token and Secret Key, you can run the test project with Simulation Mode. This mode is to help you understand the SDK before actual use.

The solution is based on jdk 1.8+. The library Dependents on:
- openfeign(10.1.0)
- log4j2(2.11.1)
- commons-configuration2(2.4)

## install
- from Maven
## build
- mvn package

## Note
- There is a file  "newegg.properties" at same directory.
- The jar of common module must be keet.
- The properties of common module must be set up.
- If the APP not load the configuration ,the simulation will be enabled 


## Q&A
```
How to load configuration ?
APIConfig.load(SellerConfig.class);

```
- Log4j configuration file location

```
By default, Log4j looks for a configuration file named log4j2.xml (not log4j.xml) in the classpath.
You can also specify the full path of the configuration file with this system property: -Dlog4j.configurationFile=path/to/log4j2.xml
Web applications can specify the Log4j configuration file location with a servlet context parameter.
```

## Modules docs

### Item
- Item Management  
    https://developer.newegg.com/newegg_marketplace_api/item_management/

### Seller
- Seller Management  
    https://developer.newegg.com/newegg_marketplace_api/seller_management/

### Order
- Order Management  
    https://developer.newegg.com/newegg_marketplace_api/order_management/
    
### Shipping
- Newegg Shipping Label Service  
    https://developer.newegg.com/newegg_marketplace_api/newegg_shipping_label_service/

### Other
- Verify Service Status  
    https://developer.newegg.com/newegg_marketplace_api/verify_service_status/

### SBN
- Shipped by Newegg Management  
    https://developer.newegg.com/newegg_marketplace_api/sbn_shipped_by_newegg_management/
    
### DataFeed
- DataFeed Management  
    https://developer.newegg.com/newegg_marketplace_api/datafeed_management/

### Report
- Reports Management  
    https://developer.newegg.com/newegg_marketplace_api/reports_management/

### RMA
- RMA(Return Merchandise Authorization) Management  
    https://developer.newegg.com/newegg_marketplace_api/rma_management/

