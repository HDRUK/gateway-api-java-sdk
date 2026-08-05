# TeamDataAccessApplicationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countTeamDarApplications**](TeamDataAccessApplicationApi.md#countTeamDarApplications) | **GET** /api/v1/teams/{teamId}/dar/applications/count | TeamDataAccessApplicationController@allCounts |
| [**countUniqueFieldsDarApplications**](TeamDataAccessApplicationApi.md#countUniqueFieldsDarApplications) | **GET** /api/v1/teams/{teamId}/dar/applications/count/{field} | TeamDataAccessApplicationController@count |
| [**fetchTeamDarApplication**](TeamDataAccessApplicationApi.md#fetchTeamDarApplication) | **GET** /api/v1/teams/{teamId}/dar/applications/{id} | TeamDataAccessApplicationController@show |
| [**fetchTeamDarApplications**](TeamDataAccessApplicationApi.md#fetchTeamDarApplications) | **GET** /api/v1/teams/{teamId}/dar/applications | TeamDataAccessApplicationController@index |


<a id="countTeamDarApplications"></a>
# **countTeamDarApplications**
> CountUniqueFieldsCollections200Response countTeamDarApplications(teamId)

TeamDataAccessApplicationController@allCounts

Get Counts for all status fields in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessApplicationApi apiInstance = new TeamDataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countTeamDarApplications(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessApplicationApi#countTeamDarApplications");
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

<a id="countUniqueFieldsDarApplications"></a>
# **countUniqueFieldsDarApplications**
> CountUniqueFieldsCollections200Response countUniqueFieldsDarApplications(teamId, field)

TeamDataAccessApplicationController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessApplicationApi apiInstance = new TeamDataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    String field = "approval_status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUniqueFieldsDarApplications(teamId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessApplicationApi#countUniqueFieldsDarApplications");
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

<a id="fetchTeamDarApplication"></a>
# **fetchTeamDarApplication**
> FetchTeamDarApplication200Response fetchTeamDarApplication(teamId, id)

TeamDataAccessApplicationController@show

Return a single DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessApplicationApi apiInstance = new TeamDataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplication200Response result = apiInstance.fetchTeamDarApplication(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessApplicationApi#fetchTeamDarApplication");
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
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplication200Response**](FetchTeamDarApplication200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchTeamDarApplications"></a>
# **fetchTeamDarApplications**
> FetchTeamDarApplications200Response fetchTeamDarApplications(teamId)

TeamDataAccessApplicationController@index

List of dar applications belonging to a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamDataAccessApplicationApi apiInstance = new TeamDataAccessApplicationApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    try {
      FetchTeamDarApplications200Response result = apiInstance.fetchTeamDarApplications(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDataAccessApplicationApi#fetchTeamDarApplications");
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

### Return type

[**FetchTeamDarApplications200Response**](FetchTeamDarApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

