# ApplicationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createApplications**](ApplicationApi.md#createApplications) | **POST** /api/v1/applications | ApplicationController@store |
| [**deleteApplications**](ApplicationApi.md#deleteApplications) | **DELETE** /api/v1/applications/{id} | ApplicationController@delete |
| [**editApplications**](ApplicationApi.md#editApplications) | **PATCH** /api/v1/applications/{id} | ApplicationController@edit |
| [**fetchAllApplications**](ApplicationApi.md#fetchAllApplications) | **GET** /api/v1/applications | ApplicationController@index |
| [**fetchAllSitemap**](ApplicationApi.md#fetchAllSitemap) | **GET** /api/v1/sitemap | SiteMapController@index |
| [**fetchApplications**](ApplicationApi.md#fetchApplications) | **GET** /api/v1/applications/{id} | ApplicationController@show |
| [**patchApplicationsClientId**](ApplicationApi.md#patchApplicationsClientId) | **PATCH** /api/v1/applications/{id}/clientid | ApplicationController@generateClientIdById |
| [**updateApplications**](ApplicationApi.md#updateApplications) | **PUT** /api/v1/applications/{id} | ApplicationController@update |


<a id="createApplications"></a>
# **createApplications**
> CreateApplications200Response createApplications(createApplicationsRequest)

ApplicationController@store

Creates application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    CreateApplicationsRequest createApplicationsRequest = new CreateApplicationsRequest(); // CreateApplicationsRequest | Application definition
    try {
      CreateApplications200Response result = apiInstance.createApplications(createApplicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#createApplications");
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
| **createApplicationsRequest** | [**CreateApplicationsRequest**](CreateApplicationsRequest.md)| Application definition | |

### Return type

[**CreateApplications200Response**](CreateApplications200Response.md)

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

<a id="deleteApplications"></a>
# **deleteApplications**
> DeleteAliases200Response deleteApplications(id)

ApplicationController@delete

Delete application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    Integer id = 1; // Integer | application id
    try {
      DeleteAliases200Response result = apiInstance.deleteApplications(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#deleteApplications");
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
| **id** | **Integer**| application id | |

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

<a id="editApplications"></a>
# **editApplications**
> UpdateApplications200Response editApplications(id, editApplicationsRequest)

ApplicationController@edit

Edit application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    Integer id = 1; // Integer | application id
    EditApplicationsRequest editApplicationsRequest = new EditApplicationsRequest(); // EditApplicationsRequest | ActivityLog definition
    try {
      UpdateApplications200Response result = apiInstance.editApplications(id, editApplicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#editApplications");
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
| **id** | **Integer**| application id | |
| **editApplicationsRequest** | [**EditApplicationsRequest**](EditApplicationsRequest.md)| ActivityLog definition | |

### Return type

[**UpdateApplications200Response**](UpdateApplications200Response.md)

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

<a id="fetchAllApplications"></a>
# **fetchAllApplications**
> FetchAllApplications200Response fetchAllApplications(teamId, text, status)

ApplicationController@index

Returns a list of applications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    Integer teamId = 56; // Integer | Filter Apps by the teamId
    String text = "text_example"; // String | Search term to filter by application name or description.
    String status = "1"; // String | Filter by application status is enabled or not (true or false).
    try {
      FetchAllApplications200Response result = apiInstance.fetchAllApplications(teamId, text, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#fetchAllApplications");
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
| **teamId** | **Integer**| Filter Apps by the teamId | [optional] |
| **text** | **String**| Search term to filter by application name or description. | [optional] |
| **status** | **String**| Filter by application status is enabled or not (true or false). | [optional] [enum: 1, 0] |

### Return type

[**FetchAllApplications200Response**](FetchAllApplications200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchAllSitemap"></a>
# **fetchAllSitemap**
> FetchAllSitemap200Response fetchAllSitemap()

SiteMapController@index

Returns a list of all ids and last updated date for Collections, Data Custodians, Data Custodian Networks, Durs, DataSets, Tools

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    try {
      FetchAllSitemap200Response result = apiInstance.fetchAllSitemap();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#fetchAllSitemap");
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

[**FetchAllSitemap200Response**](FetchAllSitemap200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchApplications"></a>
# **fetchApplications**
> FetchApplications200Response fetchApplications(id)

ApplicationController@show

Get application by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    Integer id = 1; // Integer | application id
    try {
      FetchApplications200Response result = apiInstance.fetchApplications(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#fetchApplications");
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
| **id** | **Integer**| application id | |

### Return type

[**FetchApplications200Response**](FetchApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="patchApplicationsClientId"></a>
# **patchApplicationsClientId**
> UpdateApplications200Response patchApplicationsClientId(id)

ApplicationController@generateClientIdById

Generate Client ID application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    Integer id = 1; // Integer | application id
    try {
      UpdateApplications200Response result = apiInstance.patchApplicationsClientId(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#patchApplicationsClientId");
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
| **id** | **Integer**| application id | |

### Return type

[**UpdateApplications200Response**](UpdateApplications200Response.md)

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

<a id="updateApplications"></a>
# **updateApplications**
> UpdateApplications200Response updateApplications(id, updateApplicationsRequest)

ApplicationController@update

Update application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ApplicationApi apiInstance = new ApplicationApi(defaultClient);
    Integer id = 1; // Integer | application id
    UpdateApplicationsRequest updateApplicationsRequest = new UpdateApplicationsRequest(); // UpdateApplicationsRequest | ActivityLog definition
    try {
      UpdateApplications200Response result = apiInstance.updateApplications(id, updateApplicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApplicationApi#updateApplications");
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
| **id** | **Integer**| application id | |
| **updateApplicationsRequest** | [**UpdateApplicationsRequest**](UpdateApplicationsRequest.md)| ActivityLog definition | |

### Return type

[**UpdateApplications200Response**](UpdateApplications200Response.md)

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

