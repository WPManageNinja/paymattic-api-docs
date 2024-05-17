# Entries

## Get entries

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```


> The above command returns  json structured like this:

```json
{
   "success":true,
   "data":{
      "submissions":[
         {
            "id":72,
            "form_id":"29",
            "user_id":"1",
            "customer_id":null,
            "customer_name":"ENIWeop5dD",
            "customer_email":"1c5jc@k1zw.com",
            "form_data_raw":{
               "__wpf_form_id":"29",
               "__wpf_current_url":"http://wp.test/?wp_paymentform_preview=29",
               "__wpf_current_page_id":"",
               "custom_payment_input":"512560",
               "customer_name":"ENIWeop5dD",
               "customer_name_1":"IA4IGMhVEY",
               "customer_email":"1c5jc@k1zw.com",
               "number":"034341",
               "address_input":{
                  "address_line_1":"8ZgDyq1xEC",
                  "address_line_2":"4iIftJAnDH",
                  "city":"crVOXHdCP1",
                  "state":"vyI8J5dZcU",
                  "zip_code":"mB98SQ8j6W",
                  "country":"AF"
               },
               "__stripe_payment_method_id":"pm_1LPP4yIyGOUknw8lkvqYV2gC"
            },
            "form_data_formatted":{
               "customer_name":"ENIWeop5dD",
               "customer_name_1":"IA4IGMhVEY",
               "customer_email":"1c5jc@k1zw.com",
               "number":"034341",
               "address_input":"8ZgDyq1xEC, 4iIftJAnDH, crVOXHdCP1, vyI8J5dZcU, mB98SQ8j6W, Afghanistan"
            },
            "currency":"USD",
            "payment_status":"paid",
            "submission_hash":"wpf_165874704462de78a4a943d134",
            "payment_total":51256000,
            "payment_mode":"test",
            "payment_method":"stripe",
            "status":"new",
            "ip_address":"127.0.0.1",
            "browser":"Chrome",
            "device":"Apple",
            "city":null,
            "country":null,
            "created_at":"2022-07-25 11:04:04",
            "updated_at":"2022-07-25 11:04:08",
            "post_title":"Credit Card Donation Form (#29)",
            "currencySettings":{
               "currency":"USD",
               "locale":"auto",
               "currency_sign_position":"left",
               "currency_separator":"dot_comma",
               "decimal_points":0,
               "settings_type":"global",
               "is_zero_decimal":false,
               "currency_sign":"&#36;"
            }
         },
         {
            "id":71,
            "form_id":"29",
            "user_id":"1",
            "customer_id":null,
            "customer_name":"arQcun2rs4",
            "customer_email":"1c5jc@k1zw.com",
            "form_data_raw":{
               "__wpf_form_id":"29",
               "__wpf_current_url":"http://wp.test/?wp_paymentform_preview=29",
               "__wpf_current_page_id":"",
               "custom_payment_input":"857256",
               "customer_name":"arQcun2rs4",
               "customer_name_1":"IA4IGMhVEY",
               "customer_email":"1c5jc@k1zw.com",
               "number":"960626",
               "address_input":{
                  "address_line_1":"ZADnMPsvVf",
                  "address_line_2":"CUxW3y53X0",
                  "city":"nydm5OvArI",
                  "state":"LBooT59e2y",
                  "zip_code":"b6PTKElzMw",
                  "country":"AF"
               },
               "__stripe_payment_method_id":"pm_1LOJDcIyGOUknw8lxpdXF5C6"
            },
            "form_data_formatted":{
               "customer_name":"arQcun2rs4",
               "customer_name_1":"IA4IGMhVEY",
               "customer_email":"1c5jc@k1zw.com",
               "number":"960626",
               "address_input":"ZADnMPsvVf, CUxW3y53X0, nydm5OvArI, LBooT59e2y, b6PTKElzMw, Afghanistan"
            },
            "currency":"USD",
            "payment_status":"paid",
            "submission_hash":"wpf_165848618962da7dad15ff2135",
            "payment_total":85725600,
            "payment_mode":"test",
            "payment_method":"stripe",
            "status":"new",
            "ip_address":"127.0.0.1",
            "browser":"Chrome",
            "device":"Apple",
            "city":null,
            "country":null,
            "created_at":"2022-05-06 10:36:29",
            "updated_at":"2022-05-22 10:36:32",
            "post_title":"Credit Card Donation Form (#29)",
            "currencySettings":{
               "currency":"USD",
               "locale":"auto",
               "currency_sign_position":"left",
               "currency_separator":"dot_comma",
               "decimal_points":0,
               "settings_type":"global",
               "is_zero_decimal":false,
               "currency_sign":"&#36;"
            }
         }
      ]
   }
}
```

This endpoint return all the entries/submissions for the given form id.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries`

### URL parameters

| Parameter      | type   | Required | Description                                     |
| -------------- | ------ | -------- | ----------------------------------------------- |
| id             | int    | true     | The `form ID` which entries you are gonna fetch |
| per_page       | int    | flase    | Entries per page ex: 15, 20                       |
| page_number          | int    | false    | Page number of pagination                       |
| search_string  | string | false    | Search by cutsomer_name,customer_email,payment method                           |
| payment_status | string | false    | Values are:  `paid, pending, failed`                     |
| status         | string | false    | Values are:  `read, unread`                              |

## Get a form reports


```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/reports" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```


> The above command returns  json structured like this:

```json
{
    "success": true,
    "data": {
        "reports": {
            "total": {
                "label": "All",
                "submission_count": 7,
                "payment_total": 381758400
            },
            "paid": {
                "label": "Paid",
                "submission_count": 4,
                "payment_total": 205150900
            },
            "processing": {
                "label": "Processing",
                "submission_count": 0,
                "payment_total": 0
            },
            "pending": {
                "label": "Pending",
                "submission_count": 2,
                "payment_total": "96731700"
            },
            "failed": {
                "label": "Failed",
                "submission_count": 0,
                "payment_total": 0
            },
            "refunded": {
                "label": "Refunded",
                "submission_count": 1,
                "payment_total": "79875800"
            },
            "abandoned": {
                "label": "Abandoned",
                "submission_count": 2,
                "payment_total": "96731700"
            }
        },
        "currencySettings": {
            "currency": "USD",
            "locale": "auto",
            "currency_sign_position": "left",
            "currency_separator": "dot_comma",
            "decimal_points": 0,
            "settings_type": "global",
            "is_zero_decimal": false,
            "currency_sign": "&#36;"
        },
        "is_payment_form": true
    }
}
```

This endpoint generates reports for a specific form.

### Https request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/reports`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form ID` |

## Get a specific entry

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/{entryId}" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```

> The above command returns  json structured like this:

```json
{
   "success":true,
   "data":{
      "submission":{
         "id":1,
         "form_id":"8",
         "user_id":"1",
         "customer_id":null,
         "customer_name":"tupsfrXOcd",
         "customer_email":"bdbhg@tl1w.com",
         "form_data_raw":{
            "__wpf_form_id":"8",
            "__wpf_current_url":"http://wp.test/?wp_paymentform_preview=8",
            "__wpf_current_page_id":"",
            "customer_name":"tupsfrXOcd",
            "customer_email":"bdbhg@tl1w.com",
            "text":"tRndFZTPqS",
            "textarea":"niKtsJAW3O"
         },
         "form_data_formatted":{
            "customer_name":"tupsfrXOcd",
            "customer_email":"bdbhg@tl1w.com",
            "text":"tRndFZTPqS",
            "textarea":"niKtsJAW3O"
         },
         "currency":"USD",
         "payment_status":"pending",
         "submission_hash":"wpf_165829447062d790c6e1977395",
         "payment_total":"0",
         "payment_mode":null,
         "payment_method":"",
         "status":"read",
         "ip_address":"127.0.0.1",
         "browser":"Chrome",
         "device":"Apple",
         "city":null,
         "country":null,
         "created_at":"2022-07-20 05:21:10",
         "updated_at":"2022-07-27 07:29:30",
         "post_title":"Contact Form (#8)",
         "user_profile_url":"",
         "transactions":[
            
         ],
         "order_items":[
            
         ],
         "discounts":{
            "applied":[
               
            ],
            "total":0,
            "percent":0
         },
         "tax_items":[
            
         ],
         "activities":[
            
         ],
         "refunds":[
            
         ],
         "refundTotal":0,
         "currencySetting":{
            "currency":"USD",
            "locale":"auto",
            "currency_sign_position":"left",
            "currency_separator":"dot_comma",
            "decimal_points":0,
            "settings_type":"global",
            "is_zero_decimal":false,
            "currency_sign":"&#36;"
         },
         "user":{
            "display_name":"elias",
            "email":"elias@gmail.com",
            "profile_url":""
         },
         "subscription_payment_total":0,
         "subscriptions":[
            
         ],
         "widgets":[
            
         ]
      },
      "entry":{
         "customer_name":{
            "label":"Name",
            "value":"tupsfrXOcd",
            "type":"customer_name"
         },
         "customer_email":{
            "label":"Email Address",
            "value":"bdbhg@tl1w.com",
            "type":"customer_email"
         },
         "text":{
            "label":"Subject",
            "value":"tRndFZTPqS",
            "type":"text"
         },
         "textarea":{
            "label":"Your Message",
            "value":"niKtsJAW3O",
            "type":"textarea"
         }
      }
   }
}
```

This endpoint will return a specific entry for the given form id and entryID.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/{entryId}`

### URL paramaters

| Parameter | type | Required | Description                |
| --------- | ---- | -------- | -------------------------- |
| id        | int  | true     | The `form ID` of the entry |
| entryId   | int  | true     | The specific `entry id`    |


## Delete note from entry


```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/{entryId}/notes/{noteId}" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: DELETE"
```

> The above command returns  json structured like this:

```json
{
    "success": true,
    "message": "Log deleted successfully!"
}
```

This endpoint delete a note from a specific entry. With given entry id and note id.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/{entryId}/notes/{noteId}`

### URL parameters

| Parameter | type | Required | Description                |
| --------- | ---- | -------- | -------------------------- |
| id        | int  | true     | The `form ID` of the entry |
| entryId   | int  | true     | The specific `entry id`    |
| noteId    | int  | true     | The specific `note id`     |

## Change entry status

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/{entryId}/status" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: POST"
```


> The above command returns  json structured like this:

```json
{
    "success": true,
    "message": "Log deleted successfully!"
}
```

This endpoint delete a note from a specific entry. With given entry id and note id.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/form/{id}/entries/{entryId}/status`

### URL parameters

| Parameter | type   | Required | Description                |
| --------- | ------ | -------- | -------------------------- |
| id        | int    | true     | The `form ID` of the entry |
| entryId   | int    | true     | The specific `entry id`    |
| status    | string | true     | Entry `status`             |


## Remove entry

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/entries/remove" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: DELETE"
```

> The above command returns  json structured like this:

```json
{
  "message": "Selected submission deleted successfully"
}
```

This end point removes/deletes an entry/submission for the given form id. You also need to provide the entry id.

### Http request

`DELETE https://yourdomain.com/wp-json/wppayform/v2/forms/entries/remove`

### URL parameters

| Parameter     | type | Required | Description                |
| ------------- | ---- | -------- | -------------------------- |
| submission_id | int  | true     | The specific `entry id`    |
| form_id       | int  | true     | The `form ID` of the entry |
