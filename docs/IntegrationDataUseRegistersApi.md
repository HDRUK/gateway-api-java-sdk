# IntegrationDataUseRegistersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDurIntegrations**](IntegrationDataUseRegistersApi.md#createDurIntegrations) | **POST** /api/v1/integrations/dur | IntegrationDurController@store |
| [**deleteDurIntegrations**](IntegrationDataUseRegistersApi.md#deleteDurIntegrations) | **DELETE** /api/v1/integrations/dur/{id} | Delete a dur |
| [**editDurIntegrations**](IntegrationDataUseRegistersApi.md#editDurIntegrations) | **PATCH** /api/v1/integrations/dur/{id} | Edit a dur |
| [**fetchAllDurIntegrations**](IntegrationDataUseRegistersApi.md#fetchAllDurIntegrations) | **GET** /api/v1/integrations/dur | IntegrationDurController@index |
| [**fetchDurByIdIntegrations**](IntegrationDataUseRegistersApi.md#fetchDurByIdIntegrations) | **GET** /api/v1/integrations/dur/{id} | IntegrationDurController@show |
| [**updateDurIntegrations**](IntegrationDataUseRegistersApi.md#updateDurIntegrations) | **PUT** /api/v1/integrations/dur/{id} | Update a dur by id |


<a id="createDurIntegrations"></a>
# **createDurIntegrations**
> CreateDarIntegration201Response createDurIntegrations(createDurIntegrationsRequest)

IntegrationDurController@store

Create a new dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationDataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationDataUseRegistersApi apiInstance = new IntegrationDataUseRegistersApi(defaultClient);
    CreateDurIntegrationsRequest createDurIntegrationsRequest = new CreateDurIntegrationsRequest(); // CreateDurIntegrationsRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createDurIntegrations(createDurIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationDataUseRegistersApi#createDurIntegrations");
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
| **createDurIntegrationsRequest** | [**CreateDurIntegrationsRequest**](CreateDurIntegrationsRequest.md)| Pass user credentials | |

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

<a id="deleteDurIntegrations"></a>
# **deleteDurIntegrations**
> DeleteApplications200Response deleteDurIntegrations(id)

Delete a dur

Delete a dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationDataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationDataUseRegistersApi apiInstance = new IntegrationDataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    try {
      DeleteApplications200Response result = apiInstance.deleteDurIntegrations(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationDataUseRegistersApi#deleteDurIntegrations");
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
| **id** | **Integer**| dur id | |

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

<a id="editDurIntegrations"></a>
# **editDurIntegrations**
> UpdateDurIntegrations200Response editDurIntegrations(id, createDurIntegrationsRequest)

Edit a dur

Edit a dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationDataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationDataUseRegistersApi apiInstance = new IntegrationDataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    CreateDurIntegrationsRequest createDurIntegrationsRequest = new CreateDurIntegrationsRequest(); // CreateDurIntegrationsRequest | Pass user credentials
    try {
      UpdateDurIntegrations200Response result = apiInstance.editDurIntegrations(id, createDurIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationDataUseRegistersApi#editDurIntegrations");
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
| **id** | **Integer**| dur id | |
| **createDurIntegrationsRequest** | [**CreateDurIntegrationsRequest**](CreateDurIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**UpdateDurIntegrations200Response**](UpdateDurIntegrations200Response.md)

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

<a id="fetchAllDurIntegrations"></a>
# **fetchAllDurIntegrations**
> FetchAllDurIntegrations200Response fetchAllDurIntegrations(sort, perPage)

IntegrationDurController@index

Returns a list of dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationDataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IntegrationDataUseRegistersApi apiInstance = new IntegrationDataUseRegistersApi(defaultClient);
    ProjectTitleAscupdatedAtAsc sort = new ProjectTitleAscupdatedAtAsc(); // ProjectTitleAscupdatedAtAsc | Sort fields in the format field:direction, e.g., project_title:asc,updated_at:asc
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllDurIntegrations200Response result = apiInstance.fetchAllDurIntegrations(sort, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationDataUseRegistersApi#fetchAllDurIntegrations");
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
| **sort** | [**ProjectTitleAscupdatedAtAsc**](.md)| Sort fields in the format field:direction, e.g., project_title:asc,updated_at:asc | [optional] |
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchAllDurIntegrations200Response**](FetchAllDurIntegrations200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchDurByIdIntegrations"></a>
# **fetchDurByIdIntegrations**
> FetchDurByIdIntegrations200Response fetchDurByIdIntegrations(id)

IntegrationDurController@show

Get dur by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationDataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationDataUseRegistersApi apiInstance = new IntegrationDataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | data use register id
    try {
      FetchDurByIdIntegrations200Response result = apiInstance.fetchDurByIdIntegrations(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationDataUseRegistersApi#fetchDurByIdIntegrations");
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
| **id** | **Integer**| data use register id | |

### Return type

[**FetchDurByIdIntegrations200Response**](FetchDurByIdIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="updateDurIntegrations"></a>
# **updateDurIntegrations**
> UpdateDurIntegrations200Response updateDurIntegrations(id, createDurIntegrationsRequest)

Update a dur by id

Update a dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationDataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    IntegrationDataUseRegistersApi apiInstance = new IntegrationDataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    CreateDurIntegrationsRequest createDurIntegrationsRequest = new CreateDurIntegrationsRequest(); // CreateDurIntegrationsRequest | Pass user credentials
    try {
      UpdateDurIntegrations200Response result = apiInstance.updateDurIntegrations(id, createDurIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationDataUseRegistersApi#updateDurIntegrations");
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
| **id** | **Integer**| dur id | |
| **createDurIntegrationsRequest** | [**CreateDurIntegrationsRequest**](CreateDurIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**UpdateDurIntegrations200Response**](UpdateDurIntegrations200Response.md)

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

