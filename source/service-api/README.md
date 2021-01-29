# managedServicesApi

Managed Service API

- API version: 0.0.1

- Build date: 2021-01-05T13:06:07.039699Z[Europe/Dublin]

Managed Service API


*Automatically generated by the [OpenAPI Generator](https://openapi-generator.tech)*

## Requirements

Building the API client library requires:

1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>org.openapitools</groupId>
  <artifactId>managedServicesApi</artifactId>
  <version>0.0.1</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "org.openapitools:managedServicesApi:0.0.1"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

- `target/managedServicesApi-0.0.1.jar`
- `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.openshift.cloud.*;
import com.openshift.cloud.auth.*;
import com.openshift.cloud.api.models.*;
import com.openshift.cloud.api.DefaultApi;

public class DefaultApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.openshift.com");
        
        // Configure HTTP bearer authorization: Bearer
        HttpBearerAuth Bearer = (HttpBearerAuth) defaultClient.getAuthentication("Bearer");
        Bearer.setBearerToken("BEARER TOKEN");

        DefaultApi apiInstance = new DefaultApi(defaultClient);
        Boolean async = true; // Boolean | Perform the action in an asynchronous manner
        KafkaRequestPayload kafkaRequestPayload = new KafkaRequestPayload(); // KafkaRequestPayload | Kafka data
        try {
            KafkaRequest result = apiInstance.createKafka(async, kafkaRequestPayload);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#createKafka");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://api.openshift.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**createKafka**](docs/DefaultApi.md#createKafka) | **POST** /api/managed-services-api/v1/kafkas | Create a new kafka Request
*DefaultApi* | [**createServiceAccount**](docs/DefaultApi.md#createServiceAccount) | **POST** /api/managed-services-api/v1/serviceaccounts | Create a service account
*DefaultApi* | [**deleteKafkaById**](docs/DefaultApi.md#deleteKafkaById) | **DELETE** /api/managed-services-api/v1/kafkas/{id} | Delete a kafka request by id
*DefaultApi* | [**deleteServiceAccount**](docs/DefaultApi.md#deleteServiceAccount) | **DELETE** /api/managed-services-api/v1/serviceaccounts/{id} | Delete service account
*DefaultApi* | [**getKafkaById**](docs/DefaultApi.md#getKafkaById) | **GET** /api/managed-services-api/v1/kafkas/{id} | Get a kafka request by id
*DefaultApi* | [**listCloudProviderRegions**](docs/DefaultApi.md#listCloudProviderRegions) | **GET** /api/managed-services-api/v1/cloud_providers/{id}/regions | Retrieves the list of supported regions of the supported cloud provider.
*DefaultApi* | [**listCloudProviders**](docs/DefaultApi.md#listCloudProviders) | **GET** /api/managed-services-api/v1/cloud_providers | Retrieves the list of supported cloud providers.
*DefaultApi* | [**listKafkas**](docs/DefaultApi.md#listKafkas) | **GET** /api/managed-services-api/v1/kafkas | Returns a list of Kafka requests
*DefaultApi* | [**listServiceAccounts**](docs/DefaultApi.md#listServiceAccounts) | **GET** /api/managed-services-api/v1/serviceaccounts | List service accounts
*DefaultApi* | [**resetServiceAccountCreds**](docs/DefaultApi.md#resetServiceAccountCreds) | **POST** /api/managed-services-api/v1/serviceaccounts/{id}/reset-credentials | reset credentials for the service account


## Documentation for Models

 - [CloudProvider](docs/CloudProvider.md)
 - [CloudProviderList](docs/CloudProviderList.md)
 - [CloudProviderListAllOf](docs/CloudProviderListAllOf.md)
 - [CloudRegion](docs/CloudRegion.md)
 - [CloudRegionList](docs/CloudRegionList.md)
 - [CloudRegionListAllOf](docs/CloudRegionListAllOf.md)
 - [Error](docs/Error.md)
 - [ErrorAllOf](docs/ErrorAllOf.md)
 - [ErrorList](docs/ErrorList.md)
 - [ErrorListAllOf](docs/ErrorListAllOf.md)
 - [KafkaRequest](docs/KafkaRequest.md)
 - [KafkaRequestAllOf](docs/KafkaRequestAllOf.md)
 - [KafkaRequestList](docs/KafkaRequestList.md)
 - [KafkaRequestListAllOf](docs/KafkaRequestListAllOf.md)
 - [KafkaRequestPayload](docs/KafkaRequestPayload.md)
 - [ObjectReference](docs/ObjectReference.md)
 - [ServiceAccount](docs/ServiceAccount.md)
 - [ServiceAccountAllOf](docs/ServiceAccountAllOf.md)
 - [ServiceAccountList](docs/ServiceAccountList.md)
 - [ServiceAccountListAllOf](docs/ServiceAccountListAllOf.md)
 - [ServiceAccountListItem](docs/ServiceAccountListItem.md)
 - [ServiceAccountListItemAllOf](docs/ServiceAccountListItemAllOf.md)
 - [ServiceAccountRequest](docs/ServiceAccountRequest.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### Bearer


- **Type**: HTTP basic authentication


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author


