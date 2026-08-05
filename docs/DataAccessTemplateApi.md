# DataAccessTemplateApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDarTemplate**](DataAccessTemplateApi.md#createDarTemplate) | **POST** /api/v1/dar/templates | DataAccessTemplate@store |
| [**deleteDarTemplate**](DataAccessTemplateApi.md#deleteDarTemplate) | **DELETE** /api/v1/dar/templates/{id} | DataAccessTemplate@destroy |
| [**fetchDarTemplate**](DataAccessTemplateApi.md#fetchDarTemplate) | **GET** /api/v1/dar/templates/{id} | DataAccessTemplate@show |
| [**fetchDarTemplates**](DataAccessTemplateApi.md#fetchDarTemplates) | **GET** /api/v1/dar/templates | DataAccessTemplate@index |
| [**patchDarTemplate**](DataAccessTemplateApi.md#patchDarTemplate) | **PATCH** /api/v1/dar/templates/{id} | DataAccessTemplate@update |
| [**updateDarTemplate**](DataAccessTemplateApi.md#updateDarTemplate) | **PUT** /api/v1/dar/templates/{id} | DataAccessTemplate@update |


<a id="createDarTemplate"></a>
# **createDarTemplate**
> CreateDarIntegration201Response createDarTemplate(createDarTemplateRequest)

DataAccessTemplate@store

Creates a new DAR template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplateApi apiInstance = new DataAccessTemplateApi(defaultClient);
    CreateDarTemplateRequest createDarTemplateRequest = new CreateDarTemplateRequest(); // CreateDarTemplateRequest | DataAccessTemplate definition
    try {
      CreateDarIntegration201Response result = apiInstance.createDarTemplate(createDarTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplateApi#createDarTemplate");
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
| **createDarTemplateRequest** | [**CreateDarTemplateRequest**](CreateDarTemplateRequest.md)| DataAccessTemplate definition | |

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

<a id="deleteDarTemplate"></a>
# **deleteDarTemplate**
> DeleteApplications200Response deleteDarTemplate(id)

DataAccessTemplate@destroy

Delete a system DAR template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplateApi apiInstance = new DataAccessTemplateApi(defaultClient);
    Integer id = 1; // Integer | DAR template id
    try {
      DeleteApplications200Response result = apiInstance.deleteDarTemplate(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplateApi#deleteDarTemplate");
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
| **id** | **Integer**| DAR template id | |

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

<a id="fetchDarTemplate"></a>
# **fetchDarTemplate**
> FetchDarTemplate200Response fetchDarTemplate(id)

DataAccessTemplate@show

Return a single DAR template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplateApi apiInstance = new DataAccessTemplateApi(defaultClient);
    Integer id = 1; // Integer | DAR template id
    try {
      FetchDarTemplate200Response result = apiInstance.fetchDarTemplate(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplateApi#fetchDarTemplate");
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
| **id** | **Integer**| DAR template id | |

### Return type

[**FetchDarTemplate200Response**](FetchDarTemplate200Response.md)

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

<a id="fetchDarTemplates"></a>
# **fetchDarTemplates**
> FetchDarTemplates200Response fetchDarTemplates(withQuestions, published)

DataAccessTemplate@index

List of DAR templates

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplateApi apiInstance = new DataAccessTemplateApi(defaultClient);
    Integer withQuestions = 1; // Integer | Include questions in response
    String published = "true"; // String | Template publication status to filter by (true, false)
    try {
      FetchDarTemplates200Response result = apiInstance.fetchDarTemplates(withQuestions, published);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplateApi#fetchDarTemplates");
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
| **withQuestions** | **Integer**| Include questions in response | [optional] |
| **published** | **String**| Template publication status to filter by (true, false) | [optional] |

### Return type

[**FetchDarTemplates200Response**](FetchDarTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="patchDarTemplate"></a>
# **patchDarTemplate**
> PatchDarTemplate200Response patchDarTemplate(id, patchDarTemplateRequest, sectionId)

DataAccessTemplate@update

Edit a system DAR template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplateApi apiInstance = new DataAccessTemplateApi(defaultClient);
    Integer id = 1; // Integer | DAR template id
    PatchDarTemplateRequest patchDarTemplateRequest = new PatchDarTemplateRequest(); // PatchDarTemplateRequest | DataAccessTemplate definition
    Integer sectionId = 1; // Integer | Section id
    try {
      PatchDarTemplate200Response result = apiInstance.patchDarTemplate(id, patchDarTemplateRequest, sectionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplateApi#patchDarTemplate");
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
| **id** | **Integer**| DAR template id | |
| **patchDarTemplateRequest** | [**PatchDarTemplateRequest**](PatchDarTemplateRequest.md)| DataAccessTemplate definition | |
| **sectionId** | **Integer**| Section id | [optional] |

### Return type

[**PatchDarTemplate200Response**](PatchDarTemplate200Response.md)

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

<a id="updateDarTemplate"></a>
# **updateDarTemplate**
> FetchDarTemplate200Response updateDarTemplate(id, updateDarTemplateRequest)

DataAccessTemplate@update

Update a system DAR template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplateApi apiInstance = new DataAccessTemplateApi(defaultClient);
    Integer id = 1; // Integer | DAR template id
    UpdateDarTemplateRequest updateDarTemplateRequest = new UpdateDarTemplateRequest(); // UpdateDarTemplateRequest | DataAccessTemplate definition
    try {
      FetchDarTemplate200Response result = apiInstance.updateDarTemplate(id, updateDarTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplateApi#updateDarTemplate");
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
| **id** | **Integer**| DAR template id | |
| **updateDarTemplateRequest** | [**UpdateDarTemplateRequest**](UpdateDarTemplateRequest.md)| DataAccessTemplate definition | |

### Return type

[**FetchDarTemplate200Response**](FetchDarTemplate200Response.md)

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

