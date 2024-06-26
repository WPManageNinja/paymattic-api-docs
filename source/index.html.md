---
title: Paymattic API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - php
  - python

toc_footers:
  - <a href='https://paymattic.com/'>Get Paymattic</a>

includes:
  - forms
  - settings
  - entries
  - integrations
  - payments
  - reports
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for Paymattic WordPress plugin
---

# Introduction

Welcome to the Paymattic API document. This document will describe the REST API Endpoints of Paymattic.

The example API documentation page was created with [Slate](https://github.com/slatedocs/slate). If you find any typo or would like contribute please send a pull request with improvements. Please note that, All endpoints are not added to this doc (Work in progress).

# Authentication

> Example API Call for forms:

```php

```

```python

```

```shell
# With shell, you can just pass the correct header with each request, Basic Auth credentials need to be base64 encoded.
curl "https://yourdomain.com/wp-json/wppayform/v2/forms" \
  -H "Authorization: Basic $(echo -n 'USERNAME:APPLICATION_PASSWORD' | base64)"
```


> Make sure to replace USERNAME & APPLICATION_PASSWORD with your username & application password and have base64 encoded.

Paymattic uses WordPress REST API. So you can use any authorization method that supports WordPress. The easiest way to connect is application password. To create a application password go to the __Users__ and click on the user and create a new application password for this user so that this person can easily access the REST API endpoint by using WP Username & Application password in basic auth system.

Once you create your Application Password in WordPress, Add Authorization Header to every request.

In the basic auth username section use your WP Username and in the password section use the created Application Password.

__Api Base URL__: `https://yourdomain.com/wp-json/wppayform/v2`

<aside class="notice">
You must replace <code>yourdomain.com</code> with your domain name.
</aside>


