# SearchDataUsesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchDataUses**](SearchDataUsesApi.md#searchDataUses) | **POST** /api/v1/search/dur | Search@data_uses |


<a id="searchDataUses"></a>
# **searchDataUses**
> SearchDataUses200Response searchDataUses(searchDataUsesRequest, sort, direction, download)

Search@data_uses

Returns gateway data uses related to the provided query term(s)

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchDataUsesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SearchDataUsesApi apiInstance = new SearchDataUsesApi(defaultClient);
    SearchDataUsesRequest searchDataUsesRequest = new SearchDataUsesRequest(); // SearchDataUsesRequest | Submit search query
    String sort = "created"; // String | Field to sort by (default: 'score')
    String direction = "asc"; // String | Sort direction ('asc' or 'desc', default: 'desc')
    Boolean download = false; // Boolean | Download a csv of the results (default: false)
    try {
      SearchDataUses200Response result = apiInstance.searchDataUses(searchDataUsesRequest, sort, direction, download);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchDataUsesApi#searchDataUses");
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
| **searchDataUsesRequest** | [**SearchDataUsesRequest**](SearchDataUsesRequest.md)| Submit search query | |
| **sort** | **String**| Field to sort by (default: &#39;score&#39;) | [optional] |
| **direction** | **String**| Sort direction (&#39;asc&#39; or &#39;desc&#39;, default: &#39;desc&#39;) | [optional] [enum: asc, desc] |
| **download** | **Boolean**| Download a csv of the results (default: false) | [optional] |

### Return type

[**SearchDataUses200Response**](SearchDataUses200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

