##Getting Started
To get started with Mookh 2.0 APIs, one needs to have a user account created on the system. The documentation details
how a user account can be created from a developers perspective via available REST APIs and how the created account can 
be used to access resources on the system.

###Registration
Register a user.

Endpoint `/users/register/`

Model description `users.User`

| Name            | Description               | Type     | Length  | Accessibility | Required | Unique  |
| :---------------| :-------------------------| :--------| :-------| :-------------| :--------| :------ |
| first_name      | First name of the user    | String   | 100     | Read / Write  | True     | False   |
| last_name       | Last name of the user     | String   | 100     | Read / Write  | True     | False   |
| email           | Email of the user         | String   | 100     | Read / Write  | True     | True    |
| phone_number    | Phone number of the user  | String   | 100     | Read / Write  | True     | True    |
| profile_photo   | Picture of the user       | String   | 100     | Read / Write  | False    | False   |


**Allowed methods** [POST]

**Request Body**
```
{
    'first_name': 'John',
    'last_name': 'Doe',
    'email': 'john.doe@gmail.com',
    'phone_number': '+254722123123',
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
