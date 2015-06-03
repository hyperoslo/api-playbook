# API styleguide

A place to define the conventions we use to build APIs

## Basic Tools

It's quite common in Hyper to build APIs with *ruby on rails*, so most of this conventions are designed to work well with Rails.

## Headers

A list of useful headers and how they work

### Request Headers

#### Accept-Language

When you need the responses to be localized, it's recommended to use the
`Accept-Language` header:

```
Accept-Language: nb-no, no, en
```

this means that the client is asking for a *norwegian bokmål* response, if not, it will fallback until english finally
