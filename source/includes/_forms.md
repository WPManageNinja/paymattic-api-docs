# Froms

## Get All Froms

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
```

```javascript

```

> The above command returns JSON structured like this:

```json
[
  {
    "ID": "32",
    "post_author": "1",
    "post_date": "2022-07-21 05:02:56",
    "post_date_gmt": "2022-07-21 05:02:56",
    "post_content": "",
    "post_title": "Event Registration Form (#32)",
    "post_excerpt": "",
    "post_status": "publish",
    "comment_status": "closed",
    "ping_status": "closed",
    "post_password": "",
    "post_name": "event-registration-form",
    "to_ping": "",
    "pinged": "",
    "post_modified": "2022-07-21 05:02:56",
    "post_modified_gmt": "2022-07-21 05:02:56",
    "post_content_filtered": "",
    "post_parent": "0",
    "guid": "http://wp.test/?p=32",
    "menu_order": "0",
    "post_type": "wp_payform",
    "post_mime_type": "",
    "comment_count": "0",
    "preview_url": "http://wp.test/?wp_paymentform_preview=32",
    "entries_count": 0
  },
  {
    "ID": "30",
    "post_author": "1",
    "post_date": "2022-07-20 05:38:14",
    "post_date_gmt": "2022-07-20 05:38:14",
    "post_content": "",
    "post_title": "Blank Form (#30)",
    "post_excerpt": "",
    "post_status": "publish",
    "comment_status": "closed",
    "ping_status": "closed",
    "post_password": "",
    "post_name": "blank-form-2",
    "to_ping": "",
    "pinged": "",
    "post_modified": "2022-07-20 05:38:14",
    "post_modified_gmt": "2022-07-20 05:38:14",
    "post_content_filtered": "",
    "post_parent": "0",
    "guid": "http://wp.test/?p=30",
    "menu_order": "0",
    "post_type": "wp_payform",
    "post_mime_type": "",
    "comment_count": "0",
    "preview_url": "http://wp.test/?wp_paymentform_preview=30",
    "entries_count": 2
  },
]
```

This endpoint retrieves all forms.

### HTTP Request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms`

### Query Parameters

Parameter | Type | Description | Required | Default
--------- | -----| ----------- | -------- | ------
per_page | int | Forms per page. | false | 20
page | int | Page number of pagination | false | 1
search | string | Search by forms title | false |
order_by | string | Forms sort by(use sorting key) | false |
order_type | string | ASC/DESC | false | ASC


<aside class="success">Remember — Use authentication Headers</aside>

## Create a form

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

```javascript

```

> The first command returns JSON structured like this:

```json
{
    "message":"Form successfully created.",
    "form_id":34
}
```

> The second command returns JSON structured like this:

```json
{
    "message":"Setting successfully created.",
}
```

This first endpoint creates a new blank form. Using this endpoint you will be able to create a new blank form with required params. However, to create a full workable form run the second endpoint providing form fields as builder_settings param and submit button settings as submit_button_settings.


### HTTP Requests

`POST https://yourdomain.com/wp-json/wppayform/v2/forms`

`POST https://yourdomain.com/wp-json/wppayform/v2/form/{id}/`

### URL Parameters for first end point

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
post_title | string | true | The title of the form
template | string | true | Name of the form template

### URL Parameters for second end point

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
id | int | true | The newly created form id.
builder_settings | json_string | true | All the fields and settings in a json string format
submit_button_settings | json_string | true | Submit button settings in a json string format

## Get a specific form

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

```javascript

```

> The above command returns JSON structured like this:

```json
{
    "ID": 35,
    "post_author": "1",
    "post_date": "2022-07-26 08:36:37",
    "post_date_gmt": "2022-07-26 08:36:37",
    "post_content": "",
    "post_title": "Thanksgiving Donation Form (#35)",
    "post_excerpt": "",
    "post_status": "publish",
    "comment_status": "closed",
    "ping_status": "closed",
    "post_password": "",
    "post_name": "thanksgiving-donation-form",
    "to_ping": "",
    "pinged": "",
    "post_modified": "2022-07-26 08:36:37",
    "post_modified_gmt": "2022-07-26 08:36:37",
    "post_content_filtered": "",
    "post_parent": 0,
    "guid": "http://wp.test/?p=35",
    "menu_order": 0,
    "post_type": "wp_payform",
    "post_mime_type": "",
    "comment_count": "0",
    "filter": "raw",
    "show_title_description": "yes",
    "preview_url": "http://wp.test/?wp_paymentform_preview=35"
}
```

The endpoint return a specific form in a json format. Using this endpoint you will get all the data of a form.

### HTTP Request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}`

### URL Parameters for first end point

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
id | string | true | The specific form id

## Update a form

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

```javascript

```

> The above command returns JSON structured like this:

```json
{
   "message" : "Settings successfully updated"
}
```

The endpoint update a specific form. Using this endpoint you will get to update a form.

### HTTP Request

`POST https://yourdomain.com/wp-json/wppayform/v2/form/{id}`

### URL Parameters for first end point

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
id | string | true | The specific form id


## Delete a form

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: DELETE"
```

```javascript

```

> The above command returns JSON structured like this:

```json
{
    "message" : "Selected form successfully deleted"
}
```

The endpoint delete a specific form.

### HTTP Request

`DELETE https://yourdomain.com/wp-json/wppayform/v2/form/{id}`

### URL Parameters for first end point

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
id | string | true | The specific form id


## Get demo forms

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/demo" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

```javascript

```

> The above command returns JSON structured like this:

```json
{
   "demo_forms": {
        "blank_form": {
            "label": "Blank Form",
            "description": "Create a blank form",
            "category": "Basic",
            "preview_image": "http://wp.test/wp-content/plugins/wp-payment-form/assets/images/forms/demo_blank.png",
            "is_pro": false
        },
        "contact_form": {
            "label": "Contact Form",
            "description": "Create a simple contact form.",
            "category": "Basic",
            "preview_image": "http://wp.test/wp-content/plugins/wp-payment-form/assets/images/forms/demo_form2.png",
            "is_pro": false
        },
        "donation_form": {
            "label": "Donation Form",
            "description": "Create a simple Donation form.",
            "category": "Donation",
            "preview_image": "http://wp.test/wp-content/plugins/wp-payment-form/assets/images/forms/demo_form.png",
            "is_pro": false
        },
   }
}
```

This endpoint return demo froms. Using this endpoint you will be able to get different demo forms. 


### HTTP Request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/demo`

<aside class="success">Remember — Use authentication Headers</aside>

## List of available forms

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/formatted" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

```javascript

```

> The above command returns JSON structured like this:

```json
{
  "available_forms": [
        {
            "ID": "35",
            "post_title": "Thanksgiving Donation Form (#35)"
        },
        {
            "ID": "34",
            "post_title": "Contact Form (#34)"
        },
        {
            "ID": "33",
            "post_title": "Blank Form (#33)"
        },
    ]
}
```

This endpoint return list of available forms. No url paramaters required.

### HTTP Request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/formatted`





