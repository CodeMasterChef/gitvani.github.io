---
layout: post
title: Triip Me Report
---

# Technologies: 

Report bug: bugspag.com

Image server: imgix.net

Update app: codepush

# API:

Login:

```
curl -X POST \
  https://api.triip.me/api/v1/login_with_email \
  -H 'Postman-Token: 37314411-28ae-4a8a-884a-356830c85ae4' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json; charset=utf-8' \
  -d '{"email":"goldenbear8@mailinator.com","password":"goldenbear852"}'
```

Spin Wheel:

```
curl -X POST \
  https://api.triip.me/api/v1/spin_wheel \
  -H 'Authorization: eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOltdLCJleHAiOjE1NjIwNDQwNzYsIm5iZiI6MTU1OTQ1MjA3NiwiaXNzIjoiVFJJSVBNRSIsInVpZCI6Mjc3MTY2fQ.d3R-Ghh5n7czp8USW2D9sCKIZEDoxf8hmIHgGxyJmLs' \
  -H 'Postman-Token: f2703523-82b4-40b6-9fde-125ba46ef93e' \
  -H 'cache-control: no-cache' \
  -H 'user-code: U6AD6AA9E44'

```

Register:

```
curl -X POST \
  https://api.triip.me/api/v1/users \
  -H 'Postman-Token: d471f903-d95e-4d8b-9806-d94a1c345531' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json; charset=utf-8' \
  -d '{"email":"beetranx@mailinator.com","password":"beetranx","first_name":"Bee","last_name":"Tran","referral_code":"U27D444805A"}'

```

