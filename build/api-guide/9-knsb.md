I. Get an authentication token
----------------------------------------------------------------------------------
POST
```
{
    "email": "ACCOUNT EMAIL",
    "password": "ACCOUNT PASSWORD"
}
```
to `https://api-v2.mookh.com/users/login/`. The response has a `token` parameter. Use authentication header format `Bearer TOKEN_STRING` when needed to access authenticated resources.

II. Order Processing Payload
----------------------------------------------------------------------------------
To process a KNSB order
POST
```
{
    "customer": {
        "name": "Guardian Name Here",
        "email": "register@kenyaspellingbee.com"
        "phone_number": "+2547xxxxxxxx"
    },
    "registration_data": {
        "student_first_name": "Pupil First Name Here",
        "student_last_name": "Pupil Last Name Here",
        "student_class": "Pupil Class Here",
        "school_name": "Name of School Here"
    },
    "order_detail": [
        {
            "item_id": "b5dbbcc8-3ade-4cfd-9cd4-60de38860d2a",
            "type_name": "services.registration",
            "item_quantity": 1
        }
    ],
    "order_channel": "BOT",
    "currency": "KES",
    "payment_method": "MOBILE",
    "payment_installments": 1,
    "promotional_code": null,
    "is_pay_later": false
}
```
to `https://api-v2.mookh.com/stores/orders/`

NB: 

1. `Bearer TOKEN_STRING` is NOT required to process an order.

2. Modify `customer` and `registration_data` objects appropriately. You can work with the other fields as they are.

3. Set `is_pay_later=true` in case you want to inhibit automatic payment process initiation.

III. Prompting STK Push
----------------------------------------------------------------------------------
Creating an order using step II above by default sends out an STK prompt to the customer phone number. However, you can also re-initiate the payment process for an already existing order later.

POST
```
{
    "order_number": "ORDER NUMBER"
}
```
to `https://api-v2.mookh.com/stores/orders/pay/`.

IV. Pupil Database
----------------------------------------------------------------------------------
To list entries of the pupil's database, do a GET request to `https://api-v2.mookh.com/services/registration-data/` . Be sure to add an authentication token header with the format `Bearer TOKEN_STRING`.
