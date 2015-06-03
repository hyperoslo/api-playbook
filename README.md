# API styleguide

A place to define the conventions we use to build APIs

## Basic Tools

It's quite common in Hyper to build APIs with *ruby on rails*, so most of this
conventions are designed to work well with Rails.

## Authentication

for authenticating users into the API, we use one of two strategies, with the
`Authorization` header

### http basic auth

Useful when there is no real need for different users on the backend, that said
the authentication will be sent to the backend with the `Authorization` header
as follows:

```
Authorization: Basic c2YjdXNecjpDbjFzDjAxNA==
```

### token base auth

When the application is more complex and we need different users, we use the
`Authorization` header to send that token to the backend:

```
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9.TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ
```
