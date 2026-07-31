# LibraryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createLibraries**](LibraryApi.md#createLibraries) | **POST** /api/v1/libraries | Library@store |
| [**deleteLibraries**](LibraryApi.md#deleteLibraries) | **DELETE** /api/v1/libraries/{id} | Library@destroy |
| [**editLibraries**](LibraryApi.md#editLibraries) | **PATCH** /api/v1/libraries/{id} | Library@update |
| [**fetchLibraries**](LibraryApi.md#fetchLibraries) | **GET** /api/v1/libraries/{id} | Return a single library |
| [**listLibraries**](LibraryApi.md#listLibraries) | **GET** /api/v1/libraries | Retrieve a list of libraries |
| [**updateLibraries**](LibraryApi.md#updateLibraries) | **PUT** /api/v1/libraries/{id} | Library@update |


<a id="createLibraries"></a>
# **createLibraries**
> CreateCategories200Response createLibraries(createLibrariesRequest)

Library@store

Creates a new library

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LibraryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LibraryApi apiInstance = new LibraryApi(defaultClient);
    CreateLibrariesRequest createLibrariesRequest = new CreateLibrariesRequest(); // CreateLibrariesRequest | library definition
    try {
      CreateCategories200Response result = apiInstance.createLibraries(createLibrariesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LibraryApi#createLibraries");
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
| **createLibrariesRequest** | [**CreateLibrariesRequest**](CreateLibrariesRequest.md)| library definition | |

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

<a id="deleteLibraries"></a>
# **deleteLibraries**
> DeleteAliases200Response deleteLibraries(id)

Library@destroy

Delete a library

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LibraryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LibraryApi apiInstance = new LibraryApi(defaultClient);
    Integer id = 1; // Integer | library id
    try {
      DeleteAliases200Response result = apiInstance.deleteLibraries(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LibraryApi#deleteLibraries");
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
| **id** | **Integer**| library id | |

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

<a id="editLibraries"></a>
# **editLibraries**
> UpdateLibraries200Response editLibraries(id, createLibrariesRequest)

Library@update

Edit a library

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LibraryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LibraryApi apiInstance = new LibraryApi(defaultClient);
    Integer id = 1; // Integer | library id
    CreateLibrariesRequest createLibrariesRequest = new CreateLibrariesRequest(); // CreateLibrariesRequest | library definition
    try {
      UpdateLibraries200Response result = apiInstance.editLibraries(id, createLibrariesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LibraryApi#editLibraries");
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
| **id** | **Integer**| library id | |
| **createLibrariesRequest** | [**CreateLibrariesRequest**](CreateLibrariesRequest.md)| library definition | |

### Return type

[**UpdateLibraries200Response**](UpdateLibraries200Response.md)

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

<a id="fetchLibraries"></a>
# **fetchLibraries**
> FetchLibraries200Response fetchLibraries(id)

Return a single library

Return a single library

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LibraryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LibraryApi apiInstance = new LibraryApi(defaultClient);
    Integer id = 1; // Integer | library id
    try {
      FetchLibraries200Response result = apiInstance.fetchLibraries(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LibraryApi#fetchLibraries");
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
| **id** | **Integer**| library id | |

### Return type

[**FetchLibraries200Response**](FetchLibraries200Response.md)

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

<a id="listLibraries"></a>
# **listLibraries**
> ListLibraries200Response listLibraries(perPage)

Retrieve a list of libraries

Returns a paginated list of libraries along with associated datasets and teams.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LibraryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LibraryApi apiInstance = new LibraryApi(defaultClient);
    Integer perPage = 10; // Integer | Specify the number of libraries per page
    try {
      ListLibraries200Response result = apiInstance.listLibraries(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LibraryApi#listLibraries");
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
| **perPage** | **Integer**| Specify the number of libraries per page | [optional] [default to 10] |

### Return type

[**ListLibraries200Response**](ListLibraries200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |

<a id="updateLibraries"></a>
# **updateLibraries**
> UpdateLibraries200Response updateLibraries(id, createLibrariesRequest)

Library@update

Update a library

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LibraryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LibraryApi apiInstance = new LibraryApi(defaultClient);
    Integer id = 1; // Integer | library id
    CreateLibrariesRequest createLibrariesRequest = new CreateLibrariesRequest(); // CreateLibrariesRequest | library definition
    try {
      UpdateLibraries200Response result = apiInstance.updateLibraries(id, createLibrariesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LibraryApi#updateLibraries");
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
| **id** | **Integer**| library id | |
| **createLibrariesRequest** | [**CreateLibrariesRequest**](CreateLibrariesRequest.md)| library definition | |

### Return type

[**UpdateLibraries200Response**](UpdateLibraries200Response.md)

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

