# IntegrationCollectionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCollectionsIntegrations**](IntegrationCollectionsApi.md#createCollectionsIntegrations) | **POST** /api/v1/integrations/collections | IntegrationCollectionController@store |
| [**deleteCollectionsIntegrations**](IntegrationCollectionsApi.md#deleteCollectionsIntegrations) | **DELETE** /api/v1/integrations/collections/{id} | Delete a collection |
| [**editCollectionsIntegrations**](IntegrationCollectionsApi.md#editCollectionsIntegrations) | **PATCH** /api/v1/integrations/collections/{id} | Edit a collection |
| [**fetchAllCollectionsIntegrations**](IntegrationCollectionsApi.md#fetchAllCollectionsIntegrations) | **GET** /api/v1/integrations/collections | IntegrationCollectionController@index |
| [**fetchCollectionsIntegrations**](IntegrationCollectionsApi.md#fetchCollectionsIntegrations) | **GET** /api/v1/integrations/collections/{id} | IntegrationCollectionController@show |
| [**updateCollectionsIntegrations**](IntegrationCollectionsApi.md#updateCollectionsIntegrations) | **PUT** /api/v1/integrations/collections/{id} | Update a collection |


<a id="createCollectionsIntegrations"></a>
# **createCollectionsIntegrations**
> CreateDarIntegration201Response createCollectionsIntegrations(createCollectionsIntegrationsRequest)

IntegrationCollectionController@store

Create a new collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationCollectionsApi apiInstance = new IntegrationCollectionsApi(defaultClient);
    CreateCollectionsIntegrationsRequest createCollectionsIntegrationsRequest = new CreateCollectionsIntegrationsRequest(); // CreateCollectionsIntegrationsRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createCollectionsIntegrations(createCollectionsIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationCollectionsApi#createCollectionsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createCollectionsIntegrationsRequest** | [**CreateCollectionsIntegrationsRequest**](CreateCollectionsIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteCollectionsIntegrations"></a>
# **deleteCollectionsIntegrations**
> DeleteApplications200Response deleteCollectionsIntegrations(id)

Delete a collection

Delete a collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationCollectionsApi apiInstance = new IntegrationCollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    try {
      DeleteApplications200Response result = apiInstance.deleteCollectionsIntegrations(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationCollectionsApi#deleteCollectionsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **Integer**| collection id | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="editCollectionsIntegrations"></a>
# **editCollectionsIntegrations**
> FetchCollections200Response editCollectionsIntegrations(id, createCollectionsIntegrationsRequest)

Edit a collection

Edit a collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationCollectionsApi apiInstance = new IntegrationCollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    CreateCollectionsIntegrationsRequest createCollectionsIntegrationsRequest = new CreateCollectionsIntegrationsRequest(); // CreateCollectionsIntegrationsRequest | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.editCollectionsIntegrations(id, createCollectionsIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationCollectionsApi#editCollectionsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **Integer**| collection id | |
| **createCollectionsIntegrationsRequest** | [**CreateCollectionsIntegrationsRequest**](CreateCollectionsIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="fetchAllCollectionsIntegrations"></a>
# **fetchAllCollectionsIntegrations**
> FetchAllCollections200Response fetchAllCollectionsIntegrations(name, perPage)

IntegrationCollectionController@index

Returns a list of collections

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationCollectionsApi apiInstance = new IntegrationCollectionsApi(defaultClient);
    String name = "name_example"; // String | Filter collections by name
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllCollections200Response result = apiInstance.fetchAllCollectionsIntegrations(name, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationCollectionsApi#fetchAllCollectionsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **name** | **String**| Filter collections by name | [optional] |
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchAllCollections200Response**](FetchAllCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchCollectionsIntegrations"></a>
# **fetchCollectionsIntegrations**
> FetchCollections200Response fetchCollectionsIntegrations(id)

IntegrationCollectionController@show

Get collection by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationCollectionsApi apiInstance = new IntegrationCollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    try {
      FetchCollections200Response result = apiInstance.fetchCollectionsIntegrations(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationCollectionsApi#fetchCollectionsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **Integer**| collection id | |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="updateCollectionsIntegrations"></a>
# **updateCollectionsIntegrations**
> FetchCollections200Response updateCollectionsIntegrations(id, createCollectionsIntegrationsRequest)

Update a collection

Update a collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationCollectionsApi apiInstance = new IntegrationCollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    CreateCollectionsIntegrationsRequest createCollectionsIntegrationsRequest = new CreateCollectionsIntegrationsRequest(); // CreateCollectionsIntegrationsRequest | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.updateCollectionsIntegrations(id, createCollectionsIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationCollectionsApi#updateCollectionsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **Integer**| collection id | |
| **createCollectionsIntegrationsRequest** | [**CreateCollectionsIntegrationsRequest**](CreateCollectionsIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

