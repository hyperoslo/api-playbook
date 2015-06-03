# API styleguide

A place to define the conventions we use to build APIs

<!-- TOC depth:6 withLinks:1 updateOnSave:1 -->
- [API styleguide](#api-styleguide)
	- [Basic Tools](#basic-tools)
	- [Versioning](#versioning)
<!-- /TOC -->

## Basic Tools

It's quite common in Hyper to build APIs with *ruby on rails*, so most of this conventions are designed to work well with Rails.

## Versioning

On standart rails applications, there are 3 used schemas for versioning


  * Url

  ```
  GET hyper.super-app.no/api/v1.2/spaceships
  ```

  * Query parameters

  ```
  GET hyper.super-app.no/api/spaceships?version=1.2
  ```

  * Accept Header (Chosen approach)

  ```
  GET hyper.super-app.no/api/spaceships
  ```

  request headers

  ```
  Accept: application/vnd.super-app+json; version=1.2
  ```

There is many blog post and controversy about this on the internet. Hyper's
current approach is to use **the `Accept` header**, since we allow resource Urls
to be _permalink_ and we don't bulk all parameters in the url.

_this comes with the cost that is a little more difficult to share the url of
a given request_

The reference for this was taken from the [Big Nerd Ranch][2fc9a579]

  [2fc9a579]: https://www.bignerdranch.com/blog/adding-versions-rails-api/ "Big Nerd Ranch"
