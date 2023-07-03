# Eclipse BaSyx - AssetAdministrationShell Repository 
Eclipse BaSyx provides the AssetAdministrationShell Repository as off-the-shelf component:

    docker run --name=aas-repo -p:8081:8081 -v C:/tmp:/usr/share/config eclipsebasyx/aas-repository:2.0.0-SNAPSHOT 

The API endpoint documentation is available at:

	http://{host}:{port}/v3/api-docs
	
The Swagger UI for the endpoint is available at:

	http://{host}:{port}/swagger-ui/index.html

It supports DotAAS Part 1 V3 and the following HTTP/REST endpoints defined in [DotAAS Part 2 V3 - AssetAdministrationShell Repository](https://app.swaggerhub.com/apis/Plattform_i40/AssetAdministrationShellRepositoryServiceSpecification/V3.0_SSP-001):

* AAS Repository:
  * PostAssetAdministrationShell
  * GetAllAssetAdministrationShells
  * GetAssetAdministrationShellById
  * PutAssetAdministrationShellById
  * DeleteAssetAdministrationShellById
* AAS Service
  * GetAllSubmodelReferences
  * PostSubmodelReference
  * DeleteSubmodelReference
  * GetAssetInformation
  * PutAssetInformation

Right now, no additional input parameters modifying the output (e.g., cursor, serializationModifier) are supported.

In addition, it supports the following backends:
* InMemory
* MongoDB

Furthermore, the following features are provided:
* [AAS Repository MQTT eventing](basyx.aasrepository-feature-mqtt/Readme.md)
* [AAS Service MQTT eventing](../basyx.aasservice/basyx.aasservice-feature-mqtt/Readme.md)

For a configuration example, see [application.properties](basyx.aasrepository.component/src/main/resources/application.properties)