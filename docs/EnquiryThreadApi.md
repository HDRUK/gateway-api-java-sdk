# EnquiryThreadApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createEnquiryThreads**](EnquiryThreadApi.md#createEnquiryThreads) | **POST** /api/v1/enquiry_threads | EnquiryThread@store |
| [**fetchAllEnquiryThreads**](EnquiryThreadApi.md#fetchAllEnquiryThreads) | **GET** /api/v1/enquiry_threads | EnquiryThread@index |
| [**fetchEnquiryThreads**](EnquiryThreadApi.md#fetchEnquiryThreads) | **GET** /api/v1/enquiry_threads/{id} | EnquiryThread@show |


<a id="createEnquiryThreads"></a>
# **createEnquiryThreads**
> CreateCategories200Response createEnquiryThreads(createEnquiryThreadsRequest)

EnquiryThread@store

Creates one or more new EnquiryThreads

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.EnquiryThreadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    EnquiryThreadApi apiInstance = new EnquiryThreadApi(defaultClient);
    CreateEnquiryThreadsRequest createEnquiryThreadsRequest = new CreateEnquiryThreadsRequest(); // CreateEnquiryThreadsRequest | EnquiryThread definition
    try {
      CreateCategories200Response result = apiInstance.createEnquiryThreads(createEnquiryThreadsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EnquiryThreadApi#createEnquiryThreads");
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
| **createEnquiryThreadsRequest** | [**CreateEnquiryThreadsRequest**](CreateEnquiryThreadsRequest.md)| EnquiryThread definition | |

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

<a id="fetchAllEnquiryThreads"></a>
# **fetchAllEnquiryThreads**
> FetchAllEnquiryThreads200Response fetchAllEnquiryThreads(perPage)

EnquiryThread@index

Returns a list of EnquiryThreads from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.EnquiryThreadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    EnquiryThreadApi apiInstance = new EnquiryThreadApi(defaultClient);
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllEnquiryThreads200Response result = apiInstance.fetchAllEnquiryThreads(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EnquiryThreadApi#fetchAllEnquiryThreads");
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
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchAllEnquiryThreads200Response**](FetchAllEnquiryThreads200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchEnquiryThreads"></a>
# **fetchEnquiryThreads**
> FetchAllEnquiryThreads200Response fetchEnquiryThreads(id)

EnquiryThread@show

Return a single EnquiryThread

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.EnquiryThreadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    EnquiryThreadApi apiInstance = new EnquiryThreadApi(defaultClient);
    Integer id = 1; // Integer | EnquiryThread id
    try {
      FetchAllEnquiryThreads200Response result = apiInstance.fetchEnquiryThreads(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EnquiryThreadApi#fetchEnquiryThreads");
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
| **id** | **Integer**| EnquiryThread id | |

### Return type

[**FetchAllEnquiryThreads200Response**](FetchAllEnquiryThreads200Response.md)

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

