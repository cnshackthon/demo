# test
## apigee sim
curl -X POST http://127.0.0.1:8080/nac/v2/subscriber/location -d "{\"id\":\"123456789\"}"
## dscf 
curl -X POST http://127.0.0.1:8081/ndscf/v1/location/123456789
curl -X POST http://127.0.0.1:8081/ndscf/v1/location/987654321
### add correlation
curl -X PUT http://127.0.0.1:8081/ndscf/v1/correlation/imsi-999559807001001 -d "{\"subIds\":[\"123456789\"]}"
curl -X PUT http://127.0.0.1:8081/ndscf/v1/correlation/imsi-999559807001001 -d "{\"subIds\":[\"123456789\",\"987654321\"]}"
