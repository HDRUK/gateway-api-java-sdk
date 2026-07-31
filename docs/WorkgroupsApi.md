# WorkgroupsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchAllWorkgroups**](WorkgroupsApi.md#fetchAllWorkgroups) | **GET** /api/v1/workgroups | WorkgroupController@index |


<a id="fetchAllWorkgroups"></a>
# **fetchAllWorkgroups**
> FetchAllWorkgroups200Response fetchAllWorkgroups()

WorkgroupController@index

Get All Workgroups

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WorkgroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkgroupsApi apiInstance = new WorkgroupsApi(defaultClient);
    try {
      FetchAllWorkgroups200Response result = apiInstance.fetchAllWorkgroups();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkgroupsApi#fetchAllWorkgroups");
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

[**FetchAllWorkgroups200Response**](FetchAllWorkgroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

