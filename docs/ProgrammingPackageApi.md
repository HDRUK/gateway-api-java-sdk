# ProgrammingPackageApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProgrammingPackages**](ProgrammingPackageApi.md#createProgrammingPackages) | **POST** /api/v1/programming_packages | ProgrammingPackage@store |
| [**deleteProgrammingPackages**](ProgrammingPackageApi.md#deleteProgrammingPackages) | **DELETE** /api/v1/programming_packages/{id} | ProgrammingPackage@destroy |
| [**editProgrammingPackages**](ProgrammingPackageApi.md#editProgrammingPackages) | **PATCH** /api/v1/programming_packages/{id} | ProgrammingPackage@update |
| [**fetchAllProgrammingPackages**](ProgrammingPackageApi.md#fetchAllProgrammingPackages) | **GET** /api/v1/programming_packages | ProgrammingPackage@index |
| [**fetchProgrammingPackages**](ProgrammingPackageApi.md#fetchProgrammingPackages) | **GET** /api/v1/programming_packages/{id} | ProgrammingPackage@show |
| [**updateProgrammingPackages**](ProgrammingPackageApi.md#updateProgrammingPackages) | **PUT** /api/v1/programming_packages/{id} | ProgrammingPackage@update |


<a id="createProgrammingPackages"></a>
# **createProgrammingPackages**
> CreateCategories200Response createProgrammingPackages(createCategoriesRequest)

ProgrammingPackage@store

Creates a new system programming package

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingPackageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingPackageApi apiInstance = new ProgrammingPackageApi(defaultClient);
    CreateCategoriesRequest createCategoriesRequest = new CreateCategoriesRequest(); // CreateCategoriesRequest | Programming package definition
    try {
      CreateCategories200Response result = apiInstance.createProgrammingPackages(createCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingPackageApi#createProgrammingPackages");
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
| **createCategoriesRequest** | [**CreateCategoriesRequest**](CreateCategoriesRequest.md)| Programming package definition | |

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

<a id="deleteProgrammingPackages"></a>
# **deleteProgrammingPackages**
> DeleteAliases200Response deleteProgrammingPackages(id)

ProgrammingPackage@destroy

Delete a system programming package

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingPackageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingPackageApi apiInstance = new ProgrammingPackageApi(defaultClient);
    Integer id = 1; // Integer | programming package id
    try {
      DeleteAliases200Response result = apiInstance.deleteProgrammingPackages(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingPackageApi#deleteProgrammingPackages");
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
| **id** | **Integer**| programming package id | |

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

<a id="editProgrammingPackages"></a>
# **editProgrammingPackages**
> UpdateProgrammingPackages200Response editProgrammingPackages(id, editCategoriesRequest)

ProgrammingPackage@update

Edit a system programming package

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingPackageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingPackageApi apiInstance = new ProgrammingPackageApi(defaultClient);
    Integer id = 1; // Integer | programming package id
    EditCategoriesRequest editCategoriesRequest = new EditCategoriesRequest(); // EditCategoriesRequest | ProgrammingPackage definition
    try {
      UpdateProgrammingPackages200Response result = apiInstance.editProgrammingPackages(id, editCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingPackageApi#editProgrammingPackages");
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
| **id** | **Integer**| programming package id | |
| **editCategoriesRequest** | [**EditCategoriesRequest**](EditCategoriesRequest.md)| ProgrammingPackage definition | |

### Return type

[**UpdateProgrammingPackages200Response**](UpdateProgrammingPackages200Response.md)

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

<a id="fetchAllProgrammingPackages"></a>
# **fetchAllProgrammingPackages**
> FetchAllProgrammingPackages200Response fetchAllProgrammingPackages()

ProgrammingPackage@index

Returns a list of programming packages enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingPackageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingPackageApi apiInstance = new ProgrammingPackageApi(defaultClient);
    try {
      FetchAllProgrammingPackages200Response result = apiInstance.fetchAllProgrammingPackages();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingPackageApi#fetchAllProgrammingPackages");
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

[**FetchAllProgrammingPackages200Response**](FetchAllProgrammingPackages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchProgrammingPackages"></a>
# **fetchProgrammingPackages**
> FetchProgrammingPackages200Response fetchProgrammingPackages(id)

ProgrammingPackage@show

Return a single system programming package

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingPackageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingPackageApi apiInstance = new ProgrammingPackageApi(defaultClient);
    Integer id = 1; // Integer | programming package id
    try {
      FetchProgrammingPackages200Response result = apiInstance.fetchProgrammingPackages(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingPackageApi#fetchProgrammingPackages");
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
| **id** | **Integer**| programming package id | |

### Return type

[**FetchProgrammingPackages200Response**](FetchProgrammingPackages200Response.md)

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

<a id="updateProgrammingPackages"></a>
# **updateProgrammingPackages**
> UpdateProgrammingPackages200Response updateProgrammingPackages(id, updateCategoriesRequest)

ProgrammingPackage@update

Update a system programming package

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingPackageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingPackageApi apiInstance = new ProgrammingPackageApi(defaultClient);
    Integer id = 1; // Integer | programming package id
    UpdateCategoriesRequest updateCategoriesRequest = new UpdateCategoriesRequest(); // UpdateCategoriesRequest | ProgrammingPackage definition
    try {
      UpdateProgrammingPackages200Response result = apiInstance.updateProgrammingPackages(id, updateCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingPackageApi#updateProgrammingPackages");
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
| **id** | **Integer**| programming package id | |
| **updateCategoriesRequest** | [**UpdateCategoriesRequest**](UpdateCategoriesRequest.md)| ProgrammingPackage definition | |

### Return type

[**UpdateProgrammingPackages200Response**](UpdateProgrammingPackages200Response.md)

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

