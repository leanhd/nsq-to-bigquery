![nsq to bigquery logo](http://i1.wp.com/eran.sandler.co.il/wp-content/uploads/2015/11/nsq-to-bigquery.png?resize=300%2C117)

[![Build Status](https://travis-ci.org/erans/nsq-to-bigquery.svg)](https://travis-ci.org/erans/nsq-to-bigquery)

# nsq-to-bigquery
Stream NSQ messages to Google's BigQuery using the streaming API.

Written by Eran Sandler ([@erans](https://twitter.com/erans))


This is a very early version that does work but was not (yet) tested in real hard production environment.

## Assumptions / Limitations:
- Message body is a valid JSON that is a flat dictionary (only key and simple values).
- Each message must contain data that will constitute a single row that will go into BigQuery.
- BigQuery table MUST exists and the schema MUST match the JSON being sent.
- This version sends each message in its own request and does not use any batch API (yet).


