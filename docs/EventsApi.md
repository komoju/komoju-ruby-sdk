# Komoju::EventsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_events**](EventsApi.md#list_events) | **GET** /events | Event: List |
| [**show_event**](EventsApi.md#show_event) | **GET** /events/{id} | Event Show |

## Request Models



## list_events

> <EventList> list_events(opts)

Event: List

Lists out past webhook events from most-recent to least-recent.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::EventsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56 # Integer | Page number to query for.
}

begin
  # Event: List
  result = api_instance.list_events(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling EventsApi->list_events: #{e}"
end
```

#### Using the list_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EventList>, Integer, Hash)> list_events_with_http_info(opts)

```ruby
begin
  # Event: List
  data, status_code, headers = api_instance.list_events_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EventList>
rescue Komoju::ApiError => e
  puts "Error when calling EventsApi->list_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |

### Return type

[**EventList**](EventList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_event

> <Event> show_event(id)

Event Show

View an event given an `id`. Event `id`s can be saved from a webhook or found by querying all events.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::EventsApi.new
id = 'id_example' # String | A unique identifier for an event.

begin
  # Event Show
  result = api_instance.show_event(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling EventsApi->show_event: #{e}"
end
```

#### Using the show_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Event>, Integer, Hash)> show_event_with_http_info(id)

```ruby
begin
  # Event Show
  data, status_code, headers = api_instance.show_event_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Event>
rescue Komoju::ApiError => e
  puts "Error when calling EventsApi->show_event_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for an event. |  |

### Return type

[**Event**](Event.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

