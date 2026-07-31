# AliasApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAliases**](AliasApi.md#createAliases) | **POST** /api/v1/aliases | AliasController@store |
| [**deleteAliases**](AliasApi.md#deleteAliases) | **DELETE** /api/v1/aliases/{id} | AliasController@destroy |
| [**editAliases**](AliasApi.md#editAliases) | **PATCH** /api/v1/aliases/{id} | AliasController@edit |
| [**fetchAliases**](AliasApi.md#fetchAliases) | **GET** /api/v1/aliases/{id} | Return a single alias |
| [**fetchAllAliases**](AliasApi.md#fetchAllAliases) | **GET** /api/v1/aliases | List of aliases |
| [**updateAliases**](AliasApi.md#updateAliases) | **PUT** /api/v1/aliases/{id} | AliasController@update |


<a id="createAliases"></a>
# **createAliases**
> CreateAliases200Response createAliases(createAliasesRequest)

AliasController@store

Creates a new alias

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AliasApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AliasApi apiInstance = new AliasApi(defaultClient);
    CreateAliasesRequest createAliasesRequest = new CreateAliasesRequest(); // CreateAliasesRequest | Alias definition
    try {
      CreateAliases200Response result = apiInstance.createAliases(createAliasesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliasApi#createAliases");
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
| **createAliasesRequest** | [**CreateAliasesRequest**](CreateAliasesRequest.md)| Alias definition | |

### Return type

[**CreateAliases200Response**](CreateAliases200Response.md)

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

<a id="deleteAliases"></a>
# **deleteAliases**
> DeleteAliases200Response deleteAliases(id)

AliasController@destroy

Delete an alias

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AliasApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AliasApi apiInstance = new AliasApi(defaultClient);
    Integer id = 1; // Integer | alias id
    try {
      DeleteAliases200Response result = apiInstance.deleteAliases(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliasApi#deleteAliases");
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
| **id** | **Integer**| alias id | |

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

<a id="editAliases"></a>
# **editAliases**
> UpdateAliases200Response editAliases(id, editAliasesRequest)

AliasController@edit

Edit a alias

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AliasApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AliasApi apiInstance = new AliasApi(defaultClient);
    Integer id = 1; // Integer | alias id
    EditAliasesRequest editAliasesRequest = new EditAliasesRequest(); // EditAliasesRequest | Alias definition
    try {
      UpdateAliases200Response result = apiInstance.editAliases(id, editAliasesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliasApi#editAliases");
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
| **id** | **Integer**| alias id | |
| **editAliasesRequest** | [**EditAliasesRequest**](EditAliasesRequest.md)| Alias definition | |

### Return type

[**UpdateAliases200Response**](UpdateAliases200Response.md)

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

<a id="fetchAliases"></a>
# **fetchAliases**
> FetchAliases200Response fetchAliases(id)

Return a single alias

Return a single alias

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AliasApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AliasApi apiInstance = new AliasApi(defaultClient);
    Integer id = 1; // Integer | alias id
    try {
      FetchAliases200Response result = apiInstance.fetchAliases(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliasApi#fetchAliases");
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
| **id** | **Integer**| alias id | |

### Return type

[**FetchAliases200Response**](FetchAliases200Response.md)

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

<a id="fetchAllAliases"></a>
# **fetchAllAliases**
> FetchAllAliases200Response fetchAllAliases()

List of aliases

Returns a list of aliases

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AliasApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AliasApi apiInstance = new AliasApi(defaultClient);
    try {
      FetchAllAliases200Response result = apiInstance.fetchAllAliases();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliasApi#fetchAllAliases");
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

[**FetchAllAliases200Response**](FetchAllAliases200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="updateAliases"></a>
# **updateAliases**
> UpdateAliases200Response updateAliases(id, createAliasesRequest)

AliasController@update

Update a alias

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AliasApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AliasApi apiInstance = new AliasApi(defaultClient);
    Integer id = 1; // Integer | alias id
    CreateAliasesRequest createAliasesRequest = new CreateAliasesRequest(); // CreateAliasesRequest | Alias definition
    try {
      UpdateAliases200Response result = apiInstance.updateAliases(id, createAliasesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliasApi#updateAliases");
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
| **id** | **Integer**| alias id | |
| **createAliasesRequest** | [**CreateAliasesRequest**](CreateAliasesRequest.md)| Alias definition | |

### Return type

[**UpdateAliases200Response**](UpdateAliases200Response.md)

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

