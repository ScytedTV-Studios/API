---
title: Authorization
excerpt: The methods of autorizing requests to the ScytedTV API.
deprecated: false
hidden: false
metadata:
  robots: index
---
To ensure secure access to the API, we provide several authentication methods for authorized API requests. You can authenticate your requests by using any of the following methods:

## 1. Bearer Authentication (Recommended)

The preferred method for authenticating requests is by including a Bearer token in the `Authorization` header of your HTTP request. Here's an example:

```http HTTP
Authorization: Bearer <your_token>
```

## 2. Token in URL Path

You can include the token directly in the URL path. Ensure that the token is placed after the `/token/` segment, like this:

```text URL
https://api.scyted.tv/token/<your_token>/<path>
```

## 3. Token in URL Query Parameter

Alternatively, you can add the token as a query parameter to the URL, like this:

```text URL
https://api.scyted.tv/<path>?token=<your_token>
```

## 4. Username and Password in URL

If necessary, you can authenticate using basic authentication by placing your username and password directly in the URL. The format should look like this:

```text URL
https://<username>:<password>@api.scyted.tv/<path>
```

> \[!NOTE]\
> For enhanced security, it is recommended to use the Bearer Authentication method or URL Token-based methods instead of embedding your username and password in the URL.