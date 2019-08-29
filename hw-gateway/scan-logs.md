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

### URL staging: https://devserver.supplytics.com/hw-gateway/scans/?pageSize=10&pageNumber=0

### URL prod: https://app.original4sure.com/hw-gateway/scans/?pageSize=10&pageNumber=0

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
        "uid": "e4af8371-412e-495b-8f25-05dd501fd5e1",
        "product": {
          "uid": 766931923918,
          "serialNo": 19101587657,
          "encoding": "https://dev-o4s.in/v/e/1.1.BAGj7FE.J",
          "batchId": "some-batch-id",

          "sku": {
            "code": "honeywell-genetron-404h",
            "name": "Honeywell Genetron 404 H",
            "description": "This is a honeywell product made in USA",
            "images": {
              "thumbnail": "https://o4s.io/image/path1/img.png",
              "high": "https://o4s.io/image/path1/img.png",
              "medium": "https://o4s.io/image/path1/img.png"
            },

            "expiry": 1544692724327,

            "company": {
              "code": "honeywell",
              "numericCode": 19
            },
            "isActivated": true
          }
        },

        "status": {
          "code": "VERIFIED",
          "label": "Verified",
          "text": "Verified Original Product",
          "subText": "This product has already been verified by you"
        },

        "isExpired": false,

        "timestamp": 1544692724327
      }
    ]
  }
}
```
