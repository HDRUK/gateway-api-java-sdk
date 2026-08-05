# DataAccessApplicationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteTeamDarApplicationFile**](DataAccessApplicationApi.md#deleteTeamDarApplicationFile) | **DELETE** /api/v1/teams/{teamId}/dar/applications/{id}/files/{fileId} | DataAccessApplication@destroyFile |
| [**fetchTeamDarApplicationAnswers**](DataAccessApplicationApi.md#fetchTeamDarApplicationAnswers) | **GET** /api/v1/teams/{teamId}/dar/applications/{id}/answers | DataAccessApplication@showAnswers |
| [**fetchTeamDarApplicationDownloadZip**](DataAccessApplicationApi.md#fetchTeamDarApplicationDownloadZip) | **GET** /api/v1/teams/{teamId}/dar/applications/{id}/download | DataAccessApplication@download |
| [**fetchTeamDarApplicationFile**](DataAccessApplicationApi.md#fetchTeamDarApplicationFile) | **GET** /api/v1/teams/{teamId}/dar/applications/{id}/files/{fileId}/download | DataAccessApplication@downloadFile |
| [**fetchTeamDarApplicationFiles**](DataAccessApplicationApi.md#fetchTeamDarApplicationFiles) | **GET** /api/v1/teams/{teamId}/dar/applications/{id}/files | DataAccessApplication@showFiles |
| [**fetchTeamDarApplicationStatusHistory**](DataAccessApplicationApi.md#fetchTeamDarApplicationStatusHistory) | **GET** /api/v1/teams/{teamId}/dar/applications/{id}/status | DataAccessApplication@status |
| [**updateTeamDarApplication**](DataAccessApplicationApi.md#updateTeamDarApplication) | **PATCH** /api/v1/teams/{teamId}/dar/applications/{id} | DataAccessApplication@update |


<a id="deleteTeamDarApplicationFile"></a>
# **deleteTeamDarApplicationFile**
> DeleteApplications200Response deleteTeamDarApplicationFile(teamId, id, fileId)

DataAccessApplication@destroyFile

Delete a file associated with a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer fileId = 1; // Integer | File id
    try {
      DeleteApplications200Response result = apiInstance.deleteTeamDarApplicationFile(teamId, id, fileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#deleteTeamDarApplicationFile");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |
| **fileId** | **Integer**| File id | |

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

<a id="fetchTeamDarApplicationAnswers"></a>
# **fetchTeamDarApplicationAnswers**
> FetchTeamDarApplicationAnswers200Response fetchTeamDarApplicationAnswers(teamId, id)

DataAccessApplication@showAnswers

Return answers from a single DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplicationAnswers200Response result = apiInstance.fetchTeamDarApplicationAnswers(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#fetchTeamDarApplicationAnswers");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplicationAnswers200Response**](FetchTeamDarApplicationAnswers200Response.md)

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

<a id="fetchTeamDarApplicationDownloadZip"></a>
# **fetchTeamDarApplicationDownloadZip**
> fetchTeamDarApplicationDownloadZip(teamId, id)

DataAccessApplication@download

Returns a DAR form as a CSV with attached files as a zip

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    try {
      apiInstance.fetchTeamDarApplicationDownloadZip(teamId, id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#fetchTeamDarApplicationDownloadZip");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: file, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchTeamDarApplicationFile"></a>
# **fetchTeamDarApplicationFile**
> fetchTeamDarApplicationFile(teamId, id, fileId)

DataAccessApplication@downloadFile

Download a file associated with a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    String fileId = "1"; // String | File uuid
    try {
      apiInstance.fetchTeamDarApplicationFile(teamId, id, fileId);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#fetchTeamDarApplicationFile");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |
| **fileId** | **String**| File uuid | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: file, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchTeamDarApplicationFiles"></a>
# **fetchTeamDarApplicationFiles**
> FetchTeamDarApplicationFiles200Response fetchTeamDarApplicationFiles(teamId, id)

DataAccessApplication@showFiles

Return a list of files associated with a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplicationFiles200Response result = apiInstance.fetchTeamDarApplicationFiles(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#fetchTeamDarApplicationFiles");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplicationFiles200Response**](FetchTeamDarApplicationFiles200Response.md)

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

<a id="fetchTeamDarApplicationStatusHistory"></a>
# **fetchTeamDarApplicationStatusHistory**
> FetchTeamDarApplicationStatusHistory200Response fetchTeamDarApplicationStatusHistory(teamId, id)

DataAccessApplication@status

Return the status history of a single DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplicationStatusHistory200Response result = apiInstance.fetchTeamDarApplicationStatusHistory(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#fetchTeamDarApplicationStatusHistory");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplicationStatusHistory200Response**](FetchTeamDarApplicationStatusHistory200Response.md)

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

<a id="updateTeamDarApplication"></a>
# **updateTeamDarApplication**
> FetchTeamDarApplication200Response updateTeamDarApplication(teamId, id, updateTeamDarApplicationRequest)

DataAccessApplication@update

Edit a system DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationApi apiInstance = new DataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    UpdateTeamDarApplicationRequest updateTeamDarApplicationRequest = new UpdateTeamDarApplicationRequest(); // UpdateTeamDarApplicationRequest | DataAccessApplication definition
    try {
      FetchTeamDarApplication200Response result = apiInstance.updateTeamDarApplication(teamId, id, updateTeamDarApplicationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationApi#updateTeamDarApplication");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR application id | |
| **updateTeamDarApplicationRequest** | [**UpdateTeamDarApplicationRequest**](UpdateTeamDarApplicationRequest.md)| DataAccessApplication definition | |

### Return type

[**FetchTeamDarApplication200Response**](FetchTeamDarApplication200Response.md)

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

