# UserOrganisationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchUserOrganisations**](UserOrganisationApi.md#fetchUserOrganisations) | **GET** /api/v1/users/organisations | UserOrganisation@index |


<a id="fetchUserOrganisations"></a>
# **fetchUserOrganisations**
> FetchUserOrganisations200Response fetchUserOrganisations()

UserOrganisation@index

Return a distinct list of all organisations which users belong to

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserOrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserOrganisationApi apiInstance = new UserOrganisationApi(defaultClient);
    try {
      FetchUserOrganisations200Response result = apiInstance.fetchUserOrganisations();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserOrganisationApi#fetchUserOrganisations");
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

[**FetchUserOrganisations200Response**](FetchUserOrganisations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

