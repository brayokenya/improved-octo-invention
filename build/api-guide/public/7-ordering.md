An order is composed of the following main sections;

1. Customer details (Required)
2. Payer information (Optional)
3. List of items (Required)
4. Ordering details

## 1. Customer Details
Customer information includes **name**, **phone_number** and **email** of the recipient of the purchase
```
{
    "name": "string",
    "email": "string",
    "phone_number": "string"
}
```
## 2. Payer Information
Payer information includes **name**, **phone_number** and **email** of the person to be billed for the order. The part of the order is optional. In absence of payer information, the customer information will be used in billing.
```
{
    "name": "string",
    "email": "string",
    "phone_number": "string"
}
```

## 3. List of Items
List of items makes up the items (tickets, music, ebooks) that a customer intends to purchase.
The simplest item payload structure consists of **item_id**, **type_name** and **item_quantity**

```
{
    "item_id": "<UUID of Item>",
    "type_name": "string",
    "item_quantity": "integer"
}
```

### 3.1. Additional Item fields
Depending on the type of item or customer choice, additional fields may be supplied. These include **promotional_code**, **ticket_names**, **data_entries**

1. **promotional_code** (string) - Allows a customer to provide a promo code issued by merchant who owns the particular item or otherwise.
2. **ticket_names** (string array) - For ticket purchases only. This optional field allows the customer to dictate what names will appear on there tickets. This list of names need not be equal to quantity specified.
3. **data_entries** (object) - For tickets only. In case an event organizer requires potential attendees to provide information that maybe relevant to an event as deemed fit, the entries are supplied using this field.
Item payload with additional optional fields.

```
{
    "item_id": "string",
    "type_name": "string",
    "item_quantity": "integer",
    "ticket_names": "array",
    "promotional_code": "string",
    "data_entries": "object"
}
```

## 4. Ordering details
These are additional required or optional fields that dictate how an order is processed. These fields are;

1. **currency**            - (Required) Customer"s preferred currency of payment. The currency must be supported for all items in the order.
2. **payment_method**       - (Required) Chosen payment method. Publicly available payment methods include MOBILE, CARD and CASH. Some payment options are available for authenticated Mookh agents e.g. MOBILE_CASH
3. **agent**                - (Optional, required only for POS payment options) For POS devices only. This is the UUID of agent placing the order. The agent will receive an SMS upon the order being completed and paid for.
4. **response_type**        - (Optional) Options are **json** or **html** (default **html**) for non CARD payment orders or depending on API client.
5. **exact_payment_method** - (Optional) Specific payment method. Options differ from one country to another. Example for MOBILE payment in Kenya options are **MPESA** and **AIRTEL** which in Uganda options are **MTNUG** and **AIRTELUG**.
6. **is_pay_later**         - (Optional, default false) set to **true** if customer wished to pay later. An SMS and email with payment instructions is sent after an order is successfully generated.
7. **payment_installments** - (Optional, default 1) set the number of installments a customer wishes to pay the order in. This option instructs the system to send out periodic notifications detailing when the next installment is due and when the order will expire. Generally installment orders expire 48hours after being generated on condition that the customer is unable to complete payment. After expiry any paid amount will be refunded. 

## 5. Create and order
Endpoint `/stores/orders/`

Auth Required: **False**, **True** for POS orders.

Roles Required: `[subjective]`

Request body
```
{
    "currency": "KES", 
    "payment_method": "MOBILE", 
    "exact_payment_method": null, 
    "agent": null, 
    "is_pay_later": false, 
    "payment_installments": 1, 
    "response_type": "json", 
    "customer": {
        "name": "Jane Doe",
        "email": "jane@doe.com",
        "phone_number": "+254720111222"
    },
    "payer": {
        "name": "Jane Doe",
        "email": "jane@doe.com",
        "phone_number": "+254720111222"
    },
    "order_detail": [
        {
    		"item_id": "adf86aa9-fa1c-4394-b0b8-f6a7dea5f9c6",
    		"type_name": "store.ticket",
    		"item_quantity": 2
            "ticket_names": ["Alice", "Bob", "Martin"],
            "promotional_code": "GH02",
            "data_entries": {
                "Age": "27",
                "Preferred T-shirt Color": "Blue",
                "Require Packing?": "Yes"
            }
        },
        {   
    		"item_id": "a1238351-627e-4b92-9991-bfc81d3f820b",
            "type_name": "digital_content.album",
    		"item_quantity": 1
            "promotional_code": "ALB02"
        }
    ]
}
```

Response **response_type**=**json** returns generated order.
```
{
    "id": "b752043a-327b-472f-b970-cb1050fcbbef",
    "customer": {
        "email": "jane@doe.com",
        "name": "Jane Doe",
        "phone_number": "+254720111222"
    },
    "payer": {
        "email": null,
        "name": null,
        "phone_number": null
    },
    "agent": null,
    "order_detail": [
        {
            "id": "623caa78-3d54-47f7-952f-8fc00739a484",
            "name": "Currency track",
            "item_id": "a1238351-627e-4b92-9991-bfc81d3f820b",
            "type_name": "digital_content.album",
            "item_quantity": 1,
            "selling_price": "800.00",
            "promo_amount": "200.00",
            "promo_code": null,
            "album": "a1238351-627e-4b92-9991-bfc81d3f820b",
            "category": "821e0cec-5269-486e-bd9a-4d2e6386f345",
            "category_name": "HipHop",
            "media_type": "f8be3dda-0844-49ba-a215-637c5dd9317f",
            "media_type_name": "ALBUM",
            "description": "<p>Awesome</p>",
            "store_name": "Western Digital",
            "authors": [
                "mtiaji"
            ],
            "thumbnail": "https://mookhfiles.com/uploads/poster.jpg",
            "media_files": [],
            "created": "2020-02-06T22:34:47.574975+03:00",
            "updated": "2020-02-06T22:34:47.625007+03:00"
        },
        {
            "id": "39729b36-4959-4409-ab14-87254a3acae7",
            "name": "VVIP",
            "item_id": "adf86aa9-fa1c-4394-b0b8-f6a7dea5f9c6",
            "type_name": "store.ticket",
            "item_quantity": 2,
            "selling_price": "7500.00",
            "promo_amount": "1500.00",
            "ticket_url": null,
            "promo_code": null,
            "event": "5582bf59-e019-48af-9566-90d3a03e4ca8",
            "event_name": "Mseto Music Show",
            "event_venue": "Nairobi",
            "event_description": "music concert",
            "event_poster": null,
            "event_link": "http://mookh.xyz/event/mseto_show",
            "ticket_name": "VVIP",
            "ticket_description": "Ticket for VVIP customers.",
            "start_date": "2019-03-31T21:00:00Z",
            "end_date": "2019-08-29T21:00:00Z",
            "ticket_files": [],
            "created": "2020-02-06T22:34:47.279799+03:00",
            "updated": "2020-02-06T22:34:47.441263+03:00",
        }
    ],
    "order_status": "PENDING",
    "order_number": "LFG2SL",
    "currency": "KES",
    "short_url": null,
    "order_amount": "8300.00",
    "order_balance": "8300.00",
    "payment_method": "MOBILE",
    "exact_payment_method": "",
    "payment_installments": 3,
    "installments_amount": 2766.0,
    "is_promo_order": false,
    "order_channel": "WEB",
    "registration_data": [],
    "is_mobile_payments": false,
    "payment_reference": null,
    "is_pay_later": false,
    "is_gate_purchase": false,
    "created": "2020-02-06T22:34:47.020025+03:00",
    "updated": "2020-02-06T22:34:47.785995+03:00",
}
```
Response **response_type**=**json** for CARD and Non Kenya orders. Use the response to build a form and submit to the url provided.
```
{
    "pay_response": {
        "is_archived": false,
        "slug": null,
        "status": true,
        "message": "cybersource payload, create a form with the payload below as field names and values, set the action as the url below and post",
        "url": "https://secureacceptance.cybersource.com/pay",
        "payload": {
            "profile_id": "95C874BF-D61F-4A41-B7C1-B537F2C45723",
            "access_key": "add0912e21813639994fb0338262169d",
            "transaction_uuid": "5e3c6da4db277",
            "signed_date_time": "2020-02-06T19:48:52Z",
            "signed_field_names": "profile_id,access_key,transaction_uuid,signed_field_names,unsigned_field_names,signed_date_time,locale,transaction_type,reference_number,auth_trans_ref_no,amount,currency,merchant_descriptor,override_custom_cancel_page,override_custom_receipt_page",
            "unsigned_field_names": "device_fingerprint_id,signature,bill_to_forename,bill_to_surname,bill_to_email,bill_to_phone,bill_to_address_line1,bill_to_address_line2,bill_to_address_city,bill_to_address_state,bill_to_address_country,bill_to_address_postal_code,customer_ip_address,line_item_count,item_0_code,item_0_sku,item_0_name,item_0_quantity,item_0_unit_price,merchant_defined_data1,merchant_defined_data2,merchant_defined_data3,merchant_defined_data4",
            "transaction_type": "sale",
            "reference_number": "E7H28F93RR| ORD-5OGI7",
            "auth_trans_ref_no": null,
            "amount": 2766,
            "currency": "KES",
            "locale": "en-us",
            "merchant_descriptor": "Mookhpay.com",
            "bill_to_forename": "Jane",
            "bill_to_surname": "Doe",
            "bill_to_email": "jane@doe.com",
            "bill_to_phone": "+254720111222",
            "bill_to_address_line1": null,
            "bill_to_address_line2": null,
            "bill_to_address_city": null,
            "bill_to_address_state": null,
            "bill_to_address_country": null,
            "bill_to_address_postal_code": null,
            "override_custom_cancel_page": "https://beta.mookhpay.com/callback/card/cancelled/response?callback_token=wGfAP95KOXqljZjf",
            "override_custom_receipt_page": "https://beta.mookhpay.com/callback/card/complete/response?callback_token=wGfAP95KOXqljZjf",
            "customer_ip_address": "41.79.169.14",
            "line_item_count": 1,
            "item_0_sku": "E7H28F93RR-5e3c6da4db316",
            "item_0_code": "E7H28F93RR",
            "item_0_name": "E7H28F93RR",
            "item_0_quantity": 1,
            "item_0_unit_price": 2334,
            "merchant_defined_data1": "MDD#1",
            "merchant_defined_data2": "MDD#2",
            "merchant_defined_data3": "MDD#3",
            "merchant_defined_data4": "MDD#4",
            "device_fingerprint_id": "",
            "signature": "rpBVviEAm1i4b7+7rRthNot0qpy70Fc0TJEE3CJjZ4w=",
            "created_by": null,
            "updated_by": null,
        }
    },
    "order_number": "VEZHZM"
}
```

Response **response_type**=**html** Use this to receive payment links. Works well in case the API client is unable to compose a form.
```
{
    "link": "https://api-v2.mookh.com/payments/links/f686353f-a22e-4ce7-891d-ec33f825571f/",
    "order_number": "4XS6XY",
    "currency_code": "KES"
}
```

### NOTE:
- **type_name** is a string signature (namespace) that identified the type of item and is available as a property of each object in the public APIs.
- The customer or payer **phone_number** **MUST** be in the international format e.g. +254720123456. 
- The recommended **response_type** for orders that aren"t for Kenyan customers and MOBILE is **html**. As such, the http response will be a link to either [MookhPay](https://checkout.mookhpay.com), MIGS or Cybersource payment gateways.
