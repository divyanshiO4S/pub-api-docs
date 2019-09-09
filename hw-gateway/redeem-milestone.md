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


### URL staging: https://devserver.supplytics.com/hw-gateway/reward/claim/milestone
### URL prod: https://app.original4sure.com/hw-gateway/reward/claim/milestone

#### Method : **POST**

### Headers:

```
authToken: eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE

accessToken: eyJhbIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMasjdhjkhde33M3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt79BBihqE

Content-Type: application/json
```

### Body:

```json
{
  "rewardCode": "RC-2C7E7",
  "product" : "https://dev-o4s.in/v/e/1.1.84t_IN.F"
}
```

# Response

```json
{
  "success": true,
  "data": {
    "rewardClaimed" : true
  }
}
```
