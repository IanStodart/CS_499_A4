# CS_499_A4
Kibana link: search-bitcoinprice-hgp5lulz3kgtaks2g2tf3xamla.us-west-1.es.amazonaws.com/_plugin/kibana/

This NodeJS application takes bitcoin prices (http://api.coindesk.com/v1/bpi/currentprice.json) every 60 seconds and inserts it into EBS
The API returns a JSON:

{"time":{"updated":"Mar 16, 2017 04:53:00 UTC","updatedISO":"2017-03-16T04:53:00+00:00","updateduk":"Mar 16, 2017 at 04:53 GMT"},"disclaimer":"This data was produced from the CoinDesk Bitcoin Price Index (USD). Non-USD currency data converted using hourly conversion rate from openexchangerates.org","bpi":{"USD":{"code":"USD","symbol":"&#36;","rate":"1,246.1480","description":"United States Dollar","rate_float":1246.148},"GBP":{"code":"GBP","symbol":"&pound;","rate":"1,016.0181","description":"British Pound Sterling","rate_float":1016.0181},"EUR":{"code":"EUR","symbol":"&euro;","rate":"1,162.2984","description":"Euro","rate_float":1162.2984}}}


And we pull the rate for USD, GBP and EUR.

Then Kibana graphs the USD Rate vs Time 
