# API styleguide

A place to define the conventions we use to build APIs

<!-- TOC depth:6 withLinks:1 updateOnSave:1 -->
- [API styleguide](#api-styleguide)
	- [Basic Tools](#basic-tools)
	- [Localization](#localization)
<!-- /TOC -->

## Basic Tools

It's quite common in Hyper to build APIs with *ruby on rails*, so most of this conventions are designed to work well with Rails.

## Localization

When the responses need to be localized, it's recommended the client to send the
`Accept-Language` header:

```
Accept-Language: nb-no, no, en
```

this means that the client is asking for a *norwegian bokmål* response, if not, it will fallback until english finally
