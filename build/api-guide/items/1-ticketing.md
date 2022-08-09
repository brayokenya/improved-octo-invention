##Models
Ticketing models include `Event, EventCategory, Ticket, Reservation`

##Events
Model `store.Event`

| Name                     | Description               | Type     | Required |
| :------------------------| :-------------------------| :--------| :--------|
| **event_name**           | Name of event             | String   | True     |
| **event_description**    | Description of event      | String   | True     |
| **event_venue**          | Location of event         | String   | False    |
| **event_category_fk**    | PK of event category      | String   | True     |
| **event_poster**         | URL of event poster       | String   | False    |
| **store_fk**             | PK of event's store       | String   | True     |
| **start_date**           | Start datetime of event   | Datetime | False    |
| **end_date**             | End datetime of event     | Datetime | False    |
| **latitude**             | Latitude of venue         | String   | False    |
| **longitude**            | Longitude of venue        | String   | False    |
| **country**              | Host country of event     | String   | False    |
| **is_free**              | Whether RSVP or not     | Boolean   | False    |
| **is_private**              | Ticket availability    | Boolean   | False    |
| **is_published**              | Merchant activation     | Boolean   | False    |
| **is_published_to_directory** | Admin approval / activation   | Boolean   | False    |
| **is_staff_pic**              | Whether is staff pick or not    | Boolean   | False    |
| **is_featured**               | Whether is feature or not     | Boolean   | False    |
| **staff_pick_start_date**     | Staff pick beginning datetime     | Datetime   | False    |
| **staff_pick_end_date**       | Staff pick ending datetime     | Datetime   | False    |
| **has_complimentary**         | Whether complimentary tickets accepted   | Boolean   | False    |
| **has_payment_installments**  | Whether installments are acceptable | Boolean   | False    |

###Event category
Model `store.EventCategroy`

| Name                    | Description               | Type     |
| :-----------------------| :-------------------------| :--------|
| **category_name**       | Name of category          | String   |
| **icon**                | Display font/icon         | String   |
| **event_label**         | Label of event            | String   |
| **category_metadata**   | Category extra info       | String   |

###1. Create an Event
Endpoint `/stores/event/`

Auth Required: **True**

Roles Required: `[store-owner, co-owner]`

Request body
```

```

Response
```

```

---

##Tickets
Model `store.Ticket`

| Name                | Description               | Required |
| :-------------------| :-------------------------| :--------|
| **ticket_name**     | Name of ticket            | True     |

---
##Reservations
Model `store.Reservation`

Ticket orders automatically generate reservations when they are completed.

| Name                | Description               | Required |
| :-------------------| :-------------------------| :--------|
| **ticket_label**    | Ticket number             | True     |

###1. Querying reservations
Retrieve all reservations for a specific customer. `/stores/reservations/`.

To retrieve reservations bought in an order, use `/stores/order_reservations/{ORDER_NUMBER}/`

Allowed methods: `[GET]`

Auth Required: **True**

Response
```

```

###2. Validating reservations
Endpoint `/stores/reservations/{PK}/validate/`

Allowed methods: `[POST]`

Auth Required: **True**

Roles Required: `[store-owner, co-owner, agent]`

Request body 
```
{
    'ticket_number': 'TIC-XXXXXXX',
    'order_number': 'XXXXXX'
}
```
Response
```

```

###3. Verifying reservations
Endpoint `/stores/reservations/{PK}/verify/`

Allowed methods: `[POST]`

Auth Required: **True**

Roles Required: `[store-owner, co-owner, agent]`

Request body 
```
{
    'ticket_number': 'TIC-XXXXXXX',
    'order_number': 'XXXXXX'
}
```
Response
```

```
