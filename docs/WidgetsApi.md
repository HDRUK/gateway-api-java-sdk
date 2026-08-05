# WidgetsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createWidget**](WidgetsApi.md#createWidget) | **POST** /api/v1/teams/{teamId}/widgets | Create a new widget |
| [**deleteWidget**](WidgetsApi.md#deleteWidget) | **DELETE** /api/v1/teams/{teamId}/widgets/{id} | Delete a widget |
| [**fetchAllWidgets**](WidgetsApi.md#fetchAllWidgets) | **GET** /api/v1/teams/{teamId}/widgets | WidgetController@index |
| [**fetchWidget**](WidgetsApi.md#fetchWidget) | **GET** /api/v1/teams/{teamId}/widgets/{id} | WidgetController@retrieve |
| [**fetchWidgetDataSources**](WidgetsApi.md#fetchWidgetDataSources) | **GET** /api/v1/teams/{teamId}/widgets/data | WidgetController@getWidgetData |
| [**retrieveWidgetData**](WidgetsApi.md#retrieveWidgetData) | **GET** /api/v1/teams/{teamId}/widgets/{id}/data | Retrieve data related to a widget |
| [**trackWidgetEvent**](WidgetsApi.md#trackWidgetEvent) | **POST** /api/v1/teams/{teamId}/widgets/{id}/track | Record a widget analytics event |
| [**updateWidget**](WidgetsApi.md#updateWidget) | **PATCH** /api/v1/teams/{teamId}/widgets/{id} | Update an existing widget |
| [**widgetAnalytics**](WidgetsApi.md#widgetAnalytics) | **GET** /api/v1/teams/{teamId}/widgets/analytics | Get widget analytics for a team |


<a id="createWidget"></a>
# **createWidget**
> CreateWidget201Response createWidget(teamId, createWidgetRequest)

Create a new widget

Creates a new widget for a given team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 5; // Integer | Team ID the widget belongs to
    CreateWidgetRequest createWidgetRequest = new CreateWidgetRequest(); // CreateWidgetRequest | 
    try {
      CreateWidget201Response result = apiInstance.createWidget(teamId, createWidgetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#createWidget");
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
| **teamId** | **Integer**| Team ID the widget belongs to | |
| **createWidgetRequest** | [**CreateWidgetRequest**](CreateWidgetRequest.md)|  | |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Widget created successfully |  -  |
| **400** | Validation failed |  -  |
| **500** | Server error |  -  |

<a id="deleteWidget"></a>
# **deleteWidget**
> DeleteApplications200Response deleteWidget(teamId, id)

Delete a widget

Soft delete a widget belonging to a specific team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 5; // Integer | Team ID
    Integer id = 1; // Integer | Widget ID
    try {
      DeleteApplications200Response result = apiInstance.deleteWidget(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#deleteWidget");
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
| **teamId** | **Integer**| Team ID | |
| **id** | **Integer**| Widget ID | |

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
| **404** | Widget not found |  -  |
| **200** | Widget deleted successfully |  -  |
| **500** | Server error |  -  |

<a id="fetchAllWidgets"></a>
# **fetchAllWidgets**
> FetchAllWidgets200Response fetchAllWidgets(teamId)

WidgetController@index

Get All Widgets

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 56; // Integer | Team ID
    try {
      FetchAllWidgets200Response result = apiInstance.fetchAllWidgets(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#fetchAllWidgets");
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
| **teamId** | **Integer**| Team ID | |

### Return type

[**FetchAllWidgets200Response**](FetchAllWidgets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchWidget"></a>
# **fetchWidget**
> FetchWidget200Response fetchWidget(teamId, id)

WidgetController@retrieve

Get a single Widget

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 56; // Integer | Team ID
    Integer id = 56; // Integer | Widget ID
    try {
      FetchWidget200Response result = apiInstance.fetchWidget(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#fetchWidget");
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
| **teamId** | **Integer**| Team ID | |
| **id** | **Integer**| Widget ID | |

### Return type

[**FetchWidget200Response**](FetchWidget200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Widget not found |  -  |

<a id="fetchWidgetDataSources"></a>
# **fetchWidgetDataSources**
> FetchWidgetDataSources200Response fetchWidgetDataSources(teamId, teamIds)

WidgetController@getWidgetData

Fetch lightweight data (id, name, etc.) for multiple teams across datasets, tools, collections, and DURS

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 56; // Integer | Team ID
    String teamIds = "1,2,3"; // String | Comma-separated list of team IDs to filter data
    try {
      FetchWidgetDataSources200Response result = apiInstance.fetchWidgetDataSources(teamId, teamIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#fetchWidgetDataSources");
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
| **teamId** | **Integer**| Team ID | |
| **teamIds** | **String**| Comma-separated list of team IDs to filter data | |

### Return type

[**FetchWidgetDataSources200Response**](FetchWidgetDataSources200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Aggregated data retrieved successfully |  -  |
| **400** | Invalid or missing teamIds parameter |  -  |

<a id="retrieveWidgetData"></a>
# **retrieveWidgetData**
> RetrieveWidgetData200Response retrieveWidgetData(teamId, id, domainOrigin)

Retrieve data related to a widget

Fetches datasets, data uses, scripts, and collections linked to a widget

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 56; // Integer | Team ID
    Integer id = 56; // Integer | Widget ID
    String domainOrigin = "https://example.com"; // String | Optional domain URL to check against the widget's permitted_domains list
    try {
      RetrieveWidgetData200Response result = apiInstance.retrieveWidgetData(teamId, id, domainOrigin);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#retrieveWidgetData");
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
| **teamId** | **Integer**| Team ID | |
| **id** | **Integer**| Widget ID | |
| **domainOrigin** | **String**| Optional domain URL to check against the widget&#39;s permitted_domains list | |

### Return type

[**RetrieveWidgetData200Response**](RetrieveWidgetData200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **403** | Forbidden — domain not permitted for this widget |  -  |
| **200** | Widget data retrieved successfully |  -  |
| **404** | Widget not found |  -  |

<a id="trackWidgetEvent"></a>
# **trackWidgetEvent**
> trackWidgetEvent(teamId, id, trackWidgetEventRequest)

Record a widget analytics event

Public endpoint for frontend clients to record user interactions with a widget (page views, code copies, gateway clicks, searches). No authentication required.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 56; // Integer | 
    Integer id = 56; // Integer | 
    TrackWidgetEventRequest trackWidgetEventRequest = new TrackWidgetEventRequest(); // TrackWidgetEventRequest | 
    try {
      apiInstance.trackWidgetEvent(teamId, id, trackWidgetEventRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#trackWidgetEvent");
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
| **teamId** | **Integer**|  | |
| **id** | **Integer**|  | |
| **trackWidgetEventRequest** | [**TrackWidgetEventRequest**](TrackWidgetEventRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Event recorded |  -  |
| **404** | Widget not found |  -  |
| **422** | Validation error |  -  |

<a id="updateWidget"></a>
# **updateWidget**
> UpdateWidget200Response updateWidget(teamId, id, updateWidgetRequest)

Update an existing widget

Updates an existing widget for a given team ID

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 1; // Integer | Team ID
    Integer id = 12; // Integer | Widget ID
    UpdateWidgetRequest updateWidgetRequest = new UpdateWidgetRequest(); // UpdateWidgetRequest | 
    try {
      UpdateWidget200Response result = apiInstance.updateWidget(teamId, id, updateWidgetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#updateWidget");
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
| **teamId** | **Integer**| Team ID | |
| **id** | **Integer**| Widget ID | |
| **updateWidgetRequest** | [**UpdateWidgetRequest**](UpdateWidgetRequest.md)|  | [optional] |

### Return type

[**UpdateWidget200Response**](UpdateWidget200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Widget successfully updated |  -  |
| **404** | Widget not found |  -  |
| **500** | Internal server error |  -  |

<a id="widgetAnalytics"></a>
# **widgetAnalytics**
> WidgetAnalytics200Response widgetAnalytics(teamId, from, to, groupBy)

Get widget analytics for a team

Returns aggregated event counts per widget, per event type, and over time. Supports date range filtering and time-based grouping.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.WidgetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WidgetsApi apiInstance = new WidgetsApi(defaultClient);
    Integer teamId = 56; // Integer | 
    String from = "2026-01-01"; // String | Start date (Y-m-d)
    String to = "2026-06-30"; // String | End date (Y-m-d)
    String groupBy = "day"; // String | Time granularity
    try {
      WidgetAnalytics200Response result = apiInstance.widgetAnalytics(teamId, from, to, groupBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WidgetsApi#widgetAnalytics");
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
| **teamId** | **Integer**|  | |
| **from** | **String**| Start date (Y-m-d) | [optional] |
| **to** | **String**| End date (Y-m-d) | [optional] |
| **groupBy** | **String**| Time granularity | [optional] [default to day] [enum: day, week, month] |

### Return type

[**WidgetAnalytics200Response**](WidgetAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Analytics data |  -  |

