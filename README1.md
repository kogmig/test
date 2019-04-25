# NewEgg Marketplace SDK for Java

Newegg Marketplace SDK(Java) is a library to help Java programmer easily integrates with Newegg Marketplace API. It provides the definition of the data objects models to help coder create the request and resolve the response. It also provides customize of logger and retry mechanism.

To use the SDK to communicate with Newegg API, you need to be a registered seller and get the 'Authorization' and 'Secret Key' from https://sellerportal.newegg.com. You can put this information into a 'newegg.properties' file, and load the setting from it by APIConfig.FromJsonFile method. Without the Authorization Token and Secret Key, you can run the test project with Simulation Mode. This mode is to help you understand the SDK before actual use.

The solution is based on jdk 1.8+. The library Dependents on:
- openfeign(10.1.0)
- log4j2(2.11.1)
- commons-configuration2(2.4)

## build
- mvn package

## Note
- There is a file  "newegg.properties" at same directory.
- The jar of common module must be keet.
- The properties of common module must be set up.
- If the APP not load the configuration ,the simulation will be enabled 

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

## Modules
### common
- used for other modules

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

## Change log
### 0.0.1
- initial
