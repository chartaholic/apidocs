# API Documentations for api.hoo.com

## Restful
* The base restful URI: **https://api.hoo.com**
* **JSON** is used as returned data format along with HTTP status code `200`
* **JSON {"error": "xxx"}** will be returned in case of exceptions with status `4XX` `5XX`

## Websocket
* The websocket URI: **wss://api.hoo.com/websocket**

## Authentication
[Authentication](./authentication.md)

# Endpoints

Name | Auth | Description
------------ | ------------ | ------------
[restful-market](./restful-market.md) | Public | currencies and pairs in market
[restful-quotations](./restful-quotations.md) | Public | tickers and klines
[restful-orders](./restful-orders.md) | **Private** | submit and cancel orders, active and today orders
[restful-accounts](./restful-accounts.md) | **Private** | asset in accounts
[restful-pairs](./restful-pairs.md) | **Private** | depth, trades and ticker
[websocket-trading](./websocket-trading.md) | **Private** | orders and accounts involved in trading
[websocket-pairs](./websocket-pairs.md) | **Private** | trades, depth change for every trading
[websocket-tickers](./websocket-tickers.md) | **Private** | ticker and 10 levels depth

## Root / Ping

```
GET /
```
Root path. can be used as a ping

**Response:**
```json
{
  "api": "hoo.com",
  "version": "v1"
}
```

**Ratelimit:**
60 requests / 60 seconds
