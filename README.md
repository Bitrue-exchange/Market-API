
## Bitrue API - Trade Volume

## General API Information

- Datetime default is Unix timestamp, the unit is second。

## API LIST

|API|URL|Note|
|----|---------|------|--------|
|All market real-time query|https://www.bitrue.com/kline-api/public.json?command=returnTicker |none|
|BTC Market query|https://www.bitrue.com/kline-api/publicBTC.json?command=returnTicker|BTC Base Market query|
|ETH Market query|https://www.bitrue.com/kline-api/publicETH.json?command=returnTicker|ETH Market query|
|USDT Market query|https://www.bitrue.com/kline-api/publicUSDT.json?command=returnTicker |USDT Market query|
|XRP Market query|https://www.bitrue.com/kline-api/publicXRP.json?command=returnTicker|XRP Market query|

 
## Response
|Key|Type|Description|
|---|---|---|
|code|string|response code:200, 404, 500...|
|msg|string|response|
|data|json_array|Data（depends on the API）|

## Response code description
|code|Description|
|---|---|
|200|Success|
|304|Repeat request|
|400|Request parameter verification error|
|403|No permission|
|404|not found|
|500|System error|
|4042|System maintaining|

> Sample
```
{
    "code":200,
    "msg":"succeed",
    "data": {}
}
```


## For BTC Market Parameter description example

> GET /kline-api/publicBTC.json?command=returnTicke

- Response BTC Market Trade Info

|Name|Description|
|-----|-----|
|id|Market|
|last|Last Price|
|lowestAsk|Lowest Ask（not support yet）|
|highestBid|Highest Bid（not support yet）|
|percentChange|Percent Change%|
|baseVolume|Trade Volume|
|quoteVolume|Trade Amount|
|isFrozen|Market status(not support yet)|
|high24hr|24h High|
|low24hr|24h Low|
- Sample
```
{
  "code": "200",
  "msg": "success",
  "data": {
  "BCH_BTC": {
	"id": 1394685782,
	"last": "0.07850300",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.007",
	"baseVolume": "1729.931",
	"quoteVolume": "135.21860399",
	"isFrozen": "0",
	"high24hr": "0.07960000",
	"low24hr": "0.07777800"
	},
	"WAN_BTC": {
	"id": 795141907,
	"last": "0.0001928",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0669",
	"baseVolume": "241548.53",
	"quoteVolume": "46.8440527",
	"isFrozen": "0",
	"high24hr": "0.0002204",
	"low24hr": "0.0001761"
	},
	"LTC_BTC": {
	"id": 1092843370,
	"last": "0.00857500",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0085",
	"baseVolume": "7843.49",
	"quoteVolume": "66.74141753",
	"isFrozen": "0",
	"high24hr": "0.00869400",
	"low24hr": "0.00847000"
	},
	"ETC_BTC": {
	"id": 1293247427,
	"last": "0.00185900",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "-0.0016",
	"baseVolume": "37012.40",
	"quoteVolume": "68.72889752",
	"isFrozen": "0",
	"high24hr": "0.00187400",
	"low24hr": "0.00184600"
	},
	"QKC_BTC": {
	"id": 958009304,
	"last": "0.00000451",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0226",
	"baseVolume": "4861038",
	"quoteVolume": "21.17869343",
	"isFrozen": "0",
	"high24hr": "0.00000465",
	"low24hr": "0.00000419"
	},
	"ETH_BTC": {
	"id": 1293098472,
	"last": "0.04113800",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0039",
	"baseVolume": "3303.743",
	"quoteVolume": "135.14303115",
	"isFrozen": "0",
	"high24hr": "0.04162500",
	"low24hr": "0.04066800"
	},
	"BTC_USDT": {
	"id": 197056895,
	"last": "6690.90",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0022",
	"baseVolume": "284.621",
	"quoteVolume": "1903605.97",
	"isFrozen": "0",
	"high24hr": "6737.77",
	"low24hr": "6628.85"
	},
	"XRP_BTC": {
	"id": 750753317,
	"last": "0.00004913",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0188",
	"baseVolume": "1815150",
	"quoteVolume": "87.87376996",
	"isFrozen": "0",
	"high24hr": "0.00004941",
	"low24hr": "0.00004812"
	},
	"BAT_BTC": {
	"id": 1396175332,
	"last": "0.00003182",
	"lowestAsk": "0",
	"highestBid": "0",
	"percentChange": "0.0072",
	"baseVolume": "114978",
	"quoteVolume": "3.59932522",
	"isFrozen": "0",
	"high24hr": "0.00003219",
	"low24hr": "0.00003097"
	}
  }
}
```

