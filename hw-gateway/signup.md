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


### URL staging : https://devserver.supplytics.com/hw-gateway/user/create-user
### URL prod : https://app.original4sure.com/hw-gateway/user/create-user

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
    "isProfileComplete": false
  }
}
```
### In case user with given phone number has profile completed
```json
{
  "success": true,
  "data": {
    "isProfileComplete": true,
    "authToken": "eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE",
    "accessToken": "eyJhbIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMasjdhjkhde33M3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt79BBihqE",
    "user": {
      "type" : "TRADER",
      "name" : "John Doe",
      "companyName" : "Doe Trader",
      "designation" : "Store Manager",
      "email" : "john.doe@test.com",
    }
  }
}
```
