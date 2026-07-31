# ProgrammingLanguageApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProgrammingLanguages**](ProgrammingLanguageApi.md#createProgrammingLanguages) | **POST** /api/v1/programming_languages | ProgrammingLanguage@store |
| [**deleteProgrammingLanguages**](ProgrammingLanguageApi.md#deleteProgrammingLanguages) | **DELETE** /api/v1/programming_languages/{id} | ProgrammingLanguage@destroy |
| [**editProgrammingLanguages**](ProgrammingLanguageApi.md#editProgrammingLanguages) | **PATCH** /api/v1/programming_languages/{id} | ProgrammingLanguage@update |
| [**fetchAllProgrammingLanguages**](ProgrammingLanguageApi.md#fetchAllProgrammingLanguages) | **GET** /api/v1/programming_languages | ProgrammingLanguage@index |
| [**fetchProgrammingLanguages**](ProgrammingLanguageApi.md#fetchProgrammingLanguages) | **GET** /api/v1/programming_languages/{id} | ProgrammingLanguage@show |
| [**updateProgrammingLanguages**](ProgrammingLanguageApi.md#updateProgrammingLanguages) | **PUT** /api/v1/programming_languages/{id} | ProgrammingLanguage@update |


<a id="createProgrammingLanguages"></a>
# **createProgrammingLanguages**
> CreateCategories200Response createProgrammingLanguages(createCategoriesRequest)

ProgrammingLanguage@store

Creates a new system programming language

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingLanguageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingLanguageApi apiInstance = new ProgrammingLanguageApi(defaultClient);
    CreateCategoriesRequest createCategoriesRequest = new CreateCategoriesRequest(); // CreateCategoriesRequest | Programming language definition
    try {
      CreateCategories200Response result = apiInstance.createProgrammingLanguages(createCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingLanguageApi#createProgrammingLanguages");
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
| **createCategoriesRequest** | [**CreateCategoriesRequest**](CreateCategoriesRequest.md)| Programming language definition | |

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

<a id="deleteProgrammingLanguages"></a>
# **deleteProgrammingLanguages**
> DeleteAliases200Response deleteProgrammingLanguages(id)

ProgrammingLanguage@destroy

Delete a system programming language

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingLanguageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingLanguageApi apiInstance = new ProgrammingLanguageApi(defaultClient);
    Integer id = 1; // Integer | programming language id
    try {
      DeleteAliases200Response result = apiInstance.deleteProgrammingLanguages(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingLanguageApi#deleteProgrammingLanguages");
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
| **id** | **Integer**| programming language id | |

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

<a id="editProgrammingLanguages"></a>
# **editProgrammingLanguages**
> UpdateProgrammingLanguages200Response editProgrammingLanguages(id, editCategoriesRequest)

ProgrammingLanguage@update

Edit a system programming language

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingLanguageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingLanguageApi apiInstance = new ProgrammingLanguageApi(defaultClient);
    Integer id = 1; // Integer | programming language id
    EditCategoriesRequest editCategoriesRequest = new EditCategoriesRequest(); // EditCategoriesRequest | ProgrammingLanguage definition
    try {
      UpdateProgrammingLanguages200Response result = apiInstance.editProgrammingLanguages(id, editCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingLanguageApi#editProgrammingLanguages");
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
| **id** | **Integer**| programming language id | |
| **editCategoriesRequest** | [**EditCategoriesRequest**](EditCategoriesRequest.md)| ProgrammingLanguage definition | |

### Return type

[**UpdateProgrammingLanguages200Response**](UpdateProgrammingLanguages200Response.md)

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

<a id="fetchAllProgrammingLanguages"></a>
# **fetchAllProgrammingLanguages**
> FetchAllProgrammingLanguages200Response fetchAllProgrammingLanguages()

ProgrammingLanguage@index

Returns a list of programming languages enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingLanguageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingLanguageApi apiInstance = new ProgrammingLanguageApi(defaultClient);
    try {
      FetchAllProgrammingLanguages200Response result = apiInstance.fetchAllProgrammingLanguages();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingLanguageApi#fetchAllProgrammingLanguages");
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

[**FetchAllProgrammingLanguages200Response**](FetchAllProgrammingLanguages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchProgrammingLanguages"></a>
# **fetchProgrammingLanguages**
> FetchProgrammingLanguages200Response fetchProgrammingLanguages(id)

ProgrammingLanguage@show

Return a single system programming language

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingLanguageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingLanguageApi apiInstance = new ProgrammingLanguageApi(defaultClient);
    Integer id = 1; // Integer | programming language id
    try {
      FetchProgrammingLanguages200Response result = apiInstance.fetchProgrammingLanguages(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingLanguageApi#fetchProgrammingLanguages");
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
| **id** | **Integer**| programming language id | |

### Return type

[**FetchProgrammingLanguages200Response**](FetchProgrammingLanguages200Response.md)

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

<a id="updateProgrammingLanguages"></a>
# **updateProgrammingLanguages**
> UpdateProgrammingLanguages200Response updateProgrammingLanguages(id, updateCategoriesRequest)

ProgrammingLanguage@update

Update a system programming language

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProgrammingLanguageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProgrammingLanguageApi apiInstance = new ProgrammingLanguageApi(defaultClient);
    Integer id = 1; // Integer | programming language id
    UpdateCategoriesRequest updateCategoriesRequest = new UpdateCategoriesRequest(); // UpdateCategoriesRequest | ProgrammingLanguage definition
    try {
      UpdateProgrammingLanguages200Response result = apiInstance.updateProgrammingLanguages(id, updateCategoriesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgrammingLanguageApi#updateProgrammingLanguages");
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
| **id** | **Integer**| programming language id | |
| **updateCategoriesRequest** | [**UpdateCategoriesRequest**](UpdateCategoriesRequest.md)| ProgrammingLanguage definition | |

### Return type

[**UpdateProgrammingLanguages200Response**](UpdateProgrammingLanguages200Response.md)

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

