# REST API Basics

A REST-style API exposes resources through predictable URLs and HTTP methods. It returns representations, commonly JSON, rather than server-rendered HTML.

```http
GET /api/books/42 HTTP/1.1
Accept: application/json
```

```http
HTTP/1.1 200 OK
Content-Type: application/json

{"id":42,"title":"PHP Basics"}
```

The first request asks for book 42; the response returns its JSON representation.

Tip: authenticate and authorize every protected resource. A predictable URL does not grant access to its data.
