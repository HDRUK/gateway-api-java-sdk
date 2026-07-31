# UploadApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createFiles**](UploadApi.md#createFiles) | **POST** /api/v1/files | Upload@upload |
| [**deleteFilesProcessed**](UploadApi.md#deleteFilesProcessed) | **DELETE** /api/v1/files/processed/{id} | Upload@destroy |
| [**fetchFiles**](UploadApi.md#fetchFiles) | **GET** /api/v1/files/{uuid} | Upload@show |
| [**fetchFilesProcessedContent**](UploadApi.md#fetchFilesProcessedContent) | **GET** /api/v1/files/processed/{uuid}/download | Upload@content |


<a id="createFiles"></a>
# **createFiles**
> CreateFiles200Response createFiles(entityFlag, teamId, applicationId, questionId)

Upload@upload

Upload a file to the gateway-api via scanning sub-service

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UploadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadApi apiInstance = new UploadApi(defaultClient);
    String entityFlag = "dur-from-upload"; // String | Flag to indicate the purpose of the file upload e.g. dur-from-upload
    Integer teamId = 10; // Integer | Id of team associated with the file upload
    Integer applicationId = 10; // Integer | Id of dar application associated with the file upload
    Integer questionId = 10; // Integer | Id of the question in the dar application associated with the file upload
    try {
      CreateFiles200Response result = apiInstance.createFiles(entityFlag, teamId, applicationId, questionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadApi#createFiles");
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
| **entityFlag** | **String**| Flag to indicate the purpose of the file upload e.g. dur-from-upload | [optional] |
| **teamId** | **Integer**| Id of team associated with the file upload | [optional] |
| **applicationId** | **Integer**| Id of dar application associated with the file upload | [optional] |
| **questionId** | **Integer**| Id of the question in the dar application associated with the file upload | [optional] |

### Return type

[**CreateFiles200Response**](CreateFiles200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upload complete |  -  |

<a id="deleteFilesProcessed"></a>
# **deleteFilesProcessed**
> DeleteAliases200Response deleteFilesProcessed(id)

Upload@destroy

Delete a processed file

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UploadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UploadApi apiInstance = new UploadApi(defaultClient);
    String id = "1"; // String | file uuid
    try {
      DeleteAliases200Response result = apiInstance.deleteFilesProcessed(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadApi#deleteFilesProcessed");
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
| **id** | **String**| file uuid | |

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

<a id="fetchFiles"></a>
# **fetchFiles**
> FetchFiles200Response fetchFiles(uuid)

Upload@show

Get the scanning status of an upload

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UploadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadApi apiInstance = new UploadApi(defaultClient);
    String uuid = "1"; // String | upload id
    try {
      FetchFiles200Response result = apiInstance.fetchFiles(uuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadApi#fetchFiles");
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
| **uuid** | **String**| upload id | |

### Return type

[**FetchFiles200Response**](FetchFiles200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchFilesProcessedContent"></a>
# **fetchFilesProcessedContent**
> FetchFilesProcessedContent200Response fetchFilesProcessedContent(uuid)

Upload@content

Get the content of a processed file

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UploadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadApi apiInstance = new UploadApi(defaultClient);
    String uuid = "1"; // String | upload id
    try {
      FetchFilesProcessedContent200Response result = apiInstance.fetchFilesProcessedContent(uuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadApi#fetchFilesProcessedContent");
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
| **uuid** | **String**| upload id | |

### Return type

[**FetchFilesProcessedContent200Response**](FetchFilesProcessedContent200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

