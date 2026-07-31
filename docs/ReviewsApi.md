# ReviewsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createReviews**](ReviewsApi.md#createReviews) | **POST** /api/v1/reviews | ReviewController@store |
| [**deleteReviews**](ReviewsApi.md#deleteReviews) | **DELETE** /api/v1/reviews/{id} | Delete a review |
| [**editReviews**](ReviewsApi.md#editReviews) | **PATCH** /api/v1/reviews/{id} | Edit a review |
| [**fetchAllReviews**](ReviewsApi.md#fetchAllReviews) | **GET** /api/v1/reviews | ReviewController@index |
| [**fetchReviews**](ReviewsApi.md#fetchReviews) | **GET** /api/v1/reviews/{id} | ReviewController@show |
| [**updateReviews**](ReviewsApi.md#updateReviews) | **PUT** /api/v1/reviews/{id} | Update a review |


<a id="createReviews"></a>
# **createReviews**
> CreateCategories200Response createReviews(createReviewsRequest)

ReviewController@store

Create a new review

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ReviewsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReviewsApi apiInstance = new ReviewsApi(defaultClient);
    CreateReviewsRequest createReviewsRequest = new CreateReviewsRequest(); // CreateReviewsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createReviews(createReviewsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReviewsApi#createReviews");
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
| **createReviewsRequest** | [**CreateReviewsRequest**](CreateReviewsRequest.md)| Pass user credentials | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

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

<a id="deleteReviews"></a>
# **deleteReviews**
> DeleteAliases200Response deleteReviews(id)

Delete a review

Delete a review

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ReviewsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReviewsApi apiInstance = new ReviewsApi(defaultClient);
    Integer id = 1; // Integer | review id
    try {
      DeleteAliases200Response result = apiInstance.deleteReviews(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReviewsApi#deleteReviews");
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
| **id** | **Integer**| review id | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

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

<a id="editReviews"></a>
# **editReviews**
> UpdateReviews200Response editReviews(id, createReviewsRequest)

Edit a review

Edit a review

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ReviewsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReviewsApi apiInstance = new ReviewsApi(defaultClient);
    Integer id = 1; // Integer | review id
    CreateReviewsRequest createReviewsRequest = new CreateReviewsRequest(); // CreateReviewsRequest | Pass user credentials
    try {
      UpdateReviews200Response result = apiInstance.editReviews(id, createReviewsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReviewsApi#editReviews");
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
| **id** | **Integer**| review id | |
| **createReviewsRequest** | [**CreateReviewsRequest**](CreateReviewsRequest.md)| Pass user credentials | |

### Return type

[**UpdateReviews200Response**](UpdateReviews200Response.md)

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

<a id="fetchAllReviews"></a>
# **fetchAllReviews**
> FetchAllReviews200Response fetchAllReviews()

ReviewController@index

Get All Reviews

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ReviewsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReviewsApi apiInstance = new ReviewsApi(defaultClient);
    try {
      FetchAllReviews200Response result = apiInstance.fetchAllReviews();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReviewsApi#fetchAllReviews");
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

[**FetchAllReviews200Response**](FetchAllReviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchReviews"></a>
# **fetchReviews**
> FetchAllReviews200Response fetchReviews(id)

ReviewController@show

Get review by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ReviewsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReviewsApi apiInstance = new ReviewsApi(defaultClient);
    Integer id = 1; // Integer | review id
    try {
      FetchAllReviews200Response result = apiInstance.fetchReviews(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReviewsApi#fetchReviews");
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
| **id** | **Integer**| review id | |

### Return type

[**FetchAllReviews200Response**](FetchAllReviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="updateReviews"></a>
# **updateReviews**
> UpdateReviews200Response updateReviews(id, createReviewsRequest)

Update a review

Update a review

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ReviewsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReviewsApi apiInstance = new ReviewsApi(defaultClient);
    Integer id = 1; // Integer | review id
    CreateReviewsRequest createReviewsRequest = new CreateReviewsRequest(); // CreateReviewsRequest | Pass user credentials
    try {
      UpdateReviews200Response result = apiInstance.updateReviews(id, createReviewsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReviewsApi#updateReviews");
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
| **id** | **Integer**| review id | |
| **createReviewsRequest** | [**CreateReviewsRequest**](CreateReviewsRequest.md)| Pass user credentials | |

### Return type

[**UpdateReviews200Response**](UpdateReviews200Response.md)

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

