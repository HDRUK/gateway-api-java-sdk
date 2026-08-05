# DataAccessApplicationReviewApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTeamDarApplicationQuestionReview**](DataAccessApplicationReviewApi.md#createTeamDarApplicationQuestionReview) | **POST** /api/v1/teams/{team_id}/dar/applications/{id}/questions/{questionId}/reviews | DataAccessApplicationReview@store |
| [**createTeamDarApplicationReview**](DataAccessApplicationReviewApi.md#createTeamDarApplicationReview) | **POST** /api/v1/teams/{team_id}/dar/applications/{id}/reviews | DataAccessApplicationReview@storeGlobal |
| [**deleteTeamDarApplicationQuestionReview**](DataAccessApplicationReviewApi.md#deleteTeamDarApplicationQuestionReview) | **DELETE** /api/v1/teams/{team_id}/dar/applications/{id}/questions/{questionId}/reviews/{reviewId} | DataAccessApplicationReview@destroy |
| [**deleteTeamDarApplicationReview**](DataAccessApplicationReviewApi.md#deleteTeamDarApplicationReview) | **DELETE** /api/v1/teams/{team_id}/dar/applications/{id}/reviews/{reviewId} | DataAccessApplicationReview@destroyGlobal |
| [**deleteTeamDarApplicationReviewFile**](DataAccessApplicationReviewApi.md#deleteTeamDarApplicationReviewFile) | **DELETE** /api/v1/teams/{teamId}/dar/applications/{id}/reviews/{reviewId}/files/{fileId} | DataAccessApplicationReview@destroyFile |
| [**fetchTeamDarApplicationReviewFile**](DataAccessApplicationReviewApi.md#fetchTeamDarApplicationReviewFile) | **GET** /api/v1/teams/{teamId}/dar/applications/{id}/reviews/{reviewId}/download/{fileId} | DataAccessApplicationReview@downloadFile |
| [**fetchTeamDarApplicationReviews**](DataAccessApplicationReviewApi.md#fetchTeamDarApplicationReviews) | **GET** /api/v1/teams/{team_id}/dar/applications/{id}/reviews | DataAccessApplicationReview@index |
| [**updateTeamDarApplicationQuestionReview**](DataAccessApplicationReviewApi.md#updateTeamDarApplicationQuestionReview) | **PUT** /api/v1/teams/{team_id}/dar/applications/{id}/questions/{questionId}/reviews/{reviewId} | DataAccessApplicationReview@update |
| [**updateTeamDarApplicationReview**](DataAccessApplicationReviewApi.md#updateTeamDarApplicationReview) | **PUT** /api/v1/teams/{team_id}/dar/applications/{id}/reviews/{reviewId} | DataAccessApplicationReview@updateGlobal |


<a id="createTeamDarApplicationQuestionReview"></a>
# **createTeamDarApplicationQuestionReview**
> CreateDarIntegration201Response createTeamDarApplicationQuestionReview(teamId, id, questionId, createTeamDarApplicationReviewRequest)

DataAccessApplicationReview@store

Create a new review comment on a question in a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer questionId = 1; // Integer | DAR application question id
    CreateTeamDarApplicationReviewRequest createTeamDarApplicationReviewRequest = new CreateTeamDarApplicationReviewRequest(); // CreateTeamDarApplicationReviewRequest | DataAccessApplicationReview definition
    try {
      CreateDarIntegration201Response result = apiInstance.createTeamDarApplicationQuestionReview(teamId, id, questionId, createTeamDarApplicationReviewRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#createTeamDarApplicationQuestionReview");
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
| **questionId** | **Integer**| DAR application question id | |
| **createTeamDarApplicationReviewRequest** | [**CreateTeamDarApplicationReviewRequest**](CreateTeamDarApplicationReviewRequest.md)| DataAccessApplicationReview definition | |

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
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="createTeamDarApplicationReview"></a>
# **createTeamDarApplicationReview**
> CreateDarIntegration201Response createTeamDarApplicationReview(teamId, id, createTeamDarApplicationReviewRequest)

DataAccessApplicationReview@storeGlobal

Create a new review comment on a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    CreateTeamDarApplicationReviewRequest createTeamDarApplicationReviewRequest = new CreateTeamDarApplicationReviewRequest(); // CreateTeamDarApplicationReviewRequest | DataAccessApplicationReview definition
    try {
      CreateDarIntegration201Response result = apiInstance.createTeamDarApplicationReview(teamId, id, createTeamDarApplicationReviewRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#createTeamDarApplicationReview");
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
| **createTeamDarApplicationReviewRequest** | [**CreateTeamDarApplicationReviewRequest**](CreateTeamDarApplicationReviewRequest.md)| DataAccessApplicationReview definition | |

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
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteTeamDarApplicationQuestionReview"></a>
# **deleteTeamDarApplicationQuestionReview**
> DeleteApplications200Response deleteTeamDarApplicationQuestionReview(teamId, id, questionId, reviewId)

DataAccessApplicationReview@destroy

Delete a review from a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer questionId = 1; // Integer | DAR application question id
    Integer reviewId = 1; // Integer | DAR application review id
    try {
      DeleteApplications200Response result = apiInstance.deleteTeamDarApplicationQuestionReview(teamId, id, questionId, reviewId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#deleteTeamDarApplicationQuestionReview");
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
| **questionId** | **Integer**| DAR application question id | |
| **reviewId** | **Integer**| DAR application review id | |

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
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteTeamDarApplicationReview"></a>
# **deleteTeamDarApplicationReview**
> DeleteApplications200Response deleteTeamDarApplicationReview(teamId, id, reviewId)

DataAccessApplicationReview@destroyGlobal

Delete a review from a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer reviewId = 1; // Integer | DAR application review id
    try {
      DeleteApplications200Response result = apiInstance.deleteTeamDarApplicationReview(teamId, id, reviewId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#deleteTeamDarApplicationReview");
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
| **reviewId** | **Integer**| DAR application review id | |

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
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteTeamDarApplicationReviewFile"></a>
# **deleteTeamDarApplicationReviewFile**
> DeleteApplications200Response deleteTeamDarApplicationReviewFile(teamId, id, reviewId, fileId)

DataAccessApplicationReview@destroyFile

Delete a file associated with a DAR review

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | Dar application id
    Integer reviewId = 1; // Integer | Review id
    String fileId = "1"; // String | File uuid
    try {
      DeleteApplications200Response result = apiInstance.deleteTeamDarApplicationReviewFile(teamId, id, reviewId, fileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#deleteTeamDarApplicationReviewFile");
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
| **id** | **Integer**| Dar application id | |
| **reviewId** | **Integer**| Review id | |
| **fileId** | **String**| File uuid | |

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
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="fetchTeamDarApplicationReviewFile"></a>
# **fetchTeamDarApplicationReviewFile**
> fetchTeamDarApplicationReviewFile(teamId, id, reviewId, fileId)

DataAccessApplicationReview@downloadFile

Download a file associated with a DAR application review

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer reviewId = 1; // Integer | DAR application review id
    String fileId = "1"; // String | File uuid
    try {
      apiInstance.fetchTeamDarApplicationReviewFile(teamId, id, reviewId, fileId);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#fetchTeamDarApplicationReviewFile");
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
| **reviewId** | **Integer**| DAR application review id | |
| **fileId** | **String**| File uuid | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: file, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchTeamDarApplicationReviews"></a>
# **fetchTeamDarApplicationReviews**
> FetchTeamDarApplicationReviews200Response fetchTeamDarApplicationReviews(teamId, id)

DataAccessApplicationReview@index

Return all reviews on a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplicationReviews200Response result = apiInstance.fetchTeamDarApplicationReviews(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#fetchTeamDarApplicationReviews");
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

[**FetchTeamDarApplicationReviews200Response**](FetchTeamDarApplicationReviews200Response.md)

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

<a id="updateTeamDarApplicationQuestionReview"></a>
# **updateTeamDarApplicationQuestionReview**
> UpdateTeamDarApplicationQuestionReview200Response updateTeamDarApplicationQuestionReview(teamId, id, questionId, reviewId, createTeamDarApplicationReviewRequest)

DataAccessApplicationReview@update

Update a review comment on a question in a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer questionId = 1; // Integer | DAR application question id
    Integer reviewId = 1; // Integer | DAR application review id
    CreateTeamDarApplicationReviewRequest createTeamDarApplicationReviewRequest = new CreateTeamDarApplicationReviewRequest(); // CreateTeamDarApplicationReviewRequest | DataAccessApplicationReview definition
    try {
      UpdateTeamDarApplicationQuestionReview200Response result = apiInstance.updateTeamDarApplicationQuestionReview(teamId, id, questionId, reviewId, createTeamDarApplicationReviewRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#updateTeamDarApplicationQuestionReview");
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
| **questionId** | **Integer**| DAR application question id | |
| **reviewId** | **Integer**| DAR application review id | |
| **createTeamDarApplicationReviewRequest** | [**CreateTeamDarApplicationReviewRequest**](CreateTeamDarApplicationReviewRequest.md)| DataAccessApplicationReview definition | |

### Return type

[**UpdateTeamDarApplicationQuestionReview200Response**](UpdateTeamDarApplicationQuestionReview200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="updateTeamDarApplicationReview"></a>
# **updateTeamDarApplicationReview**
> UpdateTeamDarApplicationQuestionReview200Response updateTeamDarApplicationReview(teamId, id, reviewId, createTeamDarApplicationReviewRequest)

DataAccessApplicationReview@updateGlobal

Update a review comment on a DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataAccessApplicationReviewApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataAccessApplicationReviewApi apiInstance = new DataAccessApplicationReviewApi(defaultClient);
    Integer teamId = 1; // Integer | Team id
    Integer id = 1; // Integer | DAR application id
    Integer reviewId = 1; // Integer | DAR application review id
    CreateTeamDarApplicationReviewRequest createTeamDarApplicationReviewRequest = new CreateTeamDarApplicationReviewRequest(); // CreateTeamDarApplicationReviewRequest | DataAccessApplicationReview definition
    try {
      UpdateTeamDarApplicationQuestionReview200Response result = apiInstance.updateTeamDarApplicationReview(teamId, id, reviewId, createTeamDarApplicationReviewRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataAccessApplicationReviewApi#updateTeamDarApplicationReview");
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
| **reviewId** | **Integer**| DAR application review id | |
| **createTeamDarApplicationReviewRequest** | [**CreateTeamDarApplicationReviewRequest**](CreateTeamDarApplicationReviewRequest.md)| DataAccessApplicationReview definition | |

### Return type

[**UpdateTeamDarApplicationQuestionReview200Response**](UpdateTeamDarApplicationQuestionReview200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

