Get user details and token

|                     |                |
|:--------------------|:---------------|
| Endpoint            | `/users/login/`|
| **Allowed methods** | [POST]         |

**Request Body**
```
{
    'email': 'john.doe@gmail.com',
    'password': 'password',
}
```
**Response**
```
{
    'token': 'LONG ACCESS TOKEN',
    'user': {
        'first_name': 'John',
        'last_name': 'Doe',
        'email': 'john.doe@gmail.com',
        'phone_number': '+254722123123'
    }
}
```