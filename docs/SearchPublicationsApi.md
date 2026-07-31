# SearchPublicationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchPublications**](SearchPublicationsApi.md#searchPublications) | **POST** /api/v1/search/publications | Search@publications |
| [**searchPublicationsByDoi**](SearchPublicationsApi.md#searchPublicationsByDoi) | **POST** /api/v1/search/doi | Search@publications |


<a id="searchPublications"></a>
# **searchPublications**
> SearchPublications200Response searchPublications(searchPublicationsRequest, sort, direction, source)

Search@publications

Returns gateway publications related to the provided query term(s)

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchPublicationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SearchPublicationsApi apiInstance = new SearchPublicationsApi(defaultClient);
    SearchPublicationsRequest searchPublicationsRequest = new SearchPublicationsRequest(); // SearchPublicationsRequest | Submit search query
    String sort = "created"; // String | Field to sort by (default: 'score')
    String direction = "asc"; // String | Sort direction ('asc' or 'desc', default: 'desc')
    String source = "GAT"; // String | Which source to search ('GAT' or 'FED', default: 'GAT')
    try {
      SearchPublications200Response result = apiInstance.searchPublications(searchPublicationsRequest, sort, direction, source);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchPublicationsApi#searchPublications");
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
| **searchPublicationsRequest** | [**SearchPublicationsRequest**](SearchPublicationsRequest.md)| Submit search query | |
| **sort** | **String**| Field to sort by (default: &#39;score&#39;) | [optional] |
| **direction** | **String**| Sort direction (&#39;asc&#39; or &#39;desc&#39;, default: &#39;desc&#39;) | [optional] [enum: asc, desc] |
| **source** | **String**| Which source to search (&#39;GAT&#39; or &#39;FED&#39;, default: &#39;GAT&#39;) | [optional] [enum: GAT, FED] |

### Return type

[**SearchPublications200Response**](SearchPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="searchPublicationsByDoi"></a>
# **searchPublicationsByDoi**
> SearchPublicationsByDoi200Response searchPublicationsByDoi(searchPublicationsByDoiRequest)

Search@publications

Returns publications from EuropePMC matching a give DOI

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchPublicationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SearchPublicationsApi apiInstance = new SearchPublicationsApi(defaultClient);
    SearchPublicationsByDoiRequest searchPublicationsByDoiRequest = new SearchPublicationsByDoiRequest(); // SearchPublicationsByDoiRequest | Submit search query
    try {
      SearchPublicationsByDoi200Response result = apiInstance.searchPublicationsByDoi(searchPublicationsByDoiRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchPublicationsApi#searchPublicationsByDoi");
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
| **searchPublicationsByDoiRequest** | [**SearchPublicationsByDoiRequest**](SearchPublicationsByDoiRequest.md)| Submit search query | |

### Return type

[**SearchPublicationsByDoi200Response**](SearchPublicationsByDoi200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **204** | No match found |  -  |

