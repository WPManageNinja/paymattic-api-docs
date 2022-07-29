# Reports

## Get reports

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/reports" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The above command returns JSON structured like this:

```json
{
    "payments": [
        {
            "id": 1,
            "form_id": "8",
            "customer_name": "tupsfrXOcd",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-27 07:29:30",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 60,
            "form_id": "8",
            "customer_name": "F3tkI6NQcC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 11:07:00",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 59,
            "form_id": "29",
            "customer_name": "3pMcTkn2Jp",
            "payment_total": "23954600",
            "payment_status": "pending",
            "payment_method": "stripe",
            "updated_at": "2022-07-21 10:41:56",
            "post_title": "Credit Card Donation Form (#29)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;239,546"
        },
        {
            "id": 58,
            "form_id": "29",
            "customer_name": "IA4IGMhVEY",
            "payment_total": "16659000",
            "payment_status": "paid",
            "payment_method": "stripe",
            "updated_at": "2022-07-21 10:37:25",
            "post_title": "Credit Card Donation Form (#29)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;166,590"
        },
        {
            "id": 57,
            "form_id": "8",
            "customer_name": "87o169SlXC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 09:15:29",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 56,
            "form_id": "8",
            "customer_name": "87o169SlXC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 09:15:00",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 55,
            "form_id": "8",
            "customer_name": "87o169SlXC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 09:14:42",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 54,
            "form_id": "8",
            "customer_name": "87o169SlXC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 09:14:25",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 53,
            "form_id": "8",
            "customer_name": "87o169SlXC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 09:14:07",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        },
        {
            "id": 52,
            "form_id": "8",
            "customer_name": "87o169SlXC",
            "payment_total": "0",
            "payment_status": "pending",
            "payment_method": "",
            "updated_at": "2022-07-21 09:13:33",
            "post_title": "Contact Form (#8)",
            "recurring_amount": null,
            "initial_amount": null,
            "quantity": null,
            "status": null,
            "formattedTotal": "&#36;0"
        }
    ],
    "customer": {
        "yptn5@a7tw.com": {
            "count": 1,
            "items": [
                {
                    "currency": "USD",
                    "total_paid": 166590,
                    "submissions": "1"
                }
            ],
            "name": "IA4IGMhVEY"
        }
    },
    "currency_base": [
        {
            "currency": "USD",
            "form_id": "29",
            "total_paid": "16659000",
            "formattedTotal": "&#36;166,590"
        }
    ],
    "chart": {
        "labels": [],
        "data": [
            166590
        ],
        "label": [
            "USD"
        ]
    },
    "entries_count": 60
}
```

This endpoint retreives whole reports in a json format.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/reports`

## Get Todays data

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/reports/todays-data" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The above command returns JSON structured like this:

```json
{
    "revenueWeekly": {
        "id": "revenue_overview",
        "title": "Revenue This Week",
        "type": "bar",
        "height": "70",
        "value": [
            {
                "form_id": "0",
                "currency": "USD",
                "total_paid": "0",
                "formattedTotal": "0 USD"
            }
        ],
        "change": "",
        "label": [],
        "data": [],
        "color": "rgb(22,198,114)",
        "backgroundColor": "rgb(233,247,239)"
    },
    "customersStats": [
        {
            "id": "total_customers",
            "title": "Total Customers",
            "type": "line",
            "height": "70",
            "value": 1,
            "change": "0% of last week",
            "label": [
                "2022-07-21"
            ],
            "data": [
                "1"
            ],
            "color": "rgb(255,184,36)",
            "backgroundColor": "rgb(254,245,232)"
        },
        {
            "id": "customer_new",
            "title": "New Customers",
            "type": "line",
            "height": "70",
            "value": "0/week",
            "change": "-100% of last week",
            "label": [
                1,
                2,
                3,
                4,
                5,
                6
            ],
            "data": [
                -100,
                -200,
                -300,
                -400,
                -500,
                -600
            ],
            "color": "rgb(192 161 232)",
            "backgroundColor": "rgb(233 220 250)"
        }
    ]
}
```

This endpoint retrieves Todays reports with customer stats.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/reports/todays-data`

## Recent revenues

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/reports/recent-revenues" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The above command returns JSON structured like this:

```json
{
    "data": {
        "USD": [
            {
                "currency": "USD",
                "payment_status": "paid",
                "date": "2022-07-21",
                "total_paid": "166590.00",
                "submissions": "1"
            }
        ]
    },
    "options": [
        {
            "label": "USD",
            "value": "USD"
        }
    ],
    "chartData": {
        "USD": {
            "label": [
                "2022-07-21"
            ],
            "data": [
                166590
            ]
        }
    }
}
```

This endpoint retieves recent revenues reports in a json format.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/reports/recent-revenues`

## Get customers


```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/reports/customers" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> The above command returns JSON structured like this:

```json
{
    "customers": [
        {
            "customer_email": "u4diz@x9w5.com",
            "customer_name": "F3tkI6NQcC",
            "created": "21-July-2022",
            "submissions": "1",
            "date": "8"
        },
        {
            "customer_email": "yptn5@a7tw.com",
            "customer_name": "IA4IGMhVEY",
            "created": "21-July-2022",
            "submissions": "2",
            "date": "8"
        },
        {
            "customer_email": "dxdss@acvt.com",
            "customer_name": "87o169SlXC",
            "created": "21-July-2022",
            "submissions": "7",
            "date": "8"
        },
        {
            "customer_email": "levpd@lmqw.com",
            "customer_name": "ZqxEeuzC9V",
            "created": "20-July-2022",
            "submissions": "2",
            "date": "9"
        },
        {
            "customer_email": "foxvt@vfjo.com",
            "customer_name": "5TilImF7d3",
            "created": "20-July-2022",
            "submissions": "5",
            "date": "9"
        },
        {
            "customer_email": "tozrb@zzou.com",
            "customer_name": "ylW56KzPYU",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "af5pw@sfoe.com",
            "customer_name": "XU53cOkBo1",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "y4cwp@5fjr.com",
            "customer_name": "R0X2OiBCQs",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "snwwo@mp8t.com",
            "customer_name": "FOMg5XM8c4",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "pydbn@6swu.com",
            "customer_name": "U5ivMuDNPX",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "71xyf@cjkx.com",
            "customer_name": "elias",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "ftjdo@lc3y.com",
            "customer_name": "hF0zgFgvpF",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "rk6hy@w1es.com",
            "customer_name": "uh6FJPN0tG",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "yd2z1@x0ui.com",
            "customer_name": "v8uwcheDfK",
            "created": "20-July-2022",
            "submissions": "2",
            "date": "9"
        },
        {
            "customer_email": "nvxww@9nva.com",
            "customer_name": "c9rSdAAwMR",
            "created": "20-July-2022",
            "submissions": "1",
            "date": "9"
        },
        {
            "customer_email": "hm8jr@aw4q.com",
            "customer_name": "r9mtx2UE62",
            "created": "20-July-2022",
            "submissions": "6",
            "date": "9"
        },
        {
            "customer_email": "aehbe@xugp.com",
            "customer_name": "ffeAo0yJqC",
            "created": "20-July-2022",
            "submissions": "7",
            "date": "9"
        },
        {
            "customer_email": "bl2q7@4l1k.com",
            "customer_name": "U564mkHlDu",
            "created": "20-July-2022",
            "submissions": "3",
            "date": "9"
        },
        {
            "customer_email": "xygux@quik.com",
            "customer_name": "Zf77jGvgyw",
            "created": "20-July-2022",
            "submissions": "2",
            "date": "9"
        },
        {
            "customer_email": "1c5jc@k1zw.com",
            "customer_name": "ewu9AeGkIw",
            "created": "20-July-2022",
            "submissions": "9",
            "date": "9"
        },
        {
            "customer_email": "bdbhg@tl1w.com",
            "customer_name": "tupsfrXOcd",
            "created": "20-July-2022",
            "submissions": "5",
            "date": "9"
        }
    ],
    "total": 21
}
```

This endpoint retieves all the customers and their data in a json format.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/reports/customers`

## Get a customer

```php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/reports/customers/{customer_email}" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> This above command return a json structured like this.

```json
{
    "entries": [
        {
            "id": 60,
            "form_id": "8",
            "user_id": "1",
            "customer_id": null,
            "customer_name": "F3tkI6NQcC",
            "customer_email": "u4diz@x9w5.com",
            "form_data_raw": {
                "__wpf_form_id": "8",
                "__wpf_current_url": "http://wp.test/?wp_paymentform_preview=8",
                "__wpf_current_page_id": "",
                "customer_name": "F3tkI6NQcC",
                "customer_email": "u4diz@x9w5.com",
                "text": "JXvcqdQjEy",
                "textarea": "JeEFJyeAoe"
            },
            "form_data_formatted": {
                "customer_name": "F3tkI6NQcC",
                "customer_email": "u4diz@x9w5.com",
                "text": "JXvcqdQjEy",
                "textarea": "JeEFJyeAoe"
            },
            "currency": "USD",
            "payment_status": "pending",
            "submission_hash": "wpf_165840162062d93354e7992251",
            "payment_total": "0",
            "payment_mode": null,
            "payment_method": "",
            "status": "new",
            "ip_address": "127.0.0.1",
            "browser": "Chrome",
            "device": "Apple",
            "city": null,
            "country": null,
            "created_at": "2022-07-21 11:07:00",
            "updated_at": "2022-07-21 11:07:00",
            "has_subscription": false,
            "currency_settings": {
                "currency": "USD",
                "locale": "auto",
                "currency_sign_position": "left",
                "currency_separator": "dot_comma",
                "decimal_points": 0,
                "settings_type": "global",
                "is_zero_decimal": false,
                "currency_sign": "&#36;"
            },
        }
    ],
    "info": {
        "id": 60,
        "form_id": "8",
        "user_id": "1",
        "customer_id": null,
        "customer_name": "F3tkI6NQcC",
        "customer_email": "u4diz@x9w5.com",
        "form_data_raw": {
            "__wpf_form_id": "8",
            "__wpf_current_url": "http://wp.test/?wp_paymentform_preview=8",
            "__wpf_current_page_id": "",
            "customer_name": "F3tkI6NQcC",
            "customer_email": "u4diz@x9w5.com",
            "text": "JXvcqdQjEy",
            "textarea": "JeEFJyeAoe"
        },
        "form_data_formatted": {
            "customer_name": "F3tkI6NQcC",
            "customer_email": "u4diz@x9w5.com",
            "text": "JXvcqdQjEy",
            "textarea": "JeEFJyeAoe"
        },
        "currency": "USD",
        "payment_status": "pending",
        "submission_hash": "wpf_165840162062d93354e7992251",
        "payment_total": "0",
        "payment_mode": null,
        "payment_method": "",
        "status": "new",
        "ip_address": "127.0.0.1",
        "browser": "Chrome",
        "device": "Apple",
        "city": null,
        "country": null,
        "created_at": "2022-07-21 11:07:00",
        "updated_at": "2022-07-21 11:07:00",
        "has_subscription": false,
        "currency_settings": {
            "currency": "USD",
            "locale": "auto",
            "currency_sign_position": "left",
            "currency_separator": "dot_comma",
            "decimal_points": 0,
            "settings_type": "global",
            "is_zero_decimal": false,
            "currency_sign": "&#36;"
        },
    },
    "subscriptions": [],
    "orders": []
}
```

This endpoint retieves all the data of a customer in json format.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/reports/customers/{customer_email}`

### URL parameters

Parameter | Type | Required | Description |
--------- | -----| ----------- | -------- | 
customer_email | string/email | true | The email of the customer.

## Get customer profile

``php

```

```python

```

```shell
curl "https://yourdomain.com/wp-json/wppayform/v2/reports/customers/{customer_email}/profile" \
  -H "Authorization: BASIC API_USERNAME:API_PASSWORD"
  -H "Request type: GET"
```

> This above command return a json structured like this.

```json
{
    "spends": [],
    "permissions": {
        "roles": [
            "subscriber"
        ],
        "user_id": 7,
        "display_name": "u4diz@x9w5.com",
        "manage_user": false
    }
}
```

This endpoint retrieves a customer's profile.

### Http request

`GET https://yourdomain.com/wp-json/wppayform/v2/reports/customers/{customer_email}/profile`

### URL parameters

Parameter | Type | Required | Description |
--------- | -----| ----------- | -------- | 
customer_email | string/email | true | The email of the customer.