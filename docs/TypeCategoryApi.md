# TypeCategoryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTypeCategories**](TypeCategoryApi.md#createTypeCategories) | **POST** /api/v1/type_categories | TypeCategory@store |
| [**deleteTypeCategories**](TypeCategoryApi.md#deleteTypeCategories) | **DELETE** /api/v1/type_categories/{id} | TypeCategory@destroy |
| [**editTypeCategories**](TypeCategoryApi.md#editTypeCategories) | **PATCH** /api/v1/type_categories/{id} | TypeCategory@update |
| [**fetchAllTypeCategories**](TypeCategoryApi.md#fetchAllTypeCategories) | **GET** /api/v1/type_categories | TypeCategory@index |
| [**fetchTypeCategories**](TypeCategoryApi.md#fetchTypeCategories) | **GET** /api/v1/type_categories/{id} | TypeCategory@show |
| [**updateTypeCategories**](TypeCategoryApi.md#updateTypeCategories) | **PUT** /api/v1/type_categories/{id} | TypeCategory@update |


<a id="createTypeCategories"></a>
# **createTypeCategories**
> CreateCategories200Response createTypeCategories(createTypeCategoriesRequest)

TypeCategory@store

Creates a new system type category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TypeCategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TypeCategoryApi apiInstance = new TypeCategoryApi(defaultClient);
    CreateTypeCategoriesRequest createTypeCategoriesRequest = new CreateTypeCategoriesRequest(); // CreateTypeCategoriesRequest | Programming language definition
    try {
      CreateCategories200Response result = apiInstance.createTypeCategories(createTypeCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TypeCategoryApi#createTypeCategories");
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
| **createTypeCategoriesRequest** | [**CreateTypeCategoriesRequest**](CreateTypeCategoriesRequest.md)| Programming language definition | |

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

<a id="deleteTypeCategories"></a>
# **deleteTypeCategories**
> DeleteAliases200Response deleteTypeCategories(id)

TypeCategory@destroy

Delete a system type category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TypeCategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TypeCategoryApi apiInstance = new TypeCategoryApi(defaultClient);
    Integer id = 1; // Integer | type category id
    try {
      DeleteAliases200Response result = apiInstance.deleteTypeCategories(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TypeCategoryApi#deleteTypeCategories");
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
| **id** | **Integer**| type category id | |

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

<a id="editTypeCategories"></a>
# **editTypeCategories**
> UpdateTypeCategories200Response editTypeCategories(id, editCategoriesRequest)

TypeCategory@update

Edit a system type category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TypeCategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TypeCategoryApi apiInstance = new TypeCategoryApi(defaultClient);
    Integer id = 1; // Integer | type category id
    EditCategoriesRequest editCategoriesRequest = new EditCategoriesRequest(); // EditCategoriesRequest | TypeCategory definition
    try {
      UpdateTypeCategories200Response result = apiInstance.editTypeCategories(id, editCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TypeCategoryApi#editTypeCategories");
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
| **id** | **Integer**| type category id | |
| **editCategoriesRequest** | [**EditCategoriesRequest**](EditCategoriesRequest.md)| TypeCategory definition | |

### Return type

[**UpdateTypeCategories200Response**](UpdateTypeCategories200Response.md)

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

<a id="fetchAllTypeCategories"></a>
# **fetchAllTypeCategories**
> FetchAllTypeCategories200Response fetchAllTypeCategories()

TypeCategory@index

Returns a list of type categories enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TypeCategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TypeCategoryApi apiInstance = new TypeCategoryApi(defaultClient);
    try {
      FetchAllTypeCategories200Response result = apiInstance.fetchAllTypeCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TypeCategoryApi#fetchAllTypeCategories");
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

[**FetchAllTypeCategories200Response**](FetchAllTypeCategories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchTypeCategories"></a>
# **fetchTypeCategories**
> FetchTypeCategories200Response fetchTypeCategories(id)

TypeCategory@show

Return a single system type category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TypeCategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TypeCategoryApi apiInstance = new TypeCategoryApi(defaultClient);
    Integer id = 1; // Integer | type category id
    try {
      FetchTypeCategories200Response result = apiInstance.fetchTypeCategories(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TypeCategoryApi#fetchTypeCategories");
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
| **id** | **Integer**| type category id | |

### Return type

[**FetchTypeCategories200Response**](FetchTypeCategories200Response.md)

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

<a id="updateTypeCategories"></a>
# **updateTypeCategories**
> UpdateTypeCategories200Response updateTypeCategories(id, updateTypeCategoriesRequest)

TypeCategory@update

Update a system type category

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TypeCategoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TypeCategoryApi apiInstance = new TypeCategoryApi(defaultClient);
    Integer id = 1; // Integer | type category id
    UpdateTypeCategoriesRequest updateTypeCategoriesRequest = new UpdateTypeCategoriesRequest(); // UpdateTypeCategoriesRequest | TypeCategory definition
    try {
      UpdateTypeCategories200Response result = apiInstance.updateTypeCategories(id, updateTypeCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TypeCategoryApi#updateTypeCategories");
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
| **id** | **Integer**| type category id | |
| **updateTypeCategoriesRequest** | [**UpdateTypeCategoriesRequest**](UpdateTypeCategoriesRequest.md)| TypeCategory definition | |

### Return type

[**UpdateTypeCategories200Response**](UpdateTypeCategories200Response.md)

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

