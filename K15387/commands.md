# K15387 — Commands

## You can configure the following options for BIG-IP APM cookies in the Configuration utility
```
Access > Profiles / Policies > access profile name > SSO/Auth Domains (BIG-IP APM 13.x and later) 
Access Profiles > Access Profile Lists > access profile name > SSO/Auth Domains (BIG-IP APM 12.x and earlier)

```
**Secure**: If the BIG-IP APM virtual server is configured with a Client SSL profile, select Secure (default setting) when configuring the BIG-IP APM SSO/Auth Domain cookie settings.
**Persistent:** Session cookie persistence functions only on BIG-IP LTM and APM deployments. For BIG-IP APM deployments with connectivity resources (such as Network Access, Portal Access, etc.), you cannot set BIG-IP APM cookies as Persistent. This is by design, as session cookie persistence can present a security risk. For some deployments of the BIG-IP APM system, as with Microsoft SharePoint, cookie persistence may be required. When you select cookie persistence, persistence is hard coded at 60 seconds.
**HTTP Only:** For BIG-IP APM deployments with connectivity resources (such as Network Access, Portal Access, etc.), do not set BIG-IP APM cookies with the HTTP Only flag.
This feature is controlled by the apm.rotatesessionid database variable and has a default value of enable.

## Verify setting
```
tmsh list sys db apm.rotatesessionid
```
