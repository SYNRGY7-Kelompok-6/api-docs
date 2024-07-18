# Error response for all condition

## Type 
```
{
  "type": "string",
  "title": "string",
  "status": number,
  "detail": "string",
  "instance": "string"
}
```

## Example for 401 (Unauthorized) error
```
{
  "type": "about:blank",
  "title": "Unauthorized",
  "status": 401,
  "detail": "user not found",
  "instance": "/api/v1.0/auth/login"
}
```
