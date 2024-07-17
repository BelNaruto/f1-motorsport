# F1 Motorsport Data API

The **F1 Motorsport Data API** provides comprehensive access to real-time and historical data from the world of Formula 1 racing. Perfect for developers and motorsport enthusiasts, this API allows for seamless integration of race statistics, driver information, team data, and more into your applications. This API can be found on [RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/f1-motorsport-data)

## Key Features

- **Live Race Data**: Access real-time updates during races, including lap times and positions.
- **Driver and Team Information**: Retrieve detailed statistics and profiles for drivers and teams, including standings and performance metrics.
- **Race Schedule**: Get information on upcoming races, including dates, locations, and formats.
- **Historical Data**: Access past race results and historical statistics for in-depth analysis.

## Getting Started

1. **Sign Up**: Create an account on RapidAPI.
2. **Subscribe**: Choose a subscription plan that meets your needs.
3. **API Key**: Obtain your unique API key to begin making requests.
4. **Documentation**: For detailed usage instructions, visit the [F1 Motorsport Data API Documentation](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/f1-motorsport-data).


## Driver Information Endpoint

### Description
This endpoint retrieves information about a specific athlete. The athlete ID can be obtained from other endpoints such as schedule, standings, or the ESPN website.

### Endpoint
`GET /athlete-info`

### Query Parameters
- `athleteId` (optional): The ID of the athlete (defaults to '4665').

### Conditional Request Headers
- `If-None-Match`: Allows conditional retrieval based on the provided entity tag.

### Response
The endpoint returns a JSON object containing information about the specified athlete.

### Caching
- Cached data is stored using a unique key derived from the athlete ID.
- Data is cached for 1 hour (in seconds) to reduce API requests and improve performance.

### Error Handling
If an error occurs during data retrieval, the endpoint responds with a 500 status code along with an error message indicating the issue. Users are advised to retry later or adjust the query parameters.


## Race Results Endpoint

### Description
This endpoint retrieves race results for a specific driver in a given year. It allows cross-origin requests by setting the appropriate headers. If the requested data is available in the cache, it serves the response from the cache to optimize performance. Otherwise, it fetches the data, caches it for future use, and returns it.

### Endpoint
`GET /race-results`

### Query Parameters
- `driverId` (optional): The ID of the driver (defaults to '4665').
- `year` (optional): The year of the race (defaults to '2024').

### Response
The endpoint returns a JSON object containing race results for the specified driver and year.

### Caching
- The data fetched from the API is cached using a unique key derived from the request parameters.
- Cached data is stored for 1 hour (in seconds) to reduce API requests and improve response time.

### Error Handling
If an error occurs during the data retrieval process, the endpoint returns a 500 status code along with an error message indicating the issue. Users are advised to try again later or adjust the query parameters.


## Driver Statistics Endpoint

### Description
This endpoint retrieves statistics for a specific Formula 1 driver. It enables cross-origin requests by setting the necessary headers. Cached data is utilized if available to optimize response time. Otherwise, it fetches the data from the source, caches it, and returns the response.

### Endpoint
`GET /stats`

### Query Parameters
- `driverId` (optional): The ID of the driver (defaults to '4665').

### Response
The endpoint returns a JSON object containing statistics for the specified driver.

### Caching
- The fetched data is cached using a unique key derived from the driver ID.
- Cached data is retained for 1 hour (in seconds) to minimize API requests and improve performance.

### Error Handling
In case of an error during data retrieval, the endpoint responds with a 500 status code along with an error message indicating the issue. Users are advised to retry later or adjust the query parameters.



## This endpoint retrieves current F1 News

Parameters:
limit (Default: 25)

## Current Scoreboard

This endpoint retrieves current scoreboard


## F1 Race Report

This endpoint retrieves F1 Race Report

Parameters:
eventId (* required)

### Note: This eventId is the same as the race id. You can get it on ESPN or make some calls to schedule and get the id...

## Standings by Controllers

Get Standings by Controllers

Parameters:
year (Format YYYY)


## Standings by Drivers

This endpoint retrieves Standings by Drivers

Parameters:
year (Format YYYY)


## F1 Schedule

This endpoint gets f1 schedule

Parameters:
year (Format YYYY)

## Driver Photos Endpoint

### Description
This endpoint retrieves photos for a specific Formula 1 driver. It allows cross-origin requests by setting the required headers. Cached data is utilized if available to enhance response efficiency. If the requested data is not cached, it is fetched from the source, cached, and then returned.

### Endpoint
`GET /photos`

### Query Parameters
- `driverId` (optional): The ID of the driver (defaults to '4665').
- `page` (optional): The page number for paginated results (defaults to '1').

### Response
The endpoint returns a JSON object containing photos for the specified driver.

### Caching
- Cached data is stored using a unique key generated from the combination of driver ID and page number.
- Data is cached for 1 hour (in seconds) to minimize API calls and optimize performance.

### Error Handling
In the event of an error during data retrieval, the endpoint responds with a 500 status code along with an error message indicating the issue. Users are advised to retry later or adjust the query parameters.

## Commonly Asked Questions

### 1. What kind of data can I access through the F1 Motorsport Data API?
You can access live race data, driver and team information, race schedules, and historical race results.

### 2. How do I authenticate my API requests?
You must include your API key in the headers of your requests as outlined in the API documentation.

### 3. Are there usage limits for the API?
Yes, usage limits vary based on your chosen subscription plan. Check the RapidAPI dashboard for specifics.

### 4. Can I filter data by specific races or drivers?
Yes, the API allows filtering to retrieve data for specific races or individual drivers.

### 5. Is historical data available for past seasons?
Yes, the F1 Motorsport Data API includes historical data for previous seasons, allowing for detailed comparisons and analysis.

For more information and to start using the F1 Motorsport Data API, visit [F1 Motorsport Data API on RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/f1-motorsport-data).



