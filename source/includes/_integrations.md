# Integrations 

## Get form integrations

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
   "feeds":[
      
   ],
   "available_integrations":{
      "UserRegistration":{
         "category":"wp_core",
         "disable_global_settings":"yes",
         "logo":"https://wp.test/wp-content/plugins/wp-payment-form/assets/images/integrations/user_registration.png",
         "title":"User Registration Integration",
         "is_active":true
      },
      "lifterlms":{
         "title":"LifterLMS Integration",
         "logo":"https://wp.test/wp-content/plugins/wp-payment-form/assets/images/integrations/lifterlms.png",
         "is_active":true,
         "configure_title":"Configuration required!",
         "global_configure_url":"#",
         "configure_message":"LifterLMS is not configured yet! Please configure your LifterLMS api first",
         "configure_button_text":"Set LifterLMS"
      },
      "fluentcrm":{
         "title":"FluentCRM Integration",
         "logo":"https://wp.test/wp-content/plugins/wp-payment-form/assets/images/integrations/fluentcrm-logo.png",
         "is_active":true,
         "configure_title":"Configuration required!",
         "global_configure_url":"#",
         "configure_message":"FluentCRM is not configured yet! Please configure your FluentCRM api first",
         "configure_button_text":"Set FluentCRM"
      },
      "sms_notification":{
         "title":"SMS Notification by Twilio",
         "logo":"https://wp.test/wp-content/plugins/wp-payment-form/assets/images/integrations/twilio.png",
         "is_active":false,
         "configure_title":"Configuration required!",
         "global_configure_url":"https://wp.test/wp-admin/admin.php?page=fluent_forms_settings#general-sms_notification-settings",
         "configure_message":"SMS Notification is not configured yet! Please configure your SMS api first",
         "configure_button_text":"Set SMS Notification API"
      }
   },
   "all_module_config_url":"https://wp.test/wp-admin/admin.php?page=wppayform.php#/integrations"
}
```

This endpoint retrieves all available integrations of a form.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |


## Get integration settings of a form


```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
   "settings":{
      "conditionals":{
         "conditions":[
            
         ],
         "status":false,
         "type":"all"
      },
      "enabled":true,
      "list_id":"",
      "list_name":"",
      "name":"",
      "merge_fields":[
         
      ]
   },
   "settings_fields":[
      
   ],
   "shortcodes":[
      {
         "title":"Inputs",
         "shortcodes":{
            "{input.customer_name}":"Name",
            "{input.customer_email}":"Email Address"
         }
      },
      {
         "title":"Submission Info",
         "shortcodes":{
            "{submission.id}":"Submission ID",
            "{submission.submission_hash}":"Submission Hash ID",
            "{submission.customer_name}":"Customer Name",
            "{submission.customer_email}":"Customer Email",
            "{submission.payment_method}":"Payment Method"
         }
      },
      {
         "title":"Payment Items",
         "shortcodes":[
            
         ]
      },
      {
         "title":"WordPress",
         "shortcodes":{
            "{wp:post_id}":"Post ID",
            "{wp:post_title}":"Post Title",
            "{wp:post_url}":"Post URL",
            "{wp:post_author}":"Post Author",
            "{wp:post_author_email}":"Post Author Email",
            "{post_meta:YOUR_META_KEY}":"Post Meta",
            "{wp:user_id}":"User ID",
            "{wp:user_first_name}":"User First Name",
            "{wp:user_last_name}":"User Last Name",
            "{wp:user_display_name}":"User Display Name",
            "{wp:user_email}":"User Email",
            "{wp:user_url}":"User URL",
            "{user_meta:YOUR_META_KEY}":"User Meta",
            "{wp:site_title}":"Site Title",
            "{wp:site_url}":"Site URL",
            "{wp:admin_email}":"Admin Email"
         }
      },
      {
         "title":"Other",
         "shortcodes":{
            "{querystring:YOUR_KEY}":"Query String",
            "{other:date}":"Date",
            "{other:time}":"Time",
            "{other:user_ip}":"User IP Address"
         }
      }
   ],
   "inputs":{
      "customer_name":{
         "element":"customer_name",
         "admin_label":"Name",
         "options":[
            
         ],
         "attributes":{
            "name":"Name",
            "code":"{input.customer_name}",
            "type":"customer_name"
         }
      },
      "customer_email":{
         "element":"customer_email",
         "admin_label":null,
         "options":[
            
         ],
         "attributes":{
            "name":"Email Address",
            "code":"{input.customer_email}",
            "type":"customer_email"
         }
      }
   },
   "merge_fields":false
}
```

This endpoint retrieves all integration settings of a form.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |


## Delete an Integration of a form


```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration/settings" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: DELETE"
```

> The first command returns JSON structured like this:

```json
{
     "message": "Selected integration feed successfully deleted",

}
```

This endpoint delete an integration feed of a form upon providing `form id` and `integration_id`

### Http request

`DELETE https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration/settings`

### URL parameters

| Parameter      | type | Required | Description                            |
| -------------- | ---- | -------- | -------------------------------------- |
| id             | int  | true     | The `form id`                          |
| integration_id | int  | true     | The integration id of the integration. |



## Get slack integration settings of a form

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration/slack" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
   "settings": [],
    "id": 0
}
```

This endpoint retreives slack integration settings of a form. If there is a slack integration.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration/slack"`

### URL parameters


| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |


## Get webhooks

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integration/slack" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: POST"
```

> The first command returns JSON structured like this:

```json
{
   "success":true,
   "data":{
      "integrations":[
         
      ],
      "request_headers":[
         {
            "label":"Accept",
            "value":"Accept",
            "possible_values":{
               "title":"Accept Header Samples",
               "shortcodes":{
                  "Accept: text/plain":"text/plain",
                  "Accept: text/html":"text/html",
                  "Accept: text/*":"text/*"
               }
            }
         },
         {
            "label":"Accept-Charset",
            "value":"Accept-Charset",
            "possible_values":{
               "title":"Accept-Charset Header Samples",
               "shortcodes":{
                  "Accept-Charset: utf-8":"utf-8",
                  "Accept-Charset: iso-8859-1":"iso-8859-1"
               }
            }
         },
         {
            "label":"Accept-Encoding",
            "value":"Accept-Encoding",
            "possible_values":{
               "title":"Accept-Encoding Header Samples",
               "shortcodes":{
                  "Accept-Encoding: gzip":"gzip",
                  "Accept-Encoding: compress":"compress",
                  "Accept-Encoding: deflate":"deflate",
                  "Accept-Encoding: br":"br",
                  "Accept-Encoding: identity":"identity",
                  "Accept-Encoding: *":"*"
               }
            }
         },
         {
            "label":"Accept-Language",
            "value":"Accept-Language",
            "possible_values":{
               "title":"Accept-Language Header Samples",
               "shortcodes":{
                  "Accept-Language: en":"en",
                  "Accept-Language: en-US":"en-US",
                  "Accept-Language: en-GR":"en-GR",
                  "Accept-Language: en-US,en;q=0.5":"en-US,en;q=0.5"
               }
            }
         },
         {
            "label":"Accept-Datetime",
            "value":"Accept-Datetime"
         },
         {
            "label":"Authorization",
            "value":"Authorization"
         },
         {
            "label":"Cache-Control",
            "value":"Cache-Control"
         },
         {
            "label":"Connection",
            "value":"Connection"
         },
         {
            "label":"Cookie",
            "value":"Cookie"
         },
         {
            "label":"Content-Length",
            "value":"Content-Length"
         },
         {
            "label":"Content-Type",
            "value":"Content-Type"
         },
         {
            "label":"Date",
            "value":"Date"
         },
         {
            "label":"Expect",
            "value":"Expect"
         },
         {
            "label":"Forwarded",
            "value":"Forwarded"
         },
         {
            "label":"From",
            "value":"From"
         },
         {
            "label":"Host",
            "value":"Host"
         },
         {
            "label":"If-Match",
            "value":"If-Match"
         },
         {
            "label":"If-Modified-Since",
            "value":"If-Modified-Since"
         },
         {
            "label":"If-None-Match",
            "value":"If-None-Match"
         },
         {
            "label":"If-Range",
            "value":"If-Range"
         },
         {
            "label":"If-Unmodified-Since",
            "value":"If-Unmodified-Since"
         },
         {
            "label":"Max-Forwards",
            "value":"Max-Forwards"
         },
         {
            "label":"Origin",
            "value":"Origin"
         },
         {
            "label":"Pragma",
            "value":"Pragma"
         },
         {
            "label":"Proxy-Authorization",
            "value":"Proxy-Authorization"
         },
         {
            "label":"Range",
            "value":"Range"
         },
         {
            "label":"Referer",
            "value":"Referer"
         },
         {
            "label":"TE",
            "value":"TE"
         },
         {
            "label":"User-Agent",
            "value":"User-Agent"
         },
         {
            "label":"Upgrade",
            "value":"Upgrade"
         },
         {
            "label":"Via",
            "value":"Via"
         },
         {
            "label":"Warning",
            "value":"Warning"
         }
      ],
      "inputs":{
         "customer_name":{
            "element":"customer_name",
            "admin_label":"Name",
            "options":[
               
            ],
            "attributes":{
               "name":"Name",
               "code":"{input.customer_name}",
               "type":"customer_name"
            }
         },
         "customer_email":{
            "element":"customer_email",
            "admin_label":null,
            "options":[
               
            ],
            "attributes":{
               "name":"Email Address",
               "code":"{input.customer_email}",
               "type":"customer_email"
            }
         }
      }
   }
}
```

This endpoint retreives all the webhooks settings of form.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/webhook`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |


## Delete webhook

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/webhook" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: DELETE"
```

> The first command returns JSON structured like this:

```json
{
   "message": "Selected WebHook Feed is deleted",
}
```

This endpoint delete a webhook feed from a form.

### Http request

`DELETE https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/webhook`

### URL parameters

| Parameter | type | Required | Description                                           |
| --------- | ---- | -------- | ----------------------------------------------------- |
| id        | int  | true     | The `form id`                                         |
| id        | int  | true     | The webhook `settings id` , provide with the request. |



## Get Zapier notification settings

``php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/zapier" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
   "data":[
      
   ],
   "inputs":{
      "customer_name":{
         "element":"customer_name",
         "admin_label":"Name",
         "options":[
            
         ],
         "attributes":{
            "name":"Name",
            "code":"{input.customer_name}",
            "type":"customer_name"
         }
      },
      "customer_email":{
         "element":"customer_email",
         "admin_label":null,
         "options":[
            
         ],
         "attributes":{
            "name":"Email Address",
            "code":"{input.customer_email}",
            "type":"customer_email"
         }
      }
   }
}
```

This endpoint retreives all zapier settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/zapier`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |

## Delete zapier notification settin

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/webhook" \
  -H "Authorization: BASIC USERNAME:APPLICATION_PASSWORD"
  -H "Request type: DELETE"
```

> The first command returns JSON structured like this:

```json
{
   "message": "Deleted successfully!",
}
```

This endpoint delete a webhook feed from a form.

### Http request

`DELETE https://yourdomain.com/wp-json/wppayform/v2/form/{id}/integrations/webhook`

### URL parameters

| Parameter | type | Required | Description                                                       |
| --------- | ---- | -------- | ----------------------------------------------------------------- |
| id        | int  | true     | The `form id`                                                     |
| meta_id   | int  | true     | The zapier notification `settings id` , provide with the request. |