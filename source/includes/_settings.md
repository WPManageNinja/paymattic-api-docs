# Form Settings

## Get Form settings

## Save Form settings


## Get Form design settings


## Save Form design settings



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

```javascript

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

```javascript

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

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
settings[`currecny`] | json string | true | The currency settings


## Get acces rules

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

```javascript

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

This endpoint gets acces rules.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/forms/settings/rules`

## Set acces rules

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/forms/settings/currencies" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: POST"
```

```javascript

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

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
capability | array | true | The capabilities


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

```javascript

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

```javascript

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

Parameter | type | Required | Description
--------- | ---- | -------- | -----------
settings | json string | true | The settings - `payment_mode, test_public_key, test_secret_key, live_pub_key, live_secret_key`

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

