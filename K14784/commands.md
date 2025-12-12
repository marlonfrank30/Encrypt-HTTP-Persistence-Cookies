# K14784 — Commands

## Enable cookie encryption
```
tmsh modify ltm profile http <profile_name> \
    cookie-encryption enabled \
    cookie-encryption-passphrase "YourStrongPassphrase"
```
