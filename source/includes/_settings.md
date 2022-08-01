# Form Settings

## Get Form settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```
> The first command returns JSON structured like this:

```json
{
   "confirmation_settings":{
      "confirmation_type":"custom",
      "redirectTo":"samePage",
      "customUrl":"",
      "messageToShow":"<p>Form has been successfully submitted</p>",
      "samePageFormBehavior":"hide_form"
   },
   "receipt_settings":{
      "receipt_header":"Thanks for your submission. Here are the details of your submission:",
      "receipt_footer":"",
      "info_modules":{
         "input_details":"yes",
         "payment_info":"yes"
      }
   },
   "currency_settings":{
      "currency":"USD",
      "locale":"auto",
      "currency_sign_position":"left",
      "currency_separator":"dot_comma",
      "decimal_points":0,
      "settings_type":"global",
      "is_zero_decimal":false
   },
   "editor_shortcodes":{
      "submission":{
         "title":"Submission Info",
         "placeholders":{
            "submission.id":{
               "tag":"{submission.id}",
               "label":"Submission ID",
               "callback":null
            },
            "submission.submission_hash":{
               "tag":"{submission.submission_hash}",
               "label":"Submission Hash ID",
               "callback":null
            },
            "submission.customer_name":{
               "tag":"{submission.customer_name}",
               "label":"Customer Name",
               "callback":null
            },
            "submission.customer_email":{
               "tag":"{submission.customer_email}",
               "label":"Customer Email",
               "callback":null
            },
            "submission.payment_method":{
               "tag":"{submission.payment_method}",
               "label":"Payment Method",
               "callback":null
            },
            "submission.all_input_field_html":{
               "tag":"{submission.all_input_field_html}",
               "label":"All Input Field",
               "callback":null
            },
            "submission.all_input_field_html_with_empty":{
               "tag":"{submission.all_input_field_html_with_empty}",
               "label":"All Input Field With Empty Fields",
               "callback":null
            },
            "submission.payment_receipt":{
               "tag":"{submission.payment_receipt}",
               "label":"Payment Receipt",
               "callback":null
            }
         }
      },
      "input":{
         "title":"Inputs",
         "placeholders":{
            "input.customer_name":{
               "tag":"{input.customer_name}",
               "label":"Name",
               "callback":null
            },
            "input.customer_email":{
               "tag":"{input.customer_email}",
               "label":"Email Address",
               "callback":null
            }
         }
      },
      "payment":{
         "title":"Payment Items",
         "placeholders":[
            
         ]
      },
      "wp":{
         "title":"WordPress",
         "placeholders":{
            "post_id":{
               "id":"id",
               "tag":"{wp:post_id}",
               "label":"Post ID",
               "callback":"post_id"
            },
            "post_title":{
               "id":"title",
               "tag":"{wp:post_title}",
               "label":"Post Title",
               "callback":"post_title"
            },
            "post_url":{
               "id":"url",
               "tag":"{wp:post_url}",
               "label":"Post URL",
               "callback":"post_url"
            },
            "post_author":{
               "id":"author",
               "tag":"{wp:post_author}",
               "label":"Post Author",
               "callback":"post_author"
            },
            "post_author_email":{
               "id":"author_email",
               "tag":"{wp:post_author_email}",
               "label":"Post Author Email",
               "callback":"post_author_email"
            },
            "post_meta":{
               "id":"post_meta",
               "tag":"{post_meta:YOUR_META_KEY}",
               "label":"Post Meta",
               "callback":null
            },
            "user_id":{
               "id":"user_id",
               "tag":"{wp:user_id}",
               "label":"User ID",
               "callback":"user_id"
            },
            "user_first_name":{
               "id":"first_name",
               "tag":"{wp:user_first_name}",
               "label":"User First Name",
               "callback":"user_first_name"
            },
            "user_last_name":{
               "id":"last_name",
               "tag":"{wp:user_last_name}",
               "label":"User Last Name",
               "callback":"user_last_name"
            },
            "user_display_name":{
               "id":"display_name",
               "tag":"{wp:user_display_name}",
               "label":"User Display Name",
               "callback":"user_display_name"
            },
            "user_email":{
               "id":"user_email",
               "tag":"{wp:user_email}",
               "label":"User Email",
               "callback":"user_email"
            },
            "user_url":{
               "id":"user_url",
               "tag":"{wp:user_url}",
               "label":"User URL",
               "callback":"user_url"
            },
            "user_meta":{
               "id":"user_meta",
               "tag":"{user_meta:YOUR_META_KEY}",
               "label":"User Meta",
               "callback":null
            },
            "site_title":{
               "id":"site_title",
               "tag":"{wp:site_title}",
               "label":"Site Title",
               "callback":"site_title"
            },
            "site_url":{
               "id":"site_url",
               "tag":"{wp:site_url}",
               "label":"Site URL",
               "callback":"site_url"
            },
            "admin_email":{
               "id":"admin_email",
               "tag":"{wp:admin_email}",
               "label":"Admin Email",
               "callback":"admin_email"
            }
         }
      },
      "other":{
         "title":"Other",
         "placeholders":{
            "querystring":{
               "tag":"{querystring:YOUR_KEY}",
               "label":"Query String",
               "callback":null
            },
            "date":{
               "id":"date",
               "tag":"{other:date}",
               "label":"Date",
               "callback":"system_date"
            },
            "time":{
               "id":"time",
               "tag":"{other:time}",
               "label":"Time",
               "callback":"system_time"
            },
            "ip":{
               "id":"ip",
               "tag":"{other:user_ip}",
               "label":"User IP Address",
               "callback":"user_ip"
            }
         }
      }
   },
   "currencies":{
      "AED":"United Arab Emirates Dirham",
      "AFN":"Afghan Afghani",
      "ALL":"Albanian Lek"
   },
   "locales":{
      "":"English (en) (default)",
      "auto":"Auto-detect locale",
      "zh":"Simplified Chinese (zh)",
      "da":"Danish (da)",
      "nl":"Dutch (nl)",
      "fi":"Finnish (fi)",
      "fr":"French (fr)",
      "de":"German (de)",
      "it":"Italian (it)",
      "ja":"Japanese (ja)",
      "no":"Norwegian (no)",
      "es":"Spanish (es)",
      "sv":"Swedish (sv)"
   },
   "pages":[
      {
         "ID":"2",
         "post_title":"Sample Page"
      },
      {
         "ID":"5",
         "post_title":"Payment Confirmation"
      },
      {
         "ID":"6",
         "post_title":"Payment Failed"
      }
   ],
   "recaptcha_settings":{
      "recaptcha_version":"none",
      "site_key":"",
      "secret_key":"",
      "all_forms":"no"
   },
   "form_recaptcha_status":""
}
```

This endpoint retrieves all the related settings of a form.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |

## Save Form settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```
> The first command returns JSON structured like this:

```json
{
    "message": "Settings successfully updated"
}
```

This endpoint saves the settings of a form.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings`

### URL parameters

| Parameter             | type        | Required | Description                               |
| --------------------- | ----------- | -------- | ----------------------------------------- |
| id                    | int         | true     | The `form id`                             |
| confirmation_settings | json | false    | After form `submit confirmation settings` |
| currency_settings     | json | false    | `Currency settings` of the form           |
| form_recaptcha_status | text        | false    | `Receptcha status` of the form            |
| receipt_settings      | json | false    | `Receipt settings` of the form            |

## Get Form design settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings/design" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```
> The first command returns JSON structured like this:

```json
{
    "layout_settings": {
        "labelPlacement": "top",
        "asteriskPlacement": "none",
        "submit_button_position": "left",
        "extra_styles": {
            "wpf_default_form_styles": "yes",
            "wpf_bold_labels": "no"
        }
    }
}
```

This endpoint retreives all the design settings of a form.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings/design`

### URL parameters

| Parameter | type | Required | Description   |
| --------- | ---- | -------- | ------------- |
| id        | int  | true     | The `form id` |


## Save Form design settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings/design" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```
> The first command returns JSON structured like this:

```json
{
    "message": "Settings successfully updated"
}
```

This endpoitn save the design settings of a form.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/form/{id}/settings/design`

### URL parameters

| Parameter       | type        | Required | Description                                                                                      |
| --------------- | ----------- | -------- | ------------------------------------------------------------------------------------------------ |
| id              | int         | true     | The `form id`                                                                                    |
| layout_settings | json | true     | Layout settings like `labelPlacement: top, asteriskPlacement: none, submit_button_position:left` |

# Global Settings

## Get currency settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
    "currency_settings": {
        "currency": "USD",
        "locale": "auto",
        "currency_sign_position": "left",
        "currency_separator": "dot_comma",
        "decimal_points": 0,
        "settings_type": "global",
        "is_zero_decimal": false
        },
    "currencies": {
        "AED": "United Arab Emirates Dirham",
        "AFN": "Afghan Afghani",
        "ALL": "Albanian Lek",
        "AMD": "Armenian Dram",
        "ANG": "Netherlands Antillean Gulden",
        "AOA": "Angolan Kwanza",
        "ARS": "Argentine Peso",
        "AUD": "Australian Dollar",
        "AWG": "Aruban Florin",
        "AZN": "Azerbaijani Manat",
        "BAM": "Bosnia & Herzegovina Convertible Mark",
        "BBD": "Barbadian Dollar",
        "BDT": "Bangladeshi Taka",
        "BIF": "Burundian Franc",
        "BGN": "Bulgarian Lev",
        "BMD": "Bermudian Dollar",
        "BND": "Brunei Dollar",
        "BOB": "Bolivian Boliviano",
        "BRL": "Brazilian Real",
        "BSD": "Bahamian Dollar",
        "BWP": "Botswana Pula",
        "BZD": "Belize Dollar",
        "CAD": "Canadian Dollar",
        "CDF": "Congolese Franc",
        "CHF": "Swiss Franc",
        "CLP": "Chilean Peso",
        "CNY": "Chinese Renminbi Yuan",
        "COP": "Colombian Peso",
        "CRC": "Costa Rican Colón",
        "CVE": "Cape Verdean Escudo",
        "CZK": "Czech Koruna",
        "DJF": "Djiboutian Franc",
        "DKK": "Danish Krone",
        "DOP": "Dominican Peso",
        "DZD": "Algerian Dinar",
        "EGP": "Egyptian Pound",
        "ETB": "Ethiopian Birr",
        "EUR": "Euro",
        "FJD": "Fijian Dollar",
        "FKP": "Falkland Islands Pound",
        "GBP": "British Pound",
        "GEL": "Georgian Lari",
        "GIP": "Gibraltar Pound",
        "GMD": "Gambian Dalasi",
        "GNF": "Guinean Franc",
        "GTQ": "Guatemalan Quetzal",
        "GYD": "Guyanese Dollar",
        "HKD": "Hong Kong Dollar",
        "HNL": "Honduran Lempira",
        "HRK": "Croatian Kuna",
        "HTG": "Haitian Gourde",
        "HUF": "Hungarian Forint",
        "IDR": "Indonesian Rupiah",
        "ILS": "Israeli New Sheqel",
        "INR": "Indian Rupee",
        "ISK": "Icelandic Króna",
        "JMD": "Jamaican Dollar",
        "JPY": "Japanese Yen",
        "KES": "Kenyan Shilling",
        "KGS": "Kyrgyzstani Som",
        "KHR": "Cambodian Riel",
        "KMF": "Comorian Franc",
        "KRW": "South Korean Won",
        "KYD": "Cayman Islands Dollar",
        "KZT": "Kazakhstani Tenge",
        "LAK": "Lao Kip",
        "LBP": "Lebanese Pound",
        "LKR": "Sri Lankan Rupee",
        "LRD": "Liberian Dollar",
        "LSL": "Lesotho Loti",
        "MAD": "Moroccan Dirham",
        "MDL": "Moldovan Leu",
        "MGA": "Malagasy Ariary",
        "MKD": "Macedonian Denar",
        "MNT": "Mongolian Tögrög",
        "MOP": "Macanese Pataca",
        "MRO": "Mauritanian Ouguiya",
        "MUR": "Mauritian Rupee",
        "MVR": "Maldivian Rufiyaa",
        "MWK": "Malawian Kwacha",
        "MXN": "Mexican Peso",
        "MYR": "Malaysian Ringgit",
        "MZN": "Mozambican Metical",
        "NAD": "Namibian Dollar",
        "NGN": "Nigerian Naira",
        "NIO": "Nicaraguan Córdoba",
        "NOK": "Norwegian Krone",
        "NPR": "Nepalese Rupee",
        "NZD": "New Zealand Dollar",
        "PAB": "Panamanian Balboa",
        "PEN": "Peruvian Nuevo Sol",
        "PGK": "Papua New Guinean Kina",
        "PHP": "Philippine Peso",
        "PKR": "Pakistani Rupee",
        "PLN": "Polish Złoty",
        "PYG": "Paraguayan Guaraní",
        "QAR": "Qatari Riyal",
        "RON": "Romanian Leu",
        "RSD": "Serbian Dinar",
        "RUB": "Russian Ruble",
        "RWF": "Rwandan Franc",
        "SAR": "Saudi Riyal",
        "SBD": "Solomon Islands Dollar",
        "SCR": "Seychellois Rupee",
        "SEK": "Swedish Krona",
        "SGD": "Singapore Dollar",
        "SHP": "Saint Helenian Pound",
        "SLL": "Sierra Leonean Leone",
        "SOS": "Somali Shilling",
        "SRD": "Surinamese Dollar",
        "STD": "São Tomé and Príncipe Dobra",
        "SVC": "Salvadoran Colón",
        "SZL": "Swazi Lilangeni",
        "THB": "Thai Baht",
        "TJS": "Tajikistani Somoni",
        "TOP": "Tongan Paʻanga",
        "TRY": "Turkish Lira",
        "TTD": "Trinidad and Tobago Dollar",
        "TWD": "New Taiwan Dollar",
        "TZS": "Tanzanian Shilling",
        "UAH": "Ukrainian Hryvnia",
        "UGX": "Ugandan Shilling",
        "USD": "United States Dollar",
        "UYU": "Uruguayan Peso",
        "UZS": "Uzbekistani Som",
        "VND": "Vietnamese Đồng",
        "VUV": "Vanuatu Vatu",
        "WST": "Samoan Tala",
        "XAF": "Central African Cfa Franc",
        "XCD": "East Caribbean Dollar",
        "XOF": "West African Cfa Franc",
        "XPF": "Cfp Franc",
        "YER": "Yemeni Rial",
        "ZAR": "South African Rand",
        "ZMW": "Zambian Kwacha"
    },
    "locales": {
        "": "English (en) (default)",
        "auto": "Auto-detect locale",
        "zh": "Simplified Chinese (zh)",
        "da": "Danish (da)",
        "nl": "Dutch (nl)",
        "fi": "Finnish (fi)",
        "fr": "French (fr)",
        "de": "German (de)",
        "it": "Italian (it)",
        "ja": "Japanese (ja)",
        "no": "Norwegian (no)",
        "es": "Spanish (es)",
        "sv": "Swedish (sv)"
        },
    "ip_logging_status": "yes",
    "honeypot_status": "yes",
    "abandoned_time": 3
}
```

This endpoint return global currecny settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies`

## Save global currency settings


```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

> The first command returns JSON structured like this:

```json
{
    "message": "Successfully updated settings"
}
```

This endpoint saves global currency settings.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies`

### URL parameters

| Parameter            | type        | Required | Description           |
| -------------------- | ----------- | -------- | --------------------- |
| settings | json object | true     | The currency settings | `settings` object has `currency` field


## Get access roles

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
    "roles": {
        "capability": [],
        "roles": []
    }
}
```

This endpoint gets access roles.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/settings/rules`

## Set access roles

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

> The first command returns JSON structured like this:

```json
{
   "message": "Successfully updated the role(s)."
}
```

This endpoint set global roles.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/forms/settings/rules`

### URL paramaters

| Parameter  | type  | Required | Description                           |
| ---------- | ----- | -------- | ------------------------------------- |
| capability | array | true     | The capabilities : `admin, moderator` |


## Get stripe settings

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
        "test_pub_key": "pk_test_8cp7uwcwXqjYxowDJnuNH8az",
        "test_secret_key": "sk_test_R1ANXvGZyZ1omGhmXXRUIVul",
        "company_name": "",
        "checkout_logo": "",
        "send_meta_data": "no"
    },
    "webhook_url": "https://wp.test/?wpf_stripe_listener=1",
    "is_key_defined": false
}
```

This endpoint return stripe settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/settings/stripe`

## Save stripe settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/stripe" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

> The first command returns JSON structured like this:

```json
{
   "message": "Settings successfully updated"
}
```

This endpoint save stripe settings.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/forms/settings/stripe`

### URL parameters

| Parameter | type        | Required | Description                                                                                    |
| --------- | ----------- | -------- | ---------------------------------------------------------------------------------------------- |
| settings  | json | true     | The settings - `payment_mode, test_public_key, test_secret_key, live_pub_key, live_secret_key` |

## Get integrations 

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/integrations" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
  "success": false,
  "data": {
    "settings": [],
    "settings_key": "",
    "message": "Sorry! No integration failed found with: "
   }
}
```

This endpoint return all global integration addons.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/settings/integrations`



# License

## license settings

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/license" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The first command returns JSON structured like this:

```json
{
    "price_id": "",
    "expires": "",
    "status": "unregistered",
    "purchase_url": "https://wpmanageninja.com/downloads/wppayform-pro-wordpress-payments-form-builder/"
}
```

This endpoint returns the License settings.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/license`

## Save/Update license

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/license" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

> The first command returns JSON structured like this:

```json
{
    "message" : "Your license key has been successfully updated"
}
```

This endpoint saves/updates license.

### Http request

`POST https://yourdomain.com/wp-json/wppayform/v2/license`

### URL parameters


| Parameter   | type   | Required | Description                             |
| ----------- | ------ | -------- | --------------------------------------- |
| license_key | string | true     | The given license key after purchasing. |

## Deactivate license

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/license" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: DELETE"
```

> The first command returns JSON structured like this:

```json
{
    "message" : "Your license key has been successfully deactivated"
}
```

This endpoint deactivate license.

### Http request

`DELETE https://yourdomain.com/wp-json/wppayform/v2/license`


