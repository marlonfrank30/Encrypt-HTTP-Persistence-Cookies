# K13787 — Commands

## Enable Secure + HttpOnly
```
tmsh modify ltm profile http <profile_name> \
    cookie-secure enabled \
    cookie-httponly enabled
```
