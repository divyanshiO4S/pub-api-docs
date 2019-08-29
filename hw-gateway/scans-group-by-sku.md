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

### URL staging: https://devserver.supplytics.com//hw-gateway/scans/group-by-sku/

### URL prod: https://app.original4sure.com//hw-gateway/scans/group-by-sku/

#### Method : **GET**

### Headers:

```
authToken: eyJhbGciOiJIUzIR5cCI6IkpXVCJ9.eyJsZXZlbCI6NSwidTUVSIiwicGhvbmVOdW1iZXIiOiIrMTIzNDg3ODkxMjM3IiwiZGV2aWNlSWQiOiI1NThkZjU3MC04NjkzLTRmOTItYWYTZmMTE3NzIzMjgifQ.3PxZeKO3HBrC2ToeGQWWKUgI

accessToken: eyJhbIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMasjdhjkhde33M3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt79BBihqE

Content-Type: application/json
```

# Response

```json
{
  "success": true,
  "data": {
    "items": [
      {
        "sku": {
          "code": "honeywell-genetron-404h",
          "name": "Honeywell Genetron 404 H",
          "description": "This is a honeywell product made in USA",
          "images": {
            "thumbnail": "https://o4s.io/image/path1/img.png",
            "high": "https://o4s.io/image/path1/img.png",
            "medium": "https://o4s.io/image/path1/img.png"
          },
          "infoTables": [
            {
              "title": "Documents",
              "rows": [
                {
                  "ptCharts": "https://s3.com/link/to/ptcharts.pdf",
                  "MSDS": "https://s3.com/link/to/msds.pdf",
                  "specifications": "https://s3.com/link/to/spec.pdf"
                }
              ]
            }
          ]
        },
        "count": 10
      },
      {
        "sku": {
          "code": "honeywell-genetron-505h",
          "name": "Honeywell Genetron 505 H",
          "description": "This is a honeywell product made in USA",
          "images": {
            "thumbnail": "https://o4s.io/image/path1/img.png",
            "high": "https://o4s.io/image/path1/img.png",
            "medium": "https://o4s.io/image/path1/img.png"
          },
          "infoTables": [
            {
              "title": "Documents",
              "rows": [
                {
                  "ptCharts": "https://s3.com/link/to/ptcharts.pdf",
                  "MSDS": "https://s3.com/link/to/msds.pdf",
                  "specifications": "https://s3.com/link/to/spec.pdf"
                }
              ]
            }
          ]
        },
        "count": 24
      }
    ]
  }
}
```
