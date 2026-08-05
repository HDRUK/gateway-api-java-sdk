# TeamFederationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createFederationTeam**](TeamFederationsApi.md#createFederationTeam) | **POST** /api/v1/teams/{teamId}/federations | FederationController@store |
| [**deleteFederation**](TeamFederationsApi.md#deleteFederation) | **DELETE** /api/v1/teams/{teamId}/federations/{federationId} | FederationController@destroy |
| [**editFederationTeam**](TeamFederationsApi.md#editFederationTeam) | **PATCH** /api/v1/teams/{teamId}/federations/{federationId} | FederationController@edit |
| [**getFederationByFederationIdAndTeamId**](TeamFederationsApi.md#getFederationByFederationIdAndTeamId) | **GET** /api/v1/teams/{teamId}/federations/{federationId} | FederationController@show |
| [**getFederationHistory**](TeamFederationsApi.md#getFederationHistory) | **GET** /api/v1/teams/{teamId}/federations/{federationId}/history | FederationController@history |
| [**getFederationTeamId**](TeamFederationsApi.md#getFederationTeamId) | **GET** /api/v1/teams/{teamId}/federations | FederationController@index |
| [**runFederation**](TeamFederationsApi.md#runFederation) | **GET** /api/v1/teams/{teamId}/federations/{federationId}/run | FederationController@runNow |
| [**testFederation**](TeamFederationsApi.md#testFederation) | **POST** /api/v1/teams/{teamId}/federations/test | FederationController@testFederation |
| [**updateFederationTeam**](TeamFederationsApi.md#updateFederationTeam) | **PUT** /api/v1/teams/{teamId}/federations/{federationId} | FederationController@update |


<a id="createFederationTeam"></a>
# **createFederationTeam**
> CreateDarIntegration201Response createFederationTeam(teamId, createFederationTeamRequest)

FederationController@store

Create federation

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    CreateFederationTeamRequest createFederationTeamRequest = new CreateFederationTeamRequest(); // CreateFederationTeamRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createFederationTeam(teamId, createFederationTeamRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#createFederationTeam");
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
| **teamId** | **Integer**| team id | |
| **createFederationTeamRequest** | [**CreateFederationTeamRequest**](CreateFederationTeamRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteFederation"></a>
# **deleteFederation**
> DeleteFederation200Response deleteFederation(teamId, federationId)

FederationController@destroy

Delete federation for team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer federationId = 1; // Integer | federation id
    try {
      DeleteFederation200Response result = apiInstance.deleteFederation(teamId, federationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#deleteFederation");
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
| **teamId** | **Integer**| team id | |
| **federationId** | **Integer**| federation id | |

### Return type

[**DeleteFederation200Response**](DeleteFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Error response |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="editFederationTeam"></a>
# **editFederationTeam**
> CreateDarIntegration201Response editFederationTeam(teamId, federationId, createFederationTeamRequest)

FederationController@edit

Edit federation for team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer federationId = 1; // Integer | federation id
    CreateFederationTeamRequest createFederationTeamRequest = new CreateFederationTeamRequest(); // CreateFederationTeamRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.editFederationTeam(teamId, federationId, createFederationTeamRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#editFederationTeam");
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
| **teamId** | **Integer**| team id | |
| **federationId** | **Integer**| federation id | |
| **createFederationTeamRequest** | [**CreateFederationTeamRequest**](CreateFederationTeamRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="getFederationByFederationIdAndTeamId"></a>
# **getFederationByFederationIdAndTeamId**
> GetFederationByFederationIdAndTeamId200Response getFederationByFederationIdAndTeamId(teamId, federationId)

FederationController@show

Get federation by federation id from team id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer federationId = 1; // Integer | federation id
    try {
      GetFederationByFederationIdAndTeamId200Response result = apiInstance.getFederationByFederationIdAndTeamId(teamId, federationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#getFederationByFederationIdAndTeamId");
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
| **teamId** | **Integer**| team id | |
| **federationId** | **Integer**| federation id | |

### Return type

[**GetFederationByFederationIdAndTeamId200Response**](GetFederationByFederationIdAndTeamId200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="getFederationHistory"></a>
# **getFederationHistory**
> GetFederationHistory200Response getFederationHistory(teamId, federationId, perPage)

FederationController@history

Get run history for a federation

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer federationId = 1; // Integer | federation id
    Integer perPage = 25; // Integer | per page
    try {
      GetFederationHistory200Response result = apiInstance.getFederationHistory(teamId, federationId, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#getFederationHistory");
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
| **teamId** | **Integer**| team id | |
| **federationId** | **Integer**| federation id | |
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**GetFederationHistory200Response**](GetFederationHistory200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="getFederationTeamId"></a>
# **getFederationTeamId**
> GetFederationTeamId200Response getFederationTeamId(teamId)

FederationController@index

Get federations by team id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    try {
      GetFederationTeamId200Response result = apiInstance.getFederationTeamId(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#getFederationTeamId");
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
| **teamId** | **Integer**| team id | |

### Return type

[**GetFederationTeamId200Response**](GetFederationTeamId200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="runFederation"></a>
# **runFederation**
> TestFederation200Response runFederation(teamId, federationId)

FederationController@runNow

Run federation immediately

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer federationId = 1; // Integer | federation id
    try {
      TestFederation200Response result = apiInstance.runFederation(teamId, federationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#runFederation");
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
| **teamId** | **Integer**| team id | |
| **federationId** | **Integer**| federation id | |

### Return type

[**TestFederation200Response**](TestFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="testFederation"></a>
# **testFederation**
> TestFederation200Response testFederation(teamId)

FederationController@testFederation

Test federation configuration

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    try {
      TestFederation200Response result = apiInstance.testFederation(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#testFederation");
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
| **teamId** | **Integer**| team id | |

### Return type

[**TestFederation200Response**](TestFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="updateFederationTeam"></a>
# **updateFederationTeam**
> CreateDarIntegration201Response updateFederationTeam(teamId, federationId, updateFederationTeamRequest)

FederationController@update

Update federation for team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamFederationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TeamFederationsApi apiInstance = new TeamFederationsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer federationId = 1; // Integer | federation id
    UpdateFederationTeamRequest updateFederationTeamRequest = new UpdateFederationTeamRequest(); // UpdateFederationTeamRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.updateFederationTeam(teamId, federationId, updateFederationTeamRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamFederationsApi#updateFederationTeam");
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
| **teamId** | **Integer**| team id | |
| **federationId** | **Integer**| federation id | |
| **updateFederationTeamRequest** | [**UpdateFederationTeamRequest**](UpdateFederationTeamRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

