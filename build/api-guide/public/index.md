This section of documentation covers publicly accessible Mookh APIs ranging from retrieving items, filtering items, ordering and payments.

Public APIs consists of approved and published Events, Music, Services and Products.

API host urls:

- PRODUCTION - **https://api-v2.mookh.com** 
- STAGING - **https://api-v2.staging.mookh.com** 
- SANDBOX - **https://api-v2.sandbox.mookh.com**

#API Response Structure
##Get List Response
```
{
    "pagination": [
        "count": "interger",
        "num_pages": "integer",
        "current_page": "integer",
        "html_context": {
            "previous_url": "string|null",
            "next_url": "string|null",
            "page_links": [
                {
                    "url": "string",
                    "number": 1,
                    "is_active": "boolean",
                    "is_break": "boolean"
                },
                .....
            ]
        },
        "start_index": 1,
        "end_index": 20
    ],
    "results": "objects array"
}
```
##Get Retrieve Response
```
{
    "object"
}
```
##Post Response
```
{
    "object"
}
```
