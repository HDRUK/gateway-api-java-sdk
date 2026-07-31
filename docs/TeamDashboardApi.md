# TeamDashboardApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchCollectionsViewsV3**](TeamDashboardApi.md#fetchCollectionsViewsV3) | **GET** /api/v3/teams/{id}/dashboard/collections/views | TeamDashboardController@collectionViews |
| [**fetchDarApplicationsApplicationTimelineV3**](TeamDashboardApi.md#fetchDarApplicationsApplicationTimelineV3) | **GET** /api/v3/teams/{id}/dar/dashboard/timeline | DataAccessDashboardController@getApplicationTimeline |
| [**fetchDarApplicationsAverageTimeToApprovalV3**](TeamDashboardApi.md#fetchDarApplicationsAverageTimeToApprovalV3) | **GET** /api/v3/teams/{id}/dar/dashboard/average-time | DataAccessDashboardController@getAverageTimeToApproval |
| [**fetchDarApplicationsCurrentStatusV3**](TeamDashboardApi.md#fetchDarApplicationsCurrentStatusV3) | **GET** /api/v3/teams/{id}/dar/dashboard/status | DataAccessDashboardController@getApplicationStatus |
| [**fetchDarApplicationsDashboardExportCsvV3**](TeamDashboardApi.md#fetchDarApplicationsDashboardExportCsvV3) | **GET** /api/v3/teams/{id}/dar/dashboard/export/csv | DataAccessDashboardController@exportDashboardCsv |
| [**fetchDarApplicationsDashboardRequiredActionsExportCsvV3**](TeamDashboardApi.md#fetchDarApplicationsDashboardRequiredActionsExportCsvV3) | **GET** /api/v3/teams/{id}/dar/dashboard/required-actions/export/csv | DataAccessDashboardController@exportRequiredActionsCsv |
| [**fetchDarApplicationsDashboardTimelineExportCsvV3**](TeamDashboardApi.md#fetchDarApplicationsDashboardTimelineExportCsvV3) | **GET** /api/v3/teams/{id}/dar/dashboard/timeline/export/csv | DataAccessDashboardController@exportDashboardTimelineCsv |
| [**fetchDarApplicationsRequiredActionsV3**](TeamDashboardApi.md#fetchDarApplicationsRequiredActionsV3) | **GET** /api/v3/teams/{id}/dar/dashboard/required-actions | DataAccessDashboardController@getRequiredActions |
| [**fetchDarMyApplicationsV3**](TeamDashboardApi.md#fetchDarMyApplicationsV3) | **GET** /api/v3/teams/{id}/dar/dashboard/count | DataAccessDashboardController@getMyApplications |
| [**fetchDashboardDownloadCsvV3**](TeamDashboardApi.md#fetchDashboardDownloadCsvV3) | **GET** /api/v3/teams/{id}/dashboard/download/csv | TeamDashboardController@downloadCsv |
| [**fetchDataCustodiansViewsV3**](TeamDashboardApi.md#fetchDataCustodiansViewsV3) | **GET** /api/v3/teams/{id}/dashboard/datacustodians/views | TeamDashboardController@datacustodianViews |
| [**fetchDatasetViews360V3**](TeamDashboardApi.md#fetchDatasetViews360V3) | **GET** /api/v3/teams/{id}/dashboard/datasets/views/360 | TeamDashboardController@datasetViews360 |
| [**fetchDatasetViewsTopV3**](TeamDashboardApi.md#fetchDatasetViewsTopV3) | **GET** /api/v3/teams/{id}/dashboard/datasets/views/top | TeamDashboardController@datasetViewsTop |
| [**fetchEntitiesCountV3**](TeamDashboardApi.md#fetchEntitiesCountV3) | **GET** /api/v3/teams/{id}/dashboard/{entity}/count | TeamDashboardController@entityCount |


<a id="fetchCollectionsViewsV3"></a>
# **fetchCollectionsViewsV3**
> FetchCollectionsViewsV3200Response fetchCollectionsViewsV3(id, startDate, endDate)

TeamDashboardController@collectionViews

Get count of a collection views for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      FetchCollectionsViewsV3200Response result = apiInstance.fetchCollectionsViewsV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchCollectionsViewsV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**FetchCollectionsViewsV3200Response**](FetchCollectionsViewsV3200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsApplicationTimelineV3"></a>
# **fetchDarApplicationsApplicationTimelineV3**
> CreateWidget201Response fetchDarApplicationsApplicationTimelineV3(id, startDate, endDate)

DataAccessDashboardController@getApplicationTimeline

Get Dar applications timeline for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsApplicationTimelineV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsApplicationTimelineV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsAverageTimeToApprovalV3"></a>
# **fetchDarApplicationsAverageTimeToApprovalV3**
> CreateWidget201Response fetchDarApplicationsAverageTimeToApprovalV3(id, startDate, endDate)

DataAccessDashboardController@getAverageTimeToApproval

Get Dar applications average time to approval for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsAverageTimeToApprovalV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsAverageTimeToApprovalV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsCurrentStatusV3"></a>
# **fetchDarApplicationsCurrentStatusV3**
> CreateWidget201Response fetchDarApplicationsCurrentStatusV3(id, startDate, endDate)

DataAccessDashboardController@getApplicationStatus

Get Dar applications current status for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsCurrentStatusV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsCurrentStatusV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsDashboardExportCsvV3"></a>
# **fetchDarApplicationsDashboardExportCsvV3**
> CreateWidget201Response fetchDarApplicationsDashboardExportCsvV3(id, startDate, endDate)

DataAccessDashboardController@exportDashboardCsv

Get Dar applications dashboard export csv for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsDashboardExportCsvV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsDashboardExportCsvV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsDashboardRequiredActionsExportCsvV3"></a>
# **fetchDarApplicationsDashboardRequiredActionsExportCsvV3**
> CreateWidget201Response fetchDarApplicationsDashboardRequiredActionsExportCsvV3(id)

DataAccessDashboardController@exportRequiredActionsCsv

Get Dar applications dashboard timeline export csv for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsDashboardRequiredActionsExportCsvV3(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsDashboardRequiredActionsExportCsvV3");
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
| **id** | **Integer**| Team ID | |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsDashboardTimelineExportCsvV3"></a>
# **fetchDarApplicationsDashboardTimelineExportCsvV3**
> CreateWidget201Response fetchDarApplicationsDashboardTimelineExportCsvV3(id, startDate, endDate)

DataAccessDashboardController@exportDashboardTimelineCsv

Get Dar applications dashboard timeline export csv for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsDashboardTimelineExportCsvV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsDashboardTimelineExportCsvV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarApplicationsRequiredActionsV3"></a>
# **fetchDarApplicationsRequiredActionsV3**
> CreateWidget201Response fetchDarApplicationsRequiredActionsV3(id, startDate, endDate)

DataAccessDashboardController@getRequiredActions

Get Dar applications required actions for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarApplicationsRequiredActionsV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarApplicationsRequiredActionsV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDarMyApplicationsV3"></a>
# **fetchDarMyApplicationsV3**
> CreateWidget201Response fetchDarMyApplicationsV3(id, startDate, endDate)

DataAccessDashboardController@getMyApplications

Get Dar applications for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      CreateWidget201Response result = apiInstance.fetchDarMyApplicationsV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDarMyApplicationsV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**CreateWidget201Response**](CreateWidget201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDashboardDownloadCsvV3"></a>
# **fetchDashboardDownloadCsvV3**
> File fetchDashboardDownloadCsvV3(id, startDate, endDate)

TeamDashboardController@downloadCsv

Download dashboard data custodian in csv format

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      File result = apiInstance.fetchDashboardDownloadCsvV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDashboardDownloadCsvV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**File**](File.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/csv, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | CSV file download containing dashboard metrics for the team |  -  |
| **400** | Invalid team ID |  -  |
| **500** | Invalid date interval |  -  |

<a id="fetchDataCustodiansViewsV3"></a>
# **fetchDataCustodiansViewsV3**
> FetchCollectionsViewsV3200Response fetchDataCustodiansViewsV3(id, startDate, endDate)

TeamDashboardController@datacustodianViews

Get count of a data custodian views for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      FetchCollectionsViewsV3200Response result = apiInstance.fetchDataCustodiansViewsV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDataCustodiansViewsV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**FetchCollectionsViewsV3200Response**](FetchCollectionsViewsV3200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDatasetViews360V3"></a>
# **fetchDatasetViews360V3**
> FetchDatasetViews360V3200Response fetchDatasetViews360V3(id, startDate, endDate)

TeamDashboardController@datasetViews360

Get count of a datasets views 360 for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      FetchDatasetViews360V3200Response result = apiInstance.fetchDatasetViews360V3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDatasetViews360V3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**FetchDatasetViews360V3200Response**](FetchDatasetViews360V3200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchDatasetViewsTopV3"></a>
# **fetchDatasetViewsTopV3**
> FetchDatasetViewsTopV3200Response fetchDatasetViewsTopV3(id, startDate, endDate)

TeamDashboardController@datasetViewsTop

Get count of a datasets views top for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      FetchDatasetViewsTopV3200Response result = apiInstance.fetchDatasetViewsTopV3(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchDatasetViewsTopV3");
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
| **id** | **Integer**| Team ID | |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**FetchDatasetViewsTopV3200Response**](FetchDatasetViewsTopV3200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="fetchEntitiesCountV3"></a>
# **fetchEntitiesCountV3**
> FetchEntitiesCountV3200Response fetchEntitiesCountV3(id, entity, startDate, endDate)

TeamDashboardController@entityCount

Get count of a specific entity for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.TeamDashboardApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TeamDashboardApi apiInstance = new TeamDashboardApi(defaultClient);
    Integer id = 1; // Integer | Team ID
    String entity = "datasets"; // String | Entity type to count
    LocalDate startDate = LocalDate.parse("Mon Jan 01 00:00:00 UTC 2024"); // LocalDate | Start date for the reporting interval (Y-m-d). Defaults to one year ago.
    LocalDate endDate = LocalDate.parse("Tue Dec 31 00:00:00 UTC 2024"); // LocalDate | End date for the reporting interval (Y-m-d). Defaults to today.
    try {
      FetchEntitiesCountV3200Response result = apiInstance.fetchEntitiesCountV3(id, entity, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TeamDashboardApi#fetchEntitiesCountV3");
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
| **id** | **Integer**| Team ID | |
| **entity** | **String**| Entity type to count | [enum: datasets, datauses, tools, collections, general-enquires, fesability-enquires, data-access-requests] |
| **startDate** | **LocalDate**| Start date for the reporting interval (Y-m-d). Defaults to one year ago. | [optional] |
| **endDate** | **LocalDate**| End date for the reporting interval (Y-m-d). Defaults to today. | [optional] |

### Return type

[**FetchEntitiesCountV3200Response**](FetchEntitiesCountV3200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

