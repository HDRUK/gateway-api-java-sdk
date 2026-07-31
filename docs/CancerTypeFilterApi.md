# CancerTypeFilterApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getCancerTypeFilter**](CancerTypeFilterApi.md#getCancerTypeFilter) | **GET** /api/v1/cancer-type-filters/{filter_id} | Get a single cancer type filter |
| [**getCancerTypeFilters**](CancerTypeFilterApi.md#getCancerTypeFilters) | **GET** /api/v1/cancer-type-filters | Get all cancer type filters |


<a id="getCancerTypeFilter"></a>
# **getCancerTypeFilter**
> GetCancerTypeFilter200Response getCancerTypeFilter(filterId)

Get a single cancer type filter

Returns a single cancer type filter with its children by filter_id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CancerTypeFilterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CancerTypeFilterApi apiInstance = new CancerTypeFilterApi(defaultClient);
    String filterId = "0_0_2_59"; // String | Filter ID (e.g., 0_0, 0_0_2_59)
    try {
      GetCancerTypeFilter200Response result = apiInstance.getCancerTypeFilter(filterId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CancerTypeFilterApi#getCancerTypeFilter");
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
| **filterId** | **String**| Filter ID (e.g., 0_0, 0_0_2_59) | |

### Return type

[**GetCancerTypeFilter200Response**](GetCancerTypeFilter200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Not found |  -  |

<a id="getCancerTypeFilters"></a>
# **getCancerTypeFilters**
> GetCancerTypeFilters200Response getCancerTypeFilters(parentId, level)

Get all cancer type filters

Returns a hierarchical tree of cancer type filters

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CancerTypeFilterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CancerTypeFilterApi apiInstance = new CancerTypeFilterApi(defaultClient);
    Integer parentId = 56; // Integer | Filter by parent ID
    Integer level = 56; // Integer | Filter by hierarchy level
    try {
      GetCancerTypeFilters200Response result = apiInstance.getCancerTypeFilters(parentId, level);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CancerTypeFilterApi#getCancerTypeFilters");
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
| **parentId** | **Integer**| Filter by parent ID | [optional] |
| **level** | **Integer**| Filter by hierarchy level | [optional] |

### Return type

[**GetCancerTypeFilters200Response**](GetCancerTypeFilters200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

