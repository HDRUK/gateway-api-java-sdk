# CategoryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCategories**](CategoryApi.md#createCategories) | **POST** /api/v1/categories | Category@store |
| [**deleteCategories**](CategoryApi.md#deleteCategories) | **DELETE** /api/v1/categories/{id} | Category@destroy |
| [**editCategories**](CategoryApi.md#editCategories) | **PATCH** /api/v1/categories/{id} | Category@update |
| [**fetchAllCategories**](CategoryApi.md#fetchAllCategories) | **GET** /api/v1/categories | Category@index |
| [**fetchCategories**](CategoryApi.md#fetchCategories) | **GET** /api/v1/categories/{id} | Category@show |
| [**updateCategories**](CategoryApi.md#updateCategories) | **PUT** /api/v1/categories/{id} | Category@update |


<a id="createCategories"></a>
# **createCategories**
> CreateCategories200Response createCategories(createCategoriesRequest)

Category@store

Creates a new tool category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CategoryApi apiInstance = new CategoryApi(defaultClient);
    CreateCategoriesRequest createCategoriesRequest = new CreateCategoriesRequest(); // CreateCategoriesRequest | Category definition
    try {
      CreateCategories200Response result = apiInstance.createCategories(createCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CategoryApi#createCategories");
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
| **createCategoriesRequest** | [**CreateCategoriesRequest**](CreateCategoriesRequest.md)| Category definition | |

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

<a id="deleteCategories"></a>
# **deleteCategories**
> DeleteAliases200Response deleteCategories(id)

Category@destroy

Delete a tool category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CategoryApi apiInstance = new CategoryApi(defaultClient);
    Integer id = 1; // Integer | category id
    try {
      DeleteAliases200Response result = apiInstance.deleteCategories(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CategoryApi#deleteCategories");
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
| **id** | **Integer**| category id | |

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

<a id="editCategories"></a>
# **editCategories**
> UpdateCategories200Response editCategories(id, editCategoriesRequest)

Category@update

Edit a tool category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CategoryApi apiInstance = new CategoryApi(defaultClient);
    Integer id = 1; // Integer | category id
    EditCategoriesRequest editCategoriesRequest = new EditCategoriesRequest(); // EditCategoriesRequest | Category definition
    try {
      UpdateCategories200Response result = apiInstance.editCategories(id, editCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CategoryApi#editCategories");
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
| **id** | **Integer**| category id | |
| **editCategoriesRequest** | [**EditCategoriesRequest**](EditCategoriesRequest.md)| Category definition | |

### Return type

[**UpdateCategories200Response**](UpdateCategories200Response.md)

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

<a id="fetchAllCategories"></a>
# **fetchAllCategories**
> FetchAllCategories200Response fetchAllCategories(perPage)

Category@index

Returns a list of categories enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CategoryApi apiInstance = new CategoryApi(defaultClient);
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllCategories200Response result = apiInstance.fetchAllCategories(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CategoryApi#fetchAllCategories");
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

[**FetchAllCategories200Response**](FetchAllCategories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchCategories"></a>
# **fetchCategories**
> FetchAllCategories200Response fetchCategories(id)

Category@show

Return a single tool category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CategoryApi apiInstance = new CategoryApi(defaultClient);
    Integer id = 1; // Integer | category id
    try {
      FetchAllCategories200Response result = apiInstance.fetchCategories(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CategoryApi#fetchCategories");
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
| **id** | **Integer**| category id | |

### Return type

[**FetchAllCategories200Response**](FetchAllCategories200Response.md)

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

<a id="updateCategories"></a>
# **updateCategories**
> UpdateCategories200Response updateCategories(id, updateCategoriesRequest)

Category@update

Update a tool category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CategoryApi apiInstance = new CategoryApi(defaultClient);
    Integer id = 1; // Integer | category id
    UpdateCategoriesRequest updateCategoriesRequest = new UpdateCategoriesRequest(); // UpdateCategoriesRequest | Category definition
    try {
      UpdateCategories200Response result = apiInstance.updateCategories(id, updateCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CategoryApi#updateCategories");
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
| **id** | **Integer**| category id | |
| **updateCategoriesRequest** | [**UpdateCategoriesRequest**](UpdateCategoriesRequest.md)| Category definition | |

### Return type

[**UpdateCategories200Response**](UpdateCategories200Response.md)

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

