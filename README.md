# Usage Aggregator
Acme telecom is in its early days and wants to manage their subscribers' data usage.

They asked Openet to develop a system providing two APIs:
- _reportUsage_, informing how many bytes were used by a given subscriber at an specific timestamp; and
- _getAggregatedUsage_, retrieving what was the total usage consumed by a given subscriber per day.

## reportUsage

Report how many bytes were used by a subscriber on a given time.

Consists of a POST request, passing a JSON payload:
```
{
    "subscriberId" : 5420123,
    "amount": 1024000,
    "timestamp": "2018-06-04T20:30:00.000-04:00"
}
```

And returns a JSON response:
```
{
    "status": "Success"
}
```

## getAggregatedUsage

Returns a list of total usages per day, for all days that had any usage for the given subscriber

Consists of a POST request, passing a JSON payload:

```
{
    "subscriberId": 1023595
}
```

And returns a JSON response:
```
{
  "totalUsage": 2000000,
  "day": "2018-06-04"
},
{
  "totalUsage": 1000000,
   "day": "2018-06-05"
}
```

## Instructions
1. Feel free to use any coding language, database and open source libraries/frameworks
2. Send a github project link with your submission
3. Add in your README: 
  - instructions on how to run the application
  - any assumptions you took while developing your application
