> _Every request should comprise of the following parameters_

```
{
  _location: {"latitude": number, "longitude": number} (optional)
  _clientVersion: "string" (app version)
  _clientTimestamp: "string" (epoch ms timestamp)
  _platform : "ios" | "android",
  _deviceId : "9nldasu8da89"
}
```

## Request

---

### URL : https://localhost:3001/honeywell/user/create-user

#### Method : **POST**

#### Body :

```json
{
  "phoneNumber": "+919818012935",
  "firebaseTokenID": "89ad9sdadad90ds"
}
```

## Response

---

```json
{
  "success": true,
  "data": {
    "authToken": "eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE",
    "isAlreadyRegistered": false
  }
}
```
### In case user with given phone number has registration completed
```json
{
  "success": true,
  "data": {
    "authToken": "eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE",
    "isAlreadyRegistered": false
  }
}
```