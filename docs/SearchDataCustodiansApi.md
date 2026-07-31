# SearchDataCustodiansApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchDataCustodians**](SearchDataCustodiansApi.md#searchDataCustodians) | **POST** /api/v1/search/data_custodians | Search@data_custodians |


<a id="searchDataCustodians"></a>
# **searchDataCustodians**
> SearchDataCustodians200Response searchDataCustodians(searchDataCustodiansRequest, sort, direction, perPage)

Search@data_custodians

Returns gateway data custodians related to the provided query term(s)

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchDataCustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SearchDataCustodiansApi apiInstance = new SearchDataCustodiansApi(defaultClient);
    SearchDataCustodiansRequest searchDataCustodiansRequest = new SearchDataCustodiansRequest(); // SearchDataCustodiansRequest | Submit search query
    String sort = "created"; // String | Field to sort by (default: 'score')
    String direction = "asc"; // String | Sort direction ('asc' or 'desc', default: 'desc')
    Integer perPage = 25; // Integer | Number of results to return per page
    try {
      SearchDataCustodians200Response result = apiInstance.searchDataCustodians(searchDataCustodiansRequest, sort, direction, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchDataCustodiansApi#searchDataCustodians");
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
| **searchDataCustodiansRequest** | [**SearchDataCustodiansRequest**](SearchDataCustodiansRequest.md)| Submit search query | |
| **sort** | **String**| Field to sort by (default: &#39;score&#39;) | [optional] |
| **direction** | **String**| Sort direction (&#39;asc&#39; or &#39;desc&#39;, default: &#39;desc&#39;) | [optional] [enum: asc, desc] |
| **perPage** | **Integer**| Number of results to return per page | [optional] |

### Return type

[**SearchDataCustodians200Response**](SearchDataCustodians200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

