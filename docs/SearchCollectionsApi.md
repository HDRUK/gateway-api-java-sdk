# SearchCollectionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchCollections**](SearchCollectionsApi.md#searchCollections) | **POST** /api/v1/search/collections | Search@collections |


<a id="searchCollections"></a>
# **searchCollections**
> SearchCollections200Response searchCollections(searchCollectionsRequest, sort, direction)

Search@collections

Returns gateway collections related to the provided query term(s)

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchCollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SearchCollectionsApi apiInstance = new SearchCollectionsApi(defaultClient);
    SearchCollectionsRequest searchCollectionsRequest = new SearchCollectionsRequest(); // SearchCollectionsRequest | Submit search query
    String sort = "created"; // String | Field to sort by (default: 'score')
    String direction = "asc"; // String | Sort direction ('asc' or 'desc', default: 'desc')
    try {
      SearchCollections200Response result = apiInstance.searchCollections(searchCollectionsRequest, sort, direction);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchCollectionsApi#searchCollections");
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
| **searchCollectionsRequest** | [**SearchCollectionsRequest**](SearchCollectionsRequest.md)| Submit search query | |
| **sort** | **String**| Field to sort by (default: &#39;score&#39;) | [optional] |
| **direction** | **String**| Sort direction (&#39;asc&#39; or &#39;desc&#39;, default: &#39;desc&#39;) | [optional] [enum: asc, desc] |

### Return type

[**SearchCollections200Response**](SearchCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

