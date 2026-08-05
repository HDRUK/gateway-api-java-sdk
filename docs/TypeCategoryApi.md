# TypeCategoryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTypeCategories**](TypeCategoryApi.md#createTypeCategories) | **POST** /api/v1/type_categories | TypeCategory@store |
| [**deleteTypeCategories**](TypeCategoryApi.md#deleteTypeCategories) | **DELETE** /api/v1/type_categories/{id} | TypeCategory@destroy |
| [**editTypeCategories**](TypeCategoryApi.md#editTypeCategories) | **PATCH** /api/v1/type_categories/{id} | TypeCategory@update |
| [**updateTypeCategories**](TypeCategoryApi.md#updateTypeCategories) | **PUT** /api/v1/type_categories/{id} | TypeCategory@update |


<a id="createTypeCategories"></a>
# **createTypeCategories**
> CreateDarIntegration201Response createTypeCategories(createTypeCategoriesRequest)

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
      CreateDarIntegration201Response result = apiInstance.createTypeCategories(createTypeCategoriesRequest);
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

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

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
> DeleteApplications200Response deleteTypeCategories(id)

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
      DeleteApplications200Response result = apiInstance.deleteTypeCategories(id);
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

<a id="editTypeCategories"></a>
# **editTypeCategories**
> UpdateTypeCategories200Response editTypeCategories(id, editProgrammingLanguagesRequest)

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
    EditProgrammingLanguagesRequest editProgrammingLanguagesRequest = new EditProgrammingLanguagesRequest(); // EditProgrammingLanguagesRequest | TypeCategory definition
    try {
      UpdateTypeCategories200Response result = apiInstance.editTypeCategories(id, editProgrammingLanguagesRequest);
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
| **editProgrammingLanguagesRequest** | [**EditProgrammingLanguagesRequest**](EditProgrammingLanguagesRequest.md)| TypeCategory definition | |

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

