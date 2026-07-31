# DarIntegrationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDarIntegration**](DarIntegrationApi.md#createDarIntegration) | **POST** /api/v1/dar-integration/{id} | DarIntegration@store |
| [**deleteDarIntegration**](DarIntegrationApi.md#deleteDarIntegration) | **DELETE** /api/v1/dar-integrations/{id} | DarIntegration@destroy |
| [**editDarIntegration**](DarIntegrationApi.md#editDarIntegration) | **PATCH** /api/v1/dar-integration/{id} | DarIntegration@edit |
| [**fetchAllDarIntegrations**](DarIntegrationApi.md#fetchAllDarIntegrations) | **GET** /api/v1/dar-integration | DarIntegration@index |
| [**fetchDarIntegration**](DarIntegrationApi.md#fetchDarIntegration) | **GET** /api/v1/dar-integration/{id} | DarIntegration@show |
| [**updateDarIntegration**](DarIntegrationApi.md#updateDarIntegration) | **PUT** /api/v1/dar-integration/{id} | DarIntegration@update |


<a id="createDarIntegration"></a>
# **createDarIntegration**
> CreateCategories200Response createDarIntegration(id, updateDarIntegrationRequest)

DarIntegration@store

Creates a new DAR integration enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DarIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DarIntegrationApi apiInstance = new DarIntegrationApi(defaultClient);
    Integer id = 1; // Integer | dar integration id
    UpdateDarIntegrationRequest updateDarIntegrationRequest = new UpdateDarIntegrationRequest(); // UpdateDarIntegrationRequest | DarIntegration definition
    try {
      CreateCategories200Response result = apiInstance.createDarIntegration(id, updateDarIntegrationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DarIntegrationApi#createDarIntegration");
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
| **id** | **Integer**| dar integration id | |
| **updateDarIntegrationRequest** | [**UpdateDarIntegrationRequest**](UpdateDarIntegrationRequest.md)| DarIntegration definition | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

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

<a id="deleteDarIntegration"></a>
# **deleteDarIntegration**
> DeleteAliases200Response deleteDarIntegration(id)

DarIntegration@destroy

Delete a system Dar Integration

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DarIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DarIntegrationApi apiInstance = new DarIntegrationApi(defaultClient);
    Integer id = 1; // Integer | dar integration id
    try {
      DeleteAliases200Response result = apiInstance.deleteDarIntegration(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DarIntegrationApi#deleteDarIntegration");
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
| **id** | **Integer**| dar integration id | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

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

<a id="editDarIntegration"></a>
# **editDarIntegration**
> UpdateDarIntegration200Response editDarIntegration(id, editDarIntegrationRequest)

DarIntegration@edit

Edit a DAR integration enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DarIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DarIntegrationApi apiInstance = new DarIntegrationApi(defaultClient);
    Integer id = 1; // Integer | dar integration id
    EditDarIntegrationRequest editDarIntegrationRequest = new EditDarIntegrationRequest(); // EditDarIntegrationRequest | DarIntegration definition
    try {
      UpdateDarIntegration200Response result = apiInstance.editDarIntegration(id, editDarIntegrationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DarIntegrationApi#editDarIntegration");
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
| **id** | **Integer**| dar integration id | |
| **editDarIntegrationRequest** | [**EditDarIntegrationRequest**](EditDarIntegrationRequest.md)| DarIntegration definition | |

### Return type

[**UpdateDarIntegration200Response**](UpdateDarIntegration200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="fetchAllDarIntegrations"></a>
# **fetchAllDarIntegrations**
> FetchAllDarIntegrations200Response fetchAllDarIntegrations()

DarIntegration@index

Returns a list of DAR integrations enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DarIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DarIntegrationApi apiInstance = new DarIntegrationApi(defaultClient);
    try {
      FetchAllDarIntegrations200Response result = apiInstance.fetchAllDarIntegrations();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DarIntegrationApi#fetchAllDarIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**FetchAllDarIntegrations200Response**](FetchAllDarIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **401** | Unauthorized |  -  |

<a id="fetchDarIntegration"></a>
# **fetchDarIntegration**
> FetchAllDarIntegrations200ResponseDataInner fetchDarIntegration(id)

DarIntegration@show

Returns a single DAR integration enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DarIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DarIntegrationApi apiInstance = new DarIntegrationApi(defaultClient);
    Integer id = 1; // Integer | dar integration id
    try {
      FetchAllDarIntegrations200ResponseDataInner result = apiInstance.fetchDarIntegration(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DarIntegrationApi#fetchDarIntegration");
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
| **id** | **Integer**| dar integration id | |

### Return type

[**FetchAllDarIntegrations200ResponseDataInner**](FetchAllDarIntegrations200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="updateDarIntegration"></a>
# **updateDarIntegration**
> UpdateDarIntegration200Response updateDarIntegration(id, updateDarIntegrationRequest)

DarIntegration@update

Updates a DAR integration enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DarIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DarIntegrationApi apiInstance = new DarIntegrationApi(defaultClient);
    Integer id = 1; // Integer | dar integration id
    UpdateDarIntegrationRequest updateDarIntegrationRequest = new UpdateDarIntegrationRequest(); // UpdateDarIntegrationRequest | DarIntegration definition
    try {
      UpdateDarIntegration200Response result = apiInstance.updateDarIntegration(id, updateDarIntegrationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DarIntegrationApi#updateDarIntegration");
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
| **id** | **Integer**| dar integration id | |
| **updateDarIntegrationRequest** | [**UpdateDarIntegrationRequest**](UpdateDarIntegrationRequest.md)| DarIntegration definition | |

### Return type

[**UpdateDarIntegration200Response**](UpdateDarIntegration200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

