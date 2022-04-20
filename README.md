# Starlify connector for mule gateway
Exports the Mulesoft API details to Starlify as systems and services.

## Dependencies
 Java-8 +

### spring-boot-starter-web
For exposure of connectors etc. on http.



## Start
Start by copying the project by using the link below:
https://github.com/entiros/starlify-mulesoft-anypointer-platform-connector.git

## Configuration
Make sure that the URL for MuleSoft API Gateway and Starlify is configured in your propertie file like below:

```
mulesoft:
  server:
    url: https://anypoint.mulesoft.com
starlify:
  url: https://api.starlify.com
```

To start the process, go to copied location and run the command below: 
mvn clean spring-boot:run

## import mule api details to Starlify
Use the endpoint below to start importing API details to Starlify as systems and flows:

```
	Method : POST
	URL : http://localhost:8080/submitRequest
	Body : 
			{
				"starlifyKey":"starlify-api-key",
				"apiKey":"mulesoft-api-key",
				"networkId":"starlify-network-id-to-create-services-systems-and-flows"
			}
```

## Output
After successful request submission, you should be able to see all the systems and services from Mulesoft in your Starlify network.
