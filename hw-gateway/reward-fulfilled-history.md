> _Every request should comprise of the following parameters_

```
{
  _location: {"latitude": number, "longitude": number} (optional)
  _clientVersion: "string" (app version)
  _clientTimestamp: "string" (epoch ms timestamp)
  _platform : "ios" | "android",
  _deviceId : "9nldasu8dsa89"
}
```

# Request


### URL staging: https://devserver.supplytics.com/hw-gateway/reward/fulfilment/history?pageSize=10&pageNumber=0
### URL prod: https://app.original4sure.com/hw-gateway/reward/fulfilment/history?pageSize=10&pageNumber=0

#### Method : **GET**

### Headers:

```
authToken: eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE

accessToken: eyJhbIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMasjdhjkhde33M3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt79BBihqE

Content-Type: application/json
```

# Response

```json
{
  "success": true,
  "data": [
    {
      "sku" : {
        "code": "genetron-r-407c",
        "name": "Genetron R 407C",
      },
      "companyName": "John Contractor"
      "timestamp": 1544692724327
    }
  ] 
}
```
