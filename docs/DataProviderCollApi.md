# DataProviderCollApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchDataProviderColl**](DataProviderCollApi.md#fetchDataProviderColl) | **GET** /api/v1/data_provider_colls/{id} | DataProviderColl@show |
| [**fetchDataProviderCollSummary**](DataProviderCollApi.md#fetchDataProviderCollSummary) | **GET** /api/v1/data_provider_colls/{id}/summary | DataProviderColl@showSummary |
| [**fetchDataProviderColls**](DataProviderCollApi.md#fetchDataProviderColls) | **GET** /api/v1/data_provider_colls | DataProviderColl@index |


<a id="fetchDataProviderColl"></a>
# **fetchDataProviderColl**
> FetchDataProviderColl200Response fetchDataProviderColl(id)

DataProviderColl@show

Return a single DataProviderColl

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataProviderCollApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataProviderCollApi apiInstance = new DataProviderCollApi(defaultClient);
    Integer id = 1; // Integer | DataProviderColl ID
    try {
      FetchDataProviderColl200Response result = apiInstance.fetchDataProviderColl(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataProviderCollApi#fetchDataProviderColl");
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
| **id** | **Integer**| DataProviderColl ID | |

### Return type

[**FetchDataProviderColl200Response**](FetchDataProviderColl200Response.md)

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

<a id="fetchDataProviderCollSummary"></a>
# **fetchDataProviderCollSummary**
> FetchDataProviderCollSummary200Response fetchDataProviderCollSummary(id)

DataProviderColl@showSummary

Return a single DataProviderColl - summary

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataProviderCollApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataProviderCollApi apiInstance = new DataProviderCollApi(defaultClient);
    Integer id = 1; // Integer | DataProviderColl ID - summary
    try {
      FetchDataProviderCollSummary200Response result = apiInstance.fetchDataProviderCollSummary(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataProviderCollApi#fetchDataProviderCollSummary");
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
| **id** | **Integer**| DataProviderColl ID - summary | |

### Return type

[**FetchDataProviderCollSummary200Response**](FetchDataProviderCollSummary200Response.md)

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

<a id="fetchDataProviderColls"></a>
# **fetchDataProviderColls**
> FetchDataProviderColls200Response fetchDataProviderColls(perPage)

DataProviderColl@index

Returns a list of DataProviderColls enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataProviderCollApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataProviderCollApi apiInstance = new DataProviderCollApi(defaultClient);
    Integer perPage = 1; // Integer | per page
    try {
      FetchDataProviderColls200Response result = apiInstance.fetchDataProviderColls(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataProviderCollApi#fetchDataProviderColls");
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

[**FetchDataProviderColls200Response**](FetchDataProviderColls200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

