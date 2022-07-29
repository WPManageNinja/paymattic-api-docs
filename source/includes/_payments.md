# Payments

## Get payment method settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/settings/payments/{payMethod}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
    "payment_mode": "test",
    "test_api_key": "",
    "live_api_key": ""
}
```

This endpoint retrieves specific paymeny method settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/settings/payments/{payMethod}`

### URL parameters

| Parameter | type   | Required | Description                                                        |
| --------- | ------ | -------- | ------------------------------------------------------------------ |
| payMethod | string | true     | The name of the payment method `mollie, payrexx, square, paystack` |


## Global stripe settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/stripe" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
    "settings": {
        "payment_mode": "test",
        "live_pub_key": "",
        "live_secret_key": "",
        "test_pub_key": "your pub key",
        "test_secret_key": "your secret key",
        "company_name": "",
        "checkout_logo": "",
        "send_meta_data": "no"
    },
    "webhook_url": "https://wp.test/?wpf_stripe_listener=1",
    "is_key_defined": false
}
```

This endpoint retrieves specific paymeny method settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/settings/stripe`



## Get paypal settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/settings/payments/{payMethod}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
    "settings": {
        "payment_mode": "live",
        "paypal_email": "",
        "disable_ipn_verification": "no",
        "checkout_logo": ""
    },
    "confirmation_pages": {
        "confirmation": 5,
        "failed": 6
    },
    "pages": [
        {
            "ID": "2",
            "post_title": "Sample Page"
        },
        {
            "ID": "5",
            "post_title": "Payment Confirmation"
        },
        {
            "ID": "6",
            "post_title": "Payment Failed"
        },
        {
            "ID": "18",
            "post_title": "Course Catalog"
        },
        {
            "ID": "19",
            "post_title": "Membership Catalog"
        },
        {
            "ID": "20",
            "post_title": "Purchase"
        },
        {
            "ID": "21",
            "post_title": "Dashboard"
        },
        {
            "ID": "25",
            "post_title": "Dashboard"
        },
        {
            "ID": "26",
            "post_title": "Student Registration"
        },
        {
            "ID": "27",
            "post_title": "Instructor Registration"
        }
    ]
}
```

This endpoint retrieves paypal settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/settings/paypal`

## Save/Update a payment method settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/settings/payments/{payMethod}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

> The first command returns JSON structured like this:

```json
{
   "message": "Settings successfully updated"
}
```

This endpoint save/update a specific payment method settings.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/settings/payments/{payMethod}`

### URL parameters

| Parameter    | type   | Required | Description                                                                      |
| ------------ | ------ | -------- | -------------------------------------------------------------------------------- |
| payMethod    | string | true     | The name of the payment method ex: `mollie, payrexx, square, paystack`           |
| settings     | object | true     | The settings which consist of `payment_mode, test_api_key, live_api_key` fields. |
| payment_mode | text   | true     | Modes are `live, test`                                                           |
| test_api_key | object | true     | Test api key consist of `public key, secret key`.                                |
| live_api_key | object | true     | Live api key consist of `public key, secret key`                                 |


