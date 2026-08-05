# ProgrammingLanguageApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProgrammingLanguages**](ProgrammingLanguageApi.md#createProgrammingLanguages) | **POST** /api/v1/programming_languages | ProgrammingLanguage@store |
| [**deleteProgrammingLanguages**](ProgrammingLanguageApi.md#deleteProgrammingLanguages) | **DELETE** /api/v1/programming_languages/{id} | ProgrammingLanguage@destroy |
| [**editProgrammingLanguages**](ProgrammingLanguageApi.md#editProgrammingLanguages) | **PATCH** /api/v1/programming_languages/{id} | ProgrammingLanguage@update |
| [**updateProgrammingLanguages**](ProgrammingLanguageApi.md#updateProgrammingLanguages) | **PUT** /api/v1/programming_languages/{id} | ProgrammingLanguage@update |


<a id="createProgrammingLanguages"></a>
# **createProgrammingLanguages**
> CreateDarIntegration201Response createProgrammingLanguages(createProgrammingLanguagesRequest)

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
    CreateProgrammingLanguagesRequest createProgrammingLanguagesRequest = new CreateProgrammingLanguagesRequest(); // CreateProgrammingLanguagesRequest | Programming language definition
    try {
      CreateDarIntegration201Response result = apiInstance.createProgrammingLanguages(createProgrammingLanguagesRequest);
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
| **createProgrammingLanguagesRequest** | [**CreateProgrammingLanguagesRequest**](CreateProgrammingLanguagesRequest.md)| Programming language definition | |

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

<a id="deleteProgrammingLanguages"></a>
# **deleteProgrammingLanguages**
> DeleteApplications200Response deleteProgrammingLanguages(id)

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
      DeleteApplications200Response result = apiInstance.deleteProgrammingLanguages(id);
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

<a id="editProgrammingLanguages"></a>
# **editProgrammingLanguages**
> UpdateProgrammingLanguages200Response editProgrammingLanguages(id, editProgrammingLanguagesRequest)

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
    EditProgrammingLanguagesRequest editProgrammingLanguagesRequest = new EditProgrammingLanguagesRequest(); // EditProgrammingLanguagesRequest | ProgrammingLanguage definition
    try {
      UpdateProgrammingLanguages200Response result = apiInstance.editProgrammingLanguages(id, editProgrammingLanguagesRequest);
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
| **editProgrammingLanguagesRequest** | [**EditProgrammingLanguagesRequest**](EditProgrammingLanguagesRequest.md)| ProgrammingLanguage definition | |

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

<a id="updateProgrammingLanguages"></a>
# **updateProgrammingLanguages**
> UpdateProgrammingLanguages200Response updateProgrammingLanguages(id, updateProgrammingLanguagesRequest)

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
    UpdateProgrammingLanguagesRequest updateProgrammingLanguagesRequest = new UpdateProgrammingLanguagesRequest(); // UpdateProgrammingLanguagesRequest | ProgrammingLanguage definition
    try {
      UpdateProgrammingLanguages200Response result = apiInstance.updateProgrammingLanguages(id, updateProgrammingLanguagesRequest);
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
| **updateProgrammingLanguagesRequest** | [**UpdateProgrammingLanguagesRequest**](UpdateProgrammingLanguagesRequest.md)| ProgrammingLanguage definition | |

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

