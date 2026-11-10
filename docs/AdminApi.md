# AdminApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**revokeAllTokensV2**](AdminApi.md#revokeAllTokensV2) | **POST** /api/v2/admin/tokens/revoke_all | TokenRevocationController@revokeAll |


<a id="revokeAllTokensV2"></a>
# **revokeAllTokensV2**
> RevokeAllTokensV2200Response revokeAllTokensV2()

TokenRevocationController@revokeAll

Revoke every Gateway JWT issued up to now, including the caller&#39;s own. All users must sign in again.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AdminApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AdminApi apiInstance = new AdminApi(defaultClient);
    try {
      RevokeAllTokensV2200Response result = apiInstance.revokeAllTokensV2();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminApi#revokeAllTokensV2");
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

[**RevokeAllTokensV2200Response**](RevokeAllTokensV2200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |

