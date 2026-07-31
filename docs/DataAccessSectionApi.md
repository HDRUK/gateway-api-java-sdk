# DataAccessSectionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDarSection**](DataAccessSectionApi.md#createDarSection) | **POST** /api/v1/dar/sections | DataAccessSection@store |
| [**deleteDarSection**](DataAccessSectionApi.md#deleteDarSection) | **DELETE** /api/v1/dar/sections/{id} | DataAccessSection@destroy |
| [**fetchDarSection**](DataAccessSectionApi.md#fetchDarSection) | **GET** /api/v1/dar/sections/{id} | DataAccessSection@show |
| [**fetchDarSections**](DataAccessSectionApi.md#fetchDarSections) | **GET** /api/v1/dar/sections | DataAccessSection@index |
| [**patchDarSection**](DataAccessSectionApi.md#patchDarSection) | **PATCH** /api/v1/dar/sections/{id} | DataAccessSection@update |
| [**updateDarSection**](DataAccessSectionApi.md#updateDarSection) | **PUT** /api/v1/dar/sections/{id} | DataAccessSection@update |


<a id="createDarSection"></a>
# **createDarSection**
> CreateCategories200Response createDarSection(createDarSectionRequest)

DataAccessSection@store

Creates a new DAR section

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessSectionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessSectionApi apiInstance = new DataAccessSectionApi(defaultClient);
    CreateDarSectionRequest createDarSectionRequest = new CreateDarSectionRequest(); // CreateDarSectionRequest | DataAccessSection definition
    try {
      CreateCategories200Response result = apiInstance.createDarSection(createDarSectionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessSectionApi#createDarSection");
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
| **createDarSectionRequest** | [**CreateDarSectionRequest**](CreateDarSectionRequest.md)| DataAccessSection definition | |

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
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteDarSection"></a>
# **deleteDarSection**
> DeleteAliases200Response deleteDarSection(id)

DataAccessSection@destroy

Delete a system DAR section

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessSectionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessSectionApi apiInstance = new DataAccessSectionApi(defaultClient);
    Integer id = 1; // Integer | DAR section id
    try {
      DeleteAliases200Response result = apiInstance.deleteDarSection(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessSectionApi#deleteDarSection");
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
| **id** | **Integer**| DAR section id | |

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

<a id="fetchDarSection"></a>
# **fetchDarSection**
> FetchDarSection200Response fetchDarSection(id)

DataAccessSection@show

Return a single DAR section

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessSectionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessSectionApi apiInstance = new DataAccessSectionApi(defaultClient);
    Integer id = 1; // Integer | DAR section id
    try {
      FetchDarSection200Response result = apiInstance.fetchDarSection(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessSectionApi#fetchDarSection");
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
| **id** | **Integer**| DAR section id | |

### Return type

[**FetchDarSection200Response**](FetchDarSection200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchDarSections"></a>
# **fetchDarSections**
> FetchDarSections200Response fetchDarSections(perPage)

DataAccessSection@index

List of DAR sections

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessSectionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessSectionApi apiInstance = new DataAccessSectionApi(defaultClient);
    Integer perPage = 1; // Integer | per page
    try {
      FetchDarSections200Response result = apiInstance.fetchDarSections(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessSectionApi#fetchDarSections");
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
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchDarSections200Response**](FetchDarSections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="patchDarSection"></a>
# **patchDarSection**
> FetchDarSection200Response patchDarSection(id, patchDarSectionRequest)

DataAccessSection@update

Edit a system DAR section

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessSectionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessSectionApi apiInstance = new DataAccessSectionApi(defaultClient);
    Integer id = 1; // Integer | DAR section id
    PatchDarSectionRequest patchDarSectionRequest = new PatchDarSectionRequest(); // PatchDarSectionRequest | DataAccessSection definition
    try {
      FetchDarSection200Response result = apiInstance.patchDarSection(id, patchDarSectionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessSectionApi#patchDarSection");
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
| **id** | **Integer**| DAR section id | |
| **patchDarSectionRequest** | [**PatchDarSectionRequest**](PatchDarSectionRequest.md)| DataAccessSection definition | |

### Return type

[**FetchDarSection200Response**](FetchDarSection200Response.md)

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

<a id="updateDarSection"></a>
# **updateDarSection**
> FetchDarSection200Response updateDarSection(id, createDarSectionRequest)

DataAccessSection@update

Update a system DAR section

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessSectionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessSectionApi apiInstance = new DataAccessSectionApi(defaultClient);
    Integer id = 1; // Integer | DAR section id
    CreateDarSectionRequest createDarSectionRequest = new CreateDarSectionRequest(); // CreateDarSectionRequest | DataAccessSection definition
    try {
      FetchDarSection200Response result = apiInstance.updateDarSection(id, createDarSectionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessSectionApi#updateDarSection");
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
| **id** | **Integer**| DAR section id | |
| **createDarSectionRequest** | [**CreateDarSectionRequest**](CreateDarSectionRequest.md)| DataAccessSection definition | |

### Return type

[**FetchDarSection200Response**](FetchDarSection200Response.md)

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

