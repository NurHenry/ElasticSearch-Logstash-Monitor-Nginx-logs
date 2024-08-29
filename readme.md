# Logstash Configuration for Nginx Logs

## Overview

With this Logstash configuration file you will be able to parse Nginx access logs, and forward the data to Elasticsearch.

Make sure you have Logstash installed.

## Parsed Fields

The configuration extracts the following fields from each Nginx log entry:

- **Client IP** (`clientip`): The IP address of the client who sent the request.
- **Timestamp** (`timestamp`): The date and time when the request was received.
- **HTTP Method** (`verb`): The HTTP method used (e.g., `GET`, `POST`).
- **Request Path** (`request`): The requested resource path.
- **HTTP Version** (`httpversion`): The HTTP protocol version.
- **Response Code** (`response`): The HTTP response status code (e.g., `200`, `404`).
- **Bytes Sent** (`bytes`): The size of the response in bytes.
- **Referrer** (`referrer`): The URL of the referring page.
- **User Agent** (`agent`): Information about the client (browser type and version).
- **Geolocation** (`geoip`): Geographical data derived from the client IP address (e.g., country, city).

## Usage

### 1. Location of the Config

Save the provided Logstash configuration file as `nginx_logstash.conf` in ```bash /etc/logstash/conf.d/
