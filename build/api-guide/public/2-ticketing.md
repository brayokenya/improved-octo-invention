#1. Events
##1.1. Querying Events

Methods [GET]

URL: `API_URL/stores/event/public/slug/`

RESPONSE
```
{
    "pagination": {
        "count": 78,
        "num_pages": 4,
        "current_page": 1,
        "html_context": {
            "previous_url": null,
            "next_url": "https://api-v2.mookh.com/stores/event/public/slug/?page=2",
            "page_links": [
                {
                    "url": "https://api-v2.mookh.com/stores/event/public/slug/",
                    "number": 1,
                    "is_active": true,
                    "is_break": false
                },
                {
                    "url": "https://api-v2.mookh.com/stores/event/public/slug/?page=2",
                    "number": 2,
                    "is_active": false,
                    "is_break": false
                },
                {
                    "url": "https://api-v2.mookh.com/stores/event/public/slug/?page=3",
                    "number": 3,
                    "is_active": false,
                    "is_break": false
                },
                {
                    "url": "https://api-v2.mookh.com/stores/event/public/slug/?page=4",
                    "number": 4,
                    "is_active": false,
                    "is_break": false
                }
            ]
        },
        "start_index": 1,
        "end_index": 20
    },
    "results": [
        {
            "id": "03cc166d-989d-4734-8e66-4657fe4796fe",
            "event_name": "Effective Goal Setting",
            "event_venue": "After 40 Hotels",
            "event_description": "<p>Every month we are offering you customized trainings to help you acquire the necessary skills you NEED for life. Skills that you will hardly get someone to train you ",
            "event_category_fk": "c79c2cbb-828c-441b-868e-c49ed2332725",
            "parent_event_id": null,
            "category_name": "Conference",
            "event_poster": "https://files.mookh.com/uploads/Effective_goal_setting-Moohk_Poster.jpg",
            "thumbnail_frontend": null,
            "store_fk": "0ca24105-32eb-497c-8806-3e7149b58f94",
            "store_name": "Adira Skills Development Program",
            "store_thumbnail": null,
            "currency": "KES",
            "country": "KE",
            "start_date": "2020-02-08T08:00:00+03:00",
            "end_date": "2020-02-08T13:00:00+03:00",
            "is_active": true,
            "is_free": false,
            "is_private": false,
            "is_published": true,
            "is_published_to_directory": true,
            "has_complimentary": true,
            "has_payment_installments": false,
            "payments_mpesa": true,
            "payments_cards": false,
            "payments_cash": false,
            "event_metadata": { },
            "latitude": "36.819326",
            "created": "2020-01-28T23:25:52.008616+03:00",
            "longitude": "-1.282863",
            "is_featured": false,
            "is_staff_pic": false,
            "staff_pick_start_date": null,
            "staff_pick_end_date": null,
            "shortened_url": "https://mookh.co/ZZZF3j/",
            "frontend_link": "https://mookh.com/embed/event/efffective-goal-setting",
            "slug": "efffective-goal-setting",
            "data_fields_names": [
                "Age", "What do you do?"
            ],
            "type_name": "store.event",
            "type_id": 18
        },
        {
            "id": "482e4549-8ce1-4909-8f49-db2727aea97d",
            "event_name": "254 Brewing Co. Launch",
            "event_venue": "254 Brewing Company, Kikuyu",
            "event_description": "<p>There's a new beer in town! Well, 13 of them actually. The 254 Brewing Co Launch Party marks the arrival of Kenya's newest line of craft beers. Come enjoy them FRESH from our modern brewery in Kikuyu, as we party in the garden with Blinky Bill and Jo Kisila. You will NOT want to miss this - you'll be telling your grandkids about it!! Tickets include 4 complimentary 350ml beers of your choice.<br></p>",
            "event_category_fk": "1ccd6ddc-92a3-42c6-bb4c-85e481d8e101",
            "parent_event_id": null,
            "category_name": "Entertainment",
            "event_poster": "https://files.mookh.com/uploads/254_Invitation_V52_moohk.jpg",
            "thumbnail_frontend": null,
            "store_fk": "bb651b3c-f183-41a7-82bb-9821be3486b0",
            "store_name": "254 Brewing Co.",
            "store_thumbnail": null,
            "currency": "KES",
            "country": "KE",
            "start_date": "2020-02-08T14:00:00+03:00",
            "end_date": "2020-02-08T19:00:00+03:00",
            "is_active": true,
            "is_free": false,
            "is_private": false,
            "is_published": true,
            "is_published_to_directory": true,
            "has_complimentary": true,
            "has_payment_installments": false,
            "payments_mpesa": true,
            "payments_cards": true,
            "payments_cash": false,
            "event_metadata": { },
            "latitude": "36.661417",
            "created": "2020-01-10T13:25:53.727170+03:00",
            "longitude": "-1.234482",
            "is_featured": true,
            "is_staff_pic": true,
            "staff_pick_start_date": "2020-02-01T04:12:00+03:00",
            "staff_pick_end_date": "2020-02-08T19:12:00+03:00",
            "shortened_url": "https://mookh.co/ZZZEoO/",
            "frontend_link": "https://mookh.com/embed/event/254-brewing-co-launch",
            "slug": "254-brewing-co-launch",
            "data_fields_names": [ ],
            "type_name": "store.event",
            "type_id": 18
        },
        {
            "id": "87100662-54b6-46f6-9660-8888ce3b6405",
            "event_name": "Black Valentine 🖤",
            "event_venue": "Junction mall",
            "event_description": "<p>Valentines Party for Singo peeps!</p>",
            "event_category_fk": "c79c2cbb-828c-441b-868e-c49ed2332725",
            "parent_event_id": null,
            "category_name": "Conference",
            "event_poster": "https://files.mookh.com/uploads/Black-Valentine-Poster-Square-Amended.jpg",
            "thumbnail_frontend": null,
            "store_fk": "91f48a40-9fd8-452e-bc80-df614ba20526",
            "store_name": "Pweza Africa",
            "store_thumbnail": null,
            "currency": "KES",
            "country": "KE",
            "start_date": "2020-02-09T16:30:00+03:00",
            "end_date": "2020-02-09T20:30:00+03:00",
            "is_active": true,
            "is_free": false,
            "is_private": false,
            "is_published": true,
            "is_published_to_directory": true,
            "has_complimentary": true,
            "has_payment_installments": false,
            "payments_mpesa": true,
            "payments_cards": true,
            "payments_cash": false,
            "event_metadata": { },
            "latitude": "36.763181",
            "created": "2020-01-20T17:23:18.539206+03:00",
            "longitude": "-1.298783",
            "is_featured": true,
            "is_staff_pic": true,
            "staff_pick_start_date": "2020-02-01T04:11:00+03:00",
            "staff_pick_end_date": "2020-02-09T17:11:00+03:00",
            "shortened_url": "https://mookh.co/ZZZEwh/",
            "frontend_link": "https://mookh.com/embed/event/black-valentines",
            "slug": "black-valentines",
            "data_fields_names": [ ],
            "type_name": "store.event",
            "type_id": 18
        },
        ....
    ]
}
```
##1.2. Retrieving an Event
Retrieve an event using **slug** property.

Method: [GET]

URL : `API_URL/stores/event/public/slug/<event_slug_here>`

Example [Through Think N Thin Comedy Show](https://api-v2.mookh.com/stores/event/public/slug/through-thick-n-thin-stand-up-comedy-special/) `https://api-v2.mookh.com/stores/event/public/slug/through-thick-n-thin-stand-up-comedy-special/`
```
{
    "id": "196d548c-2581-46d6-8bdf-39b17bdf9873",
    "slug": "through-thick-n-thin-stand-up-comedy-special",
    "event_name": "Through Thick N Thin Stand Up Comedy Special",
    "event_venue": "Garden City Mall",
    "event_description": "On the 14th February of 2020, we would like to celebrate a son of the soil who has brought a lot of laughter to various homes, Timothy Kimani...",
    "event_category_fk": "1ccd6ddc-92a3-42c6-bb4c-85e481d8e101",
    "category_name": "Entertainment",
    "event_poster": "https://files.mookh.com/uploads/njugush.jpg",
    "thumbnail_frontend": null,
    "store_fk": "50713b50-8871-4249-a56f-7647cfb2f789",
    "store_slug": "winnie-gor-events",
    "store_name": "NJUGUSH CREATIVES",
    "store_thumbnail": null,
    "currency": "KES",
    "country": "KE",
    "start_date": "2020-02-14T19:00:00+03:00",
    "end_date": "2020-02-14T22:00:00+03:00",
    "is_active": true,
    "tickets": [
        {
            "id": "cbcd63f7-e3cb-40eb-93c6-d9c369063fa9",
            "ticket_name": "Regular Tickets",
            "event_fk": "196d548c-2581-46d6-8bdf-39b17bdf9873",
            "ticket_description": "",
            "is_published": true,
            "ticket_metadata": { },
            "start_at": "2020-02-14T19:00:00+03:00",
            "end_at": "2020-02-14T22:00:00+03:00",
            "sort_no": 1,
            "group_ticket_quantity": 1,
            "is_group_ticket": false,
            "quantity": 1500,
            "complimentary": 0,
            "tickets_available": 1346,
            "payment_installments": 1,
            "is_available": true,
            "is_active": true,
            "thumbnail": "https://files.mookh.com/uploads/Comedy_poster_5_ajXOotX.jpg",
            "sales_start_at": "2020-01-31T22:00:00+03:00",
            "prices": [
                {
                    "price": "1000.00",
                    "price_currency": "KES"
                }
            ],
            "sales_end_at": "2020-02-14T22:00:00+03:00",
            "type_name": "store.ticket",
            "type_id": 22
        },
        {
            "id": "685da37f-18fc-4760-bc7f-9603627e684e",
            "ticket_name": "VIP TIckets",
            "event_fk": "196d548c-2581-46d6-8bdf-39b17bdf9873",
            "ticket_description": null,
            "is_published": true,
            "ticket_metadata": { },
            "sort_no": 2,
            "group_ticket_quantity": 1,
            "is_group_ticket": false,
            "tickets_available": 442,
            "payment_installments": 1,
            "is_available": true,
            "is_active": true,
            "thumbnail": "https://files.mookh.com/uploads/Comedy_poster_5_B2kEapa.jpg",
            "sales_start_at": "2020-01-12T11:45:00+03:00",
            "prices": [
                {
                    "price": "2500.00",
                    "price_currency": "KES"
                }
            ],
            "sales_end_at": "2020-02-14T22:00:00+03:00",
            "type_name": "store.ticket",
            "type_id": 22
        },
        {
            "id": "57e03718-9434-452b-9a7e-1dc69f4e5914",
            "ticket_name": "Couples Tickets",
            "event_fk": "196d548c-2581-46d6-8bdf-39b17bdf9873",
            "ticket_description": null,
            "ticket_value": "0.00",
            "is_published": true,
            "ticket_metadata": { },
            "sort_no": 3,
            "group_ticket_quantity": 2,
            "is_group_ticket": true,
            "tickets_available": 351,
            "payment_installments": 1,
            "is_available": true,
            "is_active": true,
            "thumbnail": "https://files.mookh.com/uploads/Comedy_poster_5_o2ZzCJp.jpg",
            "sales_start_at": "2020-01-12T11:45:00+03:00",
            "prices": [
                {
                    "price": "1800.00",
                    "price_currency": "KES"
                }
            ],
            "sales_end_at": "2020-02-14T22:00:00+03:00",
            "type_name": "store.ticket",
            "type_id": 22
        }
    ],
    "is_free": false,
    "is_private": false,
    "cash_locations": [ ],
    "default_cash_locations": [ ],
    "payments_mpesa": true,
    "payments_cards": true,
    "payments_cash": false,
    "is_published": true,
    "is_published_to_directory": true,
    "has_complimentary": true,
    "has_payment_installments": false,
    "shortened_url": "https://mookh.co/ZZZEnq/",
    "data_fields": [ ],
    "data_fields_names": [ ],
    "type_name": "store.event",
    "type_id": 18
}
```
###1.2.1. Important notes
* Ticket availability (can be purchased) is determined by **available** quantity and **sales_end_date**. An **is_available** preset flag is available for easy checking.
* Some events allow cash payments (**payments_cash=true**). In this case **cash_locations** and **default_cash_locations** should be displayed for the customer to see in case they want to pay for tickets with cash.
* For events with **is_free=true** (RSVP), customers should only be allowed to provide customer information and/or ticket names (See [ordering](/api-guide/public/6-ordering#31-additional-item-fields) section for more)
##1.3. Filtering / Sorting Events
You can filter public APIs supplying query parameters. The following is a list of available filters.

- **country** Filter feature items by country code. Options are **KE**, **UG** and **RW**.
- **store_fk=value** Filter events from a store using store UUID. Useful when displaying more ticket purchase options from an event organizer's store. 
- **category_name=value** (case insensitive) filter events by category name, **value**. Event categories are accessible via `API_URL/stores/event_category/`.
- **sort_by=value** this param enables filtering and sorting. **value** options are predefined as **today**, **tomorrow**, **this_weekend**, **this_week**, **next_week**, **this_month**, **next_month**, **asc** and **desc**.
- **start_date_min=value** filter events starting from date **value** to present.
- **start_date_max** filter events with starting date upto **value** to earlier (earlier being start date of first event by default or overridden by **start_date_min** stated above).
- **end_date_min** filter events whose ending dates are from date **value** to present.
- **end_date_max** filter events whose ending date upto **value** to earlier (end date of first event or overridden by **end_date_min**)
- **is_featured=value** boolean for filtering featured events.
Example usage [This week events](https://api-v2.mookh.com/stores/event/public/slug/?sort_by=this_week) `https://api-v2.mookh.comstores/event/public/slug/?sort_by=this_week`

###1.3.1. Important notes
* All date params must take the format **YYYY-MM-DD**.

##1.4. Searching Events
Mookh provides a global search for any content.

Methods: [GET]

URL: `API_URL/search/search/?q=SEARCH QUERY` **SEARCH QUERY** is user input.

Example `https://api-v2.mookh.com/search/search/?q=kenya`

RESPONSE format (some of the fields are hidden)

```
{
    "took": "integer milliseconds",
    "hits": {
        "total": "integer",
        "max_score": "integer",
        "hits": "object array"
    }
}
```
Process the `hits` object array is a mix of documents for events and music.
