# DataAccessTemplatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**darTemplateCountUniqueFields**](DataAccessTemplatesApi.md#darTemplateCountUniqueFields) | **GET** /api/v1/dar/templates/count/{field} | DataAccessTemplateController@count |


<a id="darTemplateCountUniqueFields"></a>
# **darTemplateCountUniqueFields**
> CountUniqueFieldsCollections200Response darTemplateCountUniqueFields(field)

DataAccessTemplateController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessTemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessTemplatesApi apiInstance = new DataAccessTemplatesApi(defaultClient);
    String field = "published"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.darTemplateCountUniqueFields(field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessTemplatesApi#darTemplateCountUniqueFields");
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
| **field** | **String**| name of the field to perform a count on | |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

