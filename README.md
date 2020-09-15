# sms-api-sample

# Full Stack Team Six SMS API - Version 1

[![@fullstackteam6 on Twitter](http://img.shields.io/badge/twitter-%40awsforphp-blue.svg?style=flat)](https://twitter.com/fullstackteam6) 

This is the offcial **SMS API** sample provided by [Full Stack Team Six][full-stack-team-six] to makes it easy for developers to integrate our API in their code.

Jump To:
* [Getting Started](#Getting-Started)
* [Quick Examples](#Quick-Examples)
* [Getting Help](#Getting-Help)
* [Features](#Features) 
* [More Resources](#Resources) 

## Getting Started

1. **Create an Account** – Before you begin, you need to
   sign up and register your SENDER name.
 

## Quick Examples

### Sending an SMS using PHP

```php
$phone = "Enter the recipient phone number";
$msg = "Enter your message here";
$apiKey = "Enter your API Key";


// API URL
$url = 'https://portal.fullstackteamsix.com/api/v1/send/';

// Create a new cURL resource
$ch = curl_init();

curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_POST, 1);

// Attach encoded JSON string to the POST fields
curl_setopt($ch, CURLOPT_POSTFIELDS,
    "phone=" . $phone . "&message=" . $msg . "&key=" . $apiKey . "");

// Return response instead of outputting
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

// Execute the POST request
$server_output = curl_exec($ch);

// Close cURL resource
curl_close($ch);

echo $server_output;
```

## Getting Help

Please use these community resources for getting help. We use the GitHub issues for tracking bugs and feature requests and have limited bandwidth to address them.
For general issues regarding the SMS services and their limitations, you may also take a look at the [Documentation](https://fullstackteamsix.com/docs).


### Opening Issues

If you encounter a bug with `our API` we would like to hear about it. 

## Features

* Send Automated SMS via API
 
## Reach out on social media

* [@fullstackteam6][sdk-twitter] – Follow us on Twitter

##  To learn more visit our Documentation
 
[Documentation]: http://fullstackteamsix.com/docs 