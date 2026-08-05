# TeamDataAccessTemplateApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteTeamDarTemplateFile**](TeamDataAccessTemplateApi.md#deleteTeamDarTemplateFile) | **DELETE** /api/v1/teams/{teamId}/dar/templates/{id}/files/{fileId} | TeamDataAccessTemplateController@destroyFile |
| [**fetchTeamDarTemplates**](TeamDataAccessTemplateApi.md#fetchTeamDarTemplates) | **GET** /api/v1/teams/{teamId}/dar/templates | TeamDataAccessTemplateController@index |
| [**teamDarTemplateCountUniqueFields**](TeamDataAccessTemplateApi.md#teamDarTemplateCountUniqueFields) | **GET** /api/v1/teams/{teamId}/dar/templates/count/{field} | TeamDataAccessTemplateController@count |


<a id="deleteTeamDarTemplateFile"></a>
# **deleteTeamDarTemplateFile**
> DeleteApplications200Response deleteTeamDarTemplateFile(teamId, id, fileId)

TeamDataAccessTemplateController@destroyFile

Delete a file associated with a DAR template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessTemplateApi apiInstance = new TeamDataAccessTemplateApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR template id
    String fileId = "1"; // String | File id
    try {
      DeleteApplications200Response result = apiInstance.deleteTeamDarTemplateFile(teamId, id, fileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessTemplateApi#deleteTeamDarTemplateFile");
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
| **teamId** | **Integer**| Team id | |
| **id** | **Integer**| DAR template id | |
| **fileId** | **String**| File id | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="fetchTeamDarTemplates"></a>
# **fetchTeamDarTemplates**
> FetchDarTemplates200Response fetchTeamDarTemplates(teamId, published)

TeamDataAccessTemplateController@index

List of dar templates belonging to a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessTemplateApi apiInstance = new TeamDataAccessTemplateApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    String published = "true"; // String | Template publication status to filter by (true, false)
    try {
      FetchDarTemplates200Response result = apiInstance.fetchTeamDarTemplates(teamId, published);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessTemplateApi#fetchTeamDarTemplates");
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
| **teamId** | **Integer**| Team id | |
| **published** | **String**| Template publication status to filter by (true, false) | [optional] |

### Return type

[**FetchDarTemplates200Response**](FetchDarTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="teamDarTemplateCountUniqueFields"></a>
# **teamDarTemplateCountUniqueFields**
> CountUniqueFieldsCollections200Response teamDarTemplateCountUniqueFields(teamId, field)

TeamDataAccessTemplateController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessTemplateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessTemplateApi apiInstance = new TeamDataAccessTemplateApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    String field = "published"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.teamDarTemplateCountUniqueFields(teamId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessTemplateApi#teamDarTemplateCountUniqueFields");
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
| **teamId** | **Integer**| Team id | |
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

