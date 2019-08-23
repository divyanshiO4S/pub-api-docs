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

### URL: http://localhost:3001/supplytics/products/scanin

### Headers:

```
authToken: eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE

Content-Type: application/json
```

### Body:

```json
{
  "products": [
    "http://localhost:3001/v/e/1.2.8-nBhIs.1Z",
    "http://localhost:3001/v/e/1.2.41Dwt2H.1Z"
  ]
}
```

# Response

```json
{
  "success": true,
  "data": {
    "scans": [
      {
        "uid": "e4af8371-412e-495b-8f25-05dd501fd5e1",
        "product": {
          "uid": 766931923918,
          "serialNo": 19101587657,
          "encoding": "http://localhost:3001/v/e/1.2.8-nBhIs.1Z",
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
      },
      {
        "uid": "e4af8371-412e-495b-8f25-05dd501fd5e1",
        "product": {
          "uid": 766931923918,
          "serialNo": 19101587657,
          "encoding": "http://localhost:3001/v/e/1.2.41Dwt2H.1Z",
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
