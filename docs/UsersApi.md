# UsersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**verifySecondaryEmail**](UsersApi.md#verifySecondaryEmail) | **GET** /api/v1/users/verify-secondary-email/{uuid} | Verify user&#39;s secondary email using a UUID |


<a id="verifySecondaryEmail"></a>
# **verifySecondaryEmail**
> VerifySecondaryEmail200Response verifySecondaryEmail(uuid)

Verify user&#39;s secondary email using a UUID

This endpoint verifies the secondary email for a user if the UUID is valid and not expired.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UsersApi apiInstance = new UsersApi(defaultClient);
    String uuid = "03af1f5e-5cd2-4c41-ae23-56dd2c9efc67"; // String | Verification UUID
    try {
      VerifySecondaryEmail200Response result = apiInstance.verifySecondaryEmail(uuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#verifySecondaryEmail");
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
| **uuid** | **String**| Verification UUID | |

### Return type

[**VerifySecondaryEmail200Response**](VerifySecondaryEmail200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email verified successfully |  -  |
| **400** | Invalid or expired token |  -  |
| **404** | UUID not found |  -  |

