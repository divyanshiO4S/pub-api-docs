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

# Request:

### URL staging: https://devserver.supplytics.com/hw-gateway/reward-milestone-logs/?pageSize=10&pageNumber=0

### URL prod: https://app.original4sure.com/hw-gateway/reward-milestone-logs/?pageSize=10&pageNumber=0

#### Method : **GET**

#### Headers :

```
authToken : eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE

accessToken: eyJhbIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMasjdhjkhde33M3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt79BBihqE

Content-Type: application/json
```

# Response:

```json
{
  "success": true,
  "data": {
    "items": [
      {
        "sku": {
          "code": "genetron-r-407c",
          "name": "Genetron R 407C",
          "milestoneCriteria": {
            "scanned": 2,
            "required": 10,
            "progress": 50,
            "isClaimable": false,
            "rewardCode": "RC-2C7E7",
          }
        },
        "timestamp": 1544692724327
      },
      {
        "sku": {
          "code": "genetron-r-134a",
          "name": "Genetron R 134A",
          "milestoneCriteria": {
            "scanned": 10,
            "required": 10,
            "progress": 100,
            "isClaimable": true,
            "rewardCode": "RC-2C7E8",
          }
        },
        "timestamp": 1544692724320
      }
    ]
  }
}
```
