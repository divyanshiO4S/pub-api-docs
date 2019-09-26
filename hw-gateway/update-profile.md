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

### URL staging : https://devserver.supplytics.com/hw-gateway/user/update-profile
### URL prod : https://app.original4sure.com/hw-gateway/user/update-profile

#### Method : **PUT**

#### Headers :

```
authToken : eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE

accessToken: eyJhbIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMasjdhjkhde33M3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt79BBihqE

```

#### NON-EDITABLE FIELDS : **phoneNumber, type, companyName**

#### Body :

```json
{
    "type" : "TRADER",
    "firstName" : "John",
    "lastName" : "Doe",
    "companyName" : "Doe Trader",
    "designation" : "Store Manager",
    "email" : "john.doe@test.com",
}
```

## Response

---

```json
{
  "success" : true,
  "data" : {
    "isProfileComplete" : true,
    "user": {
    "type" : "TRADER",
    "firstName" : "John",
    "lastName" : "Doe",
    "companyName" : "Doe Trader",
    "designation" : "Store Manager",
    "email" : "john.doe@test.com",
    }
  }
    
}
```