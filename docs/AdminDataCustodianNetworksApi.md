# AdminDataCustodianNetworksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchAdminDataCustodianNetworks**](AdminDataCustodianNetworksApi.md#fetchAdminDataCustodianNetworks) | **GET** /api/v2/admin/data_custodian_networks | DataCustodianNetworks@adminIndex |


<a id="fetchAdminDataCustodianNetworks"></a>
# **fetchAdminDataCustodianNetworks**
> fetchAdminDataCustodianNetworks(perPage)

DataCustodianNetworks@adminIndex

Superadmin-only listing used by the network management admin screen — unlike index(), this is not filtered to enabled&#x3D;1, so disabled networks remain visible/manageable.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AdminDataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AdminDataCustodianNetworksApi apiInstance = new AdminDataCustodianNetworksApi(defaultClient);
    Integer perPage = 1; // Integer | per page
    try {
      apiInstance.fetchAdminDataCustodianNetworks(perPage);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminDataCustodianNetworksApi#fetchAdminDataCustodianNetworks");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

