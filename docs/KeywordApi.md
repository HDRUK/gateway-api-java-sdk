# KeywordApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createKeywords**](KeywordApi.md#createKeywords) | **POST** /api/v1/keywords | KeywordController@store |
| [**deleteKeywords**](KeywordApi.md#deleteKeywords) | **DELETE** /api/v1/keywords/{id} | KeywordController@destroy |
| [**editKeywords**](KeywordApi.md#editKeywords) | **PATCH** /api/v1/keywords/{id} | KeywordController@update |
| [**fetchAllKeywords**](KeywordApi.md#fetchAllKeywords) | **GET** /api/v1/keywords | KeywordController@index |
| [**fetchKeywords**](KeywordApi.md#fetchKeywords) | **GET** /api/v1/keywords/{id} | KeywordController@show |
| [**updateKeywords**](KeywordApi.md#updateKeywords) | **PUT** /api/v1/keywords/{id} | KeywordController@update |


<a id="createKeywords"></a>
# **createKeywords**
> CreateCategories200Response createKeywords(createCategoriesRequest)

KeywordController@store

Creates a new keyword

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.KeywordApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    KeywordApi apiInstance = new KeywordApi(defaultClient);
    CreateCategoriesRequest createCategoriesRequest = new CreateCategoriesRequest(); // CreateCategoriesRequest | Keyword definition
    try {
      CreateCategories200Response result = apiInstance.createKeywords(createCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling KeywordApi#createKeywords");
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
| **createCategoriesRequest** | [**CreateCategoriesRequest**](CreateCategoriesRequest.md)| Keyword definition | |

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
| **409** | Error |  -  |

<a id="deleteKeywords"></a>
# **deleteKeywords**
> DeleteAliases200Response deleteKeywords(id)

KeywordController@destroy

Delete a keyword by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.KeywordApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    KeywordApi apiInstance = new KeywordApi(defaultClient);
    Integer id = 1; // Integer | keyword id
    try {
      DeleteAliases200Response result = apiInstance.deleteKeywords(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling KeywordApi#deleteKeywords");
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
| **id** | **Integer**| keyword id | |

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

<a id="editKeywords"></a>
# **editKeywords**
> UpdateKeywords200Response editKeywords(id, editCategoriesRequest)

KeywordController@update

Edit a keyword by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.KeywordApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    KeywordApi apiInstance = new KeywordApi(defaultClient);
    Integer id = 1; // Integer | keyword id
    EditCategoriesRequest editCategoriesRequest = new EditCategoriesRequest(); // EditCategoriesRequest | Category definition
    try {
      UpdateKeywords200Response result = apiInstance.editKeywords(id, editCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling KeywordApi#editKeywords");
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
| **id** | **Integer**| keyword id | |
| **editCategoriesRequest** | [**EditCategoriesRequest**](EditCategoriesRequest.md)| Category definition | |

### Return type

[**UpdateKeywords200Response**](UpdateKeywords200Response.md)

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

<a id="fetchAllKeywords"></a>
# **fetchAllKeywords**
> FetchAllKeywords200Response fetchAllKeywords(perPage)

KeywordController@index

Returns a list of keywords

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.KeywordApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    KeywordApi apiInstance = new KeywordApi(defaultClient);
    Integer perPage = 56; // Integer | Alternative output schema version.
    try {
      FetchAllKeywords200Response result = apiInstance.fetchAllKeywords(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling KeywordApi#fetchAllKeywords");
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
| **perPage** | **Integer**| Alternative output schema version. | [optional] |

### Return type

[**FetchAllKeywords200Response**](FetchAllKeywords200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchKeywords"></a>
# **fetchKeywords**
> FetchKeywords200Response fetchKeywords(id)

KeywordController@show

Return a single keyword

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.KeywordApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    KeywordApi apiInstance = new KeywordApi(defaultClient);
    Integer id = 1; // Integer | keyword id
    try {
      FetchKeywords200Response result = apiInstance.fetchKeywords(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling KeywordApi#fetchKeywords");
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
| **id** | **Integer**| keyword id | |

### Return type

[**FetchKeywords200Response**](FetchKeywords200Response.md)

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

<a id="updateKeywords"></a>
# **updateKeywords**
> UpdateKeywords200Response updateKeywords(id, updateCategoriesRequest)

KeywordController@update

Update a keyword by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.KeywordApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    KeywordApi apiInstance = new KeywordApi(defaultClient);
    Integer id = 1; // Integer | keyword id
    UpdateCategoriesRequest updateCategoriesRequest = new UpdateCategoriesRequest(); // UpdateCategoriesRequest | Keyword definition
    try {
      UpdateKeywords200Response result = apiInstance.updateKeywords(id, updateCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling KeywordApi#updateKeywords");
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
| **id** | **Integer**| keyword id | |
| **updateCategoriesRequest** | [**UpdateCategoriesRequest**](UpdateCategoriesRequest.md)| Keyword definition | |

### Return type

[**UpdateKeywords200Response**](UpdateKeywords200Response.md)

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

