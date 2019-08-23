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

### URL : https://localhost:3001/honeywell/user/register

#### Method : **POST**

#### Headers :

```
authToken : eyJhbG1NiIsInR5cCI6IkpXVCJ9.eyJsZXZlbCI6NCicGhvbmVOdW1iZXIiOiIrMTMyNzgxMjM5Nzg5NzgxMjM3OTgiLCJkZXZpY2VJZCI6Ik5hdmlzaW9uIn0.Gogge1r4YSi3QETUt78zMniPdLB9BBihqE
```

#### Body :

```
{
    type : "TRADER",
    name : "John Doe",
    companyName : "Doe Trader",
    designation : "Store Manager",
    email : "john.doe@test.com",
}
```

## Response

---

```json
{
    "success" : true,
    "data" : {
      "isAlreadyRegistered" : false
    }
    
}
```

## Error Response (A) in case the user is already registered.

```json
{
    "success" : false,
    "data" : {
      "isAlreadyRegistered" : true,
    }
}
```

## Error Response (B) in case the company provided in the request body is not an exact match in the database

```json
{
    "success" : false,
    "data" : {
      "isAlreadyRegistered" : false,
      "didYouMeanCompany" : "Doe Traders"
    }
}
```
