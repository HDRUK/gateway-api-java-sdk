# ProgrammingPackageApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProgrammingPackages**](ProgrammingPackageApi.md#createProgrammingPackages) | **POST** /api/v1/programming_packages | ProgrammingPackage@store |
| [**deleteProgrammingPackages**](ProgrammingPackageApi.md#deleteProgrammingPackages) | **DELETE** /api/v1/programming_packages/{id} | ProgrammingPackage@destroy |
| [**editProgrammingPackages**](ProgrammingPackageApi.md#editProgrammingPackages) | **PATCH** /api/v1/programming_packages/{id} | ProgrammingPackage@update |
| [**updateProgrammingPackages**](ProgrammingPackageApi.md#updateProgrammingPackages) | **PUT** /api/v1/programming_packages/{id} | ProgrammingPackage@update |


<a id="createProgrammingPackages"></a>
# **createProgrammingPackages**
> CreateDarIntegration201Response createProgrammingPackages(createProgrammingLanguagesRequest)

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
    CreateProgrammingLanguagesRequest createProgrammingLanguagesRequest = new CreateProgrammingLanguagesRequest(); // CreateProgrammingLanguagesRequest | Programming package definition
    try {
      CreateDarIntegration201Response result = apiInstance.createProgrammingPackages(createProgrammingLanguagesRequest);
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
| **createProgrammingLanguagesRequest** | [**CreateProgrammingLanguagesRequest**](CreateProgrammingLanguagesRequest.md)| Programming package definition | |

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

<a id="deleteProgrammingPackages"></a>
# **deleteProgrammingPackages**
> DeleteApplications200Response deleteProgrammingPackages(id)

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
      DeleteApplications200Response result = apiInstance.deleteProgrammingPackages(id);
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

<a id="editProgrammingPackages"></a>
# **editProgrammingPackages**
> UpdateProgrammingPackages200Response editProgrammingPackages(id, editProgrammingLanguagesRequest)

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
    EditProgrammingLanguagesRequest editProgrammingLanguagesRequest = new EditProgrammingLanguagesRequest(); // EditProgrammingLanguagesRequest | ProgrammingPackage definition
    try {
      UpdateProgrammingPackages200Response result = apiInstance.editProgrammingPackages(id, editProgrammingLanguagesRequest);
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
| **editProgrammingLanguagesRequest** | [**EditProgrammingLanguagesRequest**](EditProgrammingLanguagesRequest.md)| ProgrammingPackage definition | |

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

<a id="updateProgrammingPackages"></a>
# **updateProgrammingPackages**
> UpdateProgrammingPackages200Response updateProgrammingPackages(id, updateProgrammingLanguagesRequest)

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
    UpdateProgrammingLanguagesRequest updateProgrammingLanguagesRequest = new UpdateProgrammingLanguagesRequest(); // UpdateProgrammingLanguagesRequest | ProgrammingPackage definition
    try {
      UpdateProgrammingPackages200Response result = apiInstance.updateProgrammingPackages(id, updateProgrammingLanguagesRequest);
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
| **updateProgrammingLanguagesRequest** | [**UpdateProgrammingLanguagesRequest**](UpdateProgrammingLanguagesRequest.md)| ProgrammingPackage definition | |

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

