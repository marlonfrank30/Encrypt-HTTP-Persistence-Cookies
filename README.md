# 📘 F5 Knowledge Base Article Reference Repository

This repository contains structured references for key F5 BIG-IP Knowledge Base articles related to:

- Cookie security  
- HTTP/ASM cookie attributes  
- Cookie encryption  
- BIG-IP system-level enforcement settings  

It is designed to provide fast access for engineers, field personnel, and automation workflows.

---

## 📁 Structure

Each article is stored in its own directory:

```
F5-KB-Reference/
│
├── K13787/
├── K14784/
├── K000150090/
├── K93240866/
└── K51710370/
```

Each directory contains:

```
summary.md   – High-level overview of the article  
commands.md  – Related TMSH/CLI commands  
notes.md     – Field notes & operational considerations  
links.md     – Official F5 article links  
```

---

## 📚 Articles Included

| Article | Topic |
|--------|--------|
| **K13787** | Secure & HttpOnly attributes for ASM cookies |
| **K14784** | Cookie encryption in HTTP profile |
| **K000150090** | Video guide for cookie encryption |
| **K93240866** | Secure cookie enforcement via DOSL7.use_secure_cookies |
| **K51710370** | Secure cookie attribute behavior in non-HTTPS responses |

---

## 🛠️ Example Commands

### Enable Secure & HttpOnly
```
tmsh modify ltm profile http <profile>     cookie-secure enabled     cookie-httponly enabled
```

### Enable cookie encryption
```
tmsh modify ltm profile http <profile>     cookie-encryption enabled     cookie-encryption-passphrase "YourStrongPassphrase"
```

### Global secure cookie enforcement
```
tmsh modify sys db DOSL7.use_secure_cookies value true
```

---

## 🔗 Official F5 Article URLs

```
https://my.f5.com/manage/s/article/K13787
https://my.f5.com/manage/s/article/K14784
https://my.f5.com/manage/s/article/K000150090
https://my.f5.com/manage/s/article/K93240866
https://my.f5.com/manage/s/article/K51710370
```

---

## 🤝 Contributing

You may contribute by adding:

- Additional F5 Knowledge articles  
- Troubleshooting workflows  
- Automation examples (iCall, REST, Ansible, Terraform)  
- Operational notes  

---

## 📝 Disclaimer

This repository is not official F5 documentation—always validate changes in a test environment and reference the official articles when implementing in production.
