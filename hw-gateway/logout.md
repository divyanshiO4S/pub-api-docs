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

## Request

---

### URL : https://localhost:3001/honeywell/user/logout

#### Method : **GET**

#### Header :

```
authToken : eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE
```

## Response

---

```json
{
    "success" : true,
    "data" : {
      "isLoggedOut" : true
    },
    "many" : false
}
```
