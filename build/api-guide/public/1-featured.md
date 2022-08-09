#1. Introduction
Mookh Staff occasionally pick items (ticket and music) to be featured on [mookh.com](https://mookh.com) carousel.
##1.1. Querying Featured ITems

Methods [GET]

URL: `API_URL/stores/feature/`

Example [featured items](https://api-v2.mookh.com/store/featured/)

RESPONSE
```
[
    {
        "content_type_name": "event",
        "item_id": "093a164c-9711-40ac-b2da-0d5248932c1c",
        "id": "093a164c-9711-40ac-b2da-0d5248932c1c",
        "slug": "roast-and-rhyme-2020",
        "name": "ROAST AND RHYME 2020",
        "event_name": "ROAST AND RHYME 2020",
        "event_venue": "Jahazi Pier",
        "venue": "Jahazi Pier",
        "event_description": "<p>ROAST AND RHYME 2020 Edition 1: #ReggaeRaggaNyamNyam</p><p>1st March 2020&nbsp;</p><p>JAHAZI PIER, MUNYONO&nbsp;</p><p>EARLY BIRD - 50K, GROUP OF 5 - 200K&nbsp;</p><p>GATE TICKETS - 70K&nbsp;</p>",
        "country": "UG",
        "start_date": "2020-03-01T11:00:00+03:00",
        "end_date": "2020-03-01T23:00:00+03:00",
        "pick_start_date": "2020-02-01T04:09:00+03:00",
        "pick_end_date": "2020-03-01T19:09:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/IMG-20200131-WA0009.jpg",
        "store": "Swangz Avenue",
        "category_name": "Entertainment",
        "type_name": "store.event",
        "created": "2020-01-31T10:50:41.434474+03:00"
    },
    {
        "content_type_name": "event",
        "item_id": "24737b2d-1be1-4d5b-9d28-5962f89c0310",
        "id": "24737b2d-1be1-4d5b-9d28-5962f89c0310",
        "slug": "dstrkt-launch-party",
        "name": "Launch Party: dstrkt",
        "event_name": "Launch Party: dstrkt",
        "event_venue": "Nairobi",
        "venue": "Nairobi",
        "event_description": "<p>Reviving underground music in Kenya.</p>",
        "country": "KE",
        "start_date": "2020-02-07T23:59:00+03:00",
        "end_date": "2020-02-08T06:00:00+03:00",
        "pick_start_date": "2020-02-01T04:13:00+03:00",
        "pick_end_date": "2020-02-07T19:13:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/82518299_2207515512682616_9123429277453254656_n.jpg",
        "store": "KENYA NIGHTS EVENTS",
        "category_name": "Entertainment",
        "type_name": "store.event",
        "created": "2020-01-07T13:54:16.157283+03:00"
    },
    {
        "content_type_name": "event",
        "item_id": "87100662-54b6-46f6-9660-8888ce3b6405",
        "id": "87100662-54b6-46f6-9660-8888ce3b6405",
        "slug": "black-valentines",
        "name": "Black Valentine 🖤",
        "event_name": "Black Valentine 🖤",
        "event_venue": "Junction mall",
        "venue": "Junction mall",
        "event_description": "<p>Valentines Party for Singo peeps!</p>",
        "country": "KE",
        "start_date": "2020-02-09T16:30:00+03:00",
        "end_date": "2020-02-09T20:30:00+03:00",
        "pick_start_date": "2020-02-01T04:11:00+03:00",
        "pick_end_date": "2020-02-09T17:11:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/Black-Valentine-Poster-Square-Amended.jpg",
        "store": "Pweza Africa",
        "category_name": "Conference",
        "type_name": "store.event",
        "created": "2020-01-20T17:23:18.539206+03:00"
    },
    {
        "content_type_name": "event",
        "item_id": "6f4eaa8a-e937-492b-8aaf-71cc63b1b4f5",
        "id": "6f4eaa8a-e937-492b-8aaf-71cc63b1b4f5",
        "slug": "journey-to-1000",
        "name": "Journey to 1,000",
        "event_name": "Journey to 1,000",
        "event_venue": "The Alchemist Bar",
        "venue": "The Alchemist Bar",
        "event_description": "<p><span style="font-size: 14px;">A journey of a thousand miles begins with a single step. Journey to 1,000 is a concert series starting on February 9th. This will be the first of four editions happening in 2020 and is the first step towards filling the Alchemist bar with 1,000 Tetu Shani fans by November. We purpose to get 5,000 fans at a venue by the end of next year, 10,000 by the following year and we hope to fill a small stadium by 2021.</span></p><p><span style="font-size: 14px;">Join us in making this ambitious plan a reality!</span></p><p><br></p>",
        "country": "KE",
        "start_date": "2020-02-09T19:00:00+03:00",
        "end_date": "2020-11-01T21:00:00+03:00",
        "pick_start_date": "2020-02-01T04:10:00+03:00",
        "pick_end_date": "2020-02-09T21:10:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/For_WhatsApp.jpg",
        "store": "TETU SHANI",
        "category_name": "Entertainment",
        "type_name": "store.event",
        "created": "2020-01-09T13:01:52.490661+03:00"
    },
    {
        "content_type_name": "event",
        "item_id": "ba9f59d3-575d-42f5-a167-28f36777d0b4",
        "id": "ba9f59d3-575d-42f5-a167-28f36777d0b4",
        "slug": "khanga-festival",
        "name": "Khanga Festival",
        "event_name": "Khanga Festival",
        "event_venue": "Beneath the Baobabs",
        "venue": "Beneath the Baobabs",
        "event_description": "<p class="MsoNormal"><span lang="en-KE">From the collaborative minds behind <a href="https://www.churchill.co.ke/">The Churchill <span lang="EN-US">S</span>how</a> and <a href="http://beneaththebaobabs.com/kilifinewyear/">Kilifi New Year</a></span><span lang="en-KE"> </span><span lang="en-KE">- Laugh Industry and Beneath the Baobabs present Khanga Festival. <o:p></o:p></span></p><p class="MsoNormal"><span lang="en-KE"><o:p>&nbsp;</o:p></span></p><p class="MsoNormal"><span lang="en-KE"><a href="http://khangafestival.com/" style="font-weight: bold;">Khanga Festival 2020</a> is a joyful and colorful gathering and celebration of East African music, arts, culture, food, comedy, stories and performance. <o:p></o:p></span></p><p class="MsoNormal"><span lang="en-KE"><o:p>&nbsp;</o:p></span></p><p class="MsoNormal"><span lang="en-KE">The festival aims to bring people together to laugh, dance, learn, play, create, participate, explore and evolve – to celebrate life, peace, love, freedom of expression and respect for mother nature.<o:p></o:p></span></p><p class="MsoNormal"><span lang="en-KE"><o:p>&nbsp;</o:p></span></p><p class="MsoNormal"><span lang="en-KE">Khanga Festival will reignite the value of the ‘Khanga’ as an East African heritage and purposes to create a popular culture that attendees can own and develop.<o:p></o:p></span></p><p class="MsoNormal"><span lang="en-KE"><o:p>&nbsp;</o:p></span></p><p class="MsoNormal"><span lang="en-KE">For 3 straight days, Khanga Festival will bring together musicians, comedians, storytellers, visual artists, designers and performers from all across East Africa for a fun-filled, all-welcoming, family-friendly event packed with memorable immersive experiences! <o:p></o:p></span></p><p class="MsoNormal"><span lang="en-KE"><o:p>&nbsp;</o:p></span></p><p class="MsoNormal"> </p><p class="MsoNormal"><span lang="en-KE">We can't wait to welcome you!<o:p></o:p></span></p>",
        "country": "KE",
        "start_date": "2020-04-10T14:00:00+03:00",
        "end_date": "2020-04-13T05:00:00+03:00",
        "pick_start_date": "2020-02-01T04:05:00+03:00",
        "pick_end_date": "2020-04-12T04:05:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/EASTER_2020_vuRiATn.jpg",
        "store": "Khanga Festival",
        "category_name": "Entertainment",
        "type_name": "store.event",
        "created": "2020-01-22T14:32:10.760089+03:00"
    },
    {
        "content_type_name": "album",
        "item_id": "b4d32ed3-96e8-4c0f-80d4-e19385bc5b19",
        "id": "b4d32ed3-96e8-4c0f-80d4-e19385bc5b19",
        "slug": "conqueror",
        "name": "Conqueror",
        "description": "<p class="MsoNormal"><span lang="EN-US" style="font-size: 11pt; color: rgb(34, 34, 34); background-image: initial; background-position: initial; background-size: initial; background-repeat: initial; background-attachment: initial; background-origin: initial; background-clip: initial;">The song&nbsp;<b>Conqueror</b>&nbsp;is Collo's 3rd single&nbsp;after finding salvation and a 2-year music hiatus. In his new track, the celebrated&nbsp;<i>sheng</i>&nbsp;rapper introduces a new and fresh sound to Kenya's urban&nbsp;gospel music scene, in collaboration with Burundian beatmaker, Kevin Mindozi a.k.a "K Da Great."&nbsp; The song was recorded, mixed and mastered at Supersonic Studio by Sean Peevers.</span><span lang="EN-US" style="font-size:11.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;; mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin;mso-fareast-language: EN-GB"> The Music video was shot and directed by Mike (V.j One) Odhiambo<o:p></o:p></span></p> <p class="MsoNormal"><span lang="EN-US" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-fareast-language:EN-GB"><o:p>&nbsp;</o:p></span></p> <p class="MsoNormal"><span lang="en-KE" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-ansi-language:#0C00;mso-fareast-language:EN-GB">Connect with me... <o:p></o:p></span></p> <p class="MsoNormal"><span lang="en-KE" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-ansi-language:#0C00;mso-fareast-language:EN-GB">Instagram: <a href="https://www.instagram.com/collo.mfalme/">https://www.instagram.com/collo.mfalme/</a> <o:p></o:p></span></p> <p class="MsoNormal"><span lang="en-KE" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-ansi-language:#0C00;mso-fareast-language:EN-GB">Facebook: <a href="https://www.facebook.com/collomajale">https://www.facebook.com/collomajale</a> <o:p></o:p></span></p> <p class="MsoNormal"><span lang="en-KE" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-ansi-language:#0C00;mso-fareast-language:EN-GB">Twitter: <a href="https://twitter.com/collo_mfalme">https://twitter.com/collo_mfalme</a><o:p></o:p></span></p> <p class="MsoNormal"><span lang="en-KE" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-ansi-language:#0C00;mso-fareast-language:EN-GB"><o:p>&nbsp;</o:p></span></p> <p class="MsoNormal"><span lang="EN-US" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-fareast-language:EN-GB">THE BARZ<o:p></o:p></span></p> <p class="MsoNormal"><span lang="EN-US" style="font-size:11.0pt;mso-fareast-font-family: &quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin; mso-fareast-language:EN-GB"><o:p>&nbsp;</o:p></span></p> <p class="MsoNormal"><b><span lang="EN-US" style="font-size: 11pt; color: rgb(34, 34, 34); background-image: initial; background-position: initial; background-size: initial; background-repeat: initial; background-attachment: initial; background-origin: initial; background-clip: initial;">Born Sinner, Born Again Winner.<br> Kaa Bazooka Nalipuka Kaa Strife.<br> Sina Mila Ila Vina, Nina Jina.<br> Take a Look, it's in the Book of Life.<br> Africa's First 007.<br> Karibu Kenya, Kwetu 047.<br> Hapa Kazi Tu, 24/7<br> Still Alive Kaa 365 Ha!<br> <br> Nani Process. (Yes)<br> Ndio maana nina proceed. (Yeah)<br> Instead of counting loses,<br> Hesabu zangu siku hizi huwa ku-sow seeds...mnhhh.<br> Tucheze truth or dare /<br> Miracle baby uliza Pastor Deya. Niko ritho kaa peddy, na pia m-scarce kaa spare.<br> Full blast power puff, pass there. Clan ya Black Ku Klux woooh!<br> <br> Ndugu ni Ndugu/Tattoo si heena boo.<br> Kama hujaskia Lovers Lie.<br> Kuku ni Nuku. Jogoo jina tu.<br> Caterpillar&nbsp;pia Butterfly.<br> Pride, Envy, Wrath, Gluttony, Lust, Sloth, Greed.<br> Devil you're a Liar, Mwizi, Murderer trying to Destroy I... FREEZE!<br> <br> We at the Mountain Top...yeah.<br> I had to Leave the Valley of the Shadow of Death. So that the crowd can't stop. (Na)<br> Never Lose Your Soul Confusing Money for Wealth, Look Even I Fell out but Did I Sell out? Bar for Bar, I've held it down.<br> From Way Back, bila Maybach. Si play back, Tuko Live Buda Payback.<br> <br> Napepea Kaa Paa, Wasinizibie na Ganji.<br> Namesea Kadhaa, Usiniingizie na Rangi.<br> Tembea Kaa Star, Usizidiwe na Dhambi.<br> Kemea Kataa, Usi-Deceive-iwe na Bangi.<br> Hmnh... Hawaradi/ Niwieni Radhi<br> Flow Thitima/ Nikuwapiga Radi.<br> Naombea Mama, Mkono Mtupu Haulambwi.<br> Nyenyekea Baba, Upunguziwe Kitambi.<br> <br> Hii hata hain-need hook. It does not need a chorus. No chorus!<br> <br> Kutokana na hayo, niseme nini zaidi? Ikiwa Mungu Yuko Upande Wangu, Nani Awezaye Kunipinga?<br> <br> Ah Zi, Hio Box Yao Siingii Bana. Siingii Hio Box Yao!.<br> <br> Mbele Iko Sawa Hatwezi Backslide Pia.<br> Kwa Sanaa Mi NI G.O.A. T though Kondoo In Christ..Ah.<br> Revelation,&nbsp;Jubilation.&nbsp;Now I know why&nbsp;they call me Rival.<br> Restoration,&nbsp;Reformation&nbsp;for the Spring Board&nbsp;of Revival.</span></b><span lang="EN-US"><o:p></o:p></span></p>",
        "country": "",
        "price": 20,
        "prices": [
            {
                "price": "20.00",
                "price_currency": "KES"
            }
        ],
        "no_of_tracks": 1,
        "pick_start_date": "2020-01-23T10:16:00+03:00",
        "pick_end_date": "2020-02-12T10:16:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/CONQUEROR_-_COLLO_ARTWORK_SQjMgxG.jpg",
        "store": "Hope Nation KE",
        "category_name": "gospel",
        "category_type": "MUSIC SINGLE",
        "type_name": "digital_content.album",
        "created": "2020-01-20T13:02:46.202702+03:00"
    },
    {
        "content_type_name": "album",
        "item_id": "5431707a-7f0e-4648-a5f5-fc03a24dbb1a",
        "id": "5431707a-7f0e-4648-a5f5-fc03a24dbb1a",
        "slug": "set-us-on-fire",
        "name": "Set Us On Fire",
        "description": "<p>Set Us On Fire is Kanjii's 3rd worship album recorded live in Irvine California.&nbsp;</p>",
        "country": "",
        "price": 450,
        "prices": [
            {
                price: "450.00",
                price_currency: "KES"
            }
        ],
        "no_of_tracks": 10,
        "pick_start_date": "2020-02-04T13:28:00+03:00",
        "pick_end_date": "2020-02-11T13:28:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/Album_Cover_2S5IjQw.jpg",
        "store": "Kanjii Mbugua Music",
        "category_name": "gospel",
        "category_type": "MUSIC SINGLE",
        "type_name": "digital_content.album",
        "created": "2019-11-01T16:50:21.219430+03:00"
    },
    {
        "content_type_name": "album",
        "item_id": "ee1d887e-3b9e-4cf4-91d2-db3edc61ebc8",
        "id": "ee1d887e-3b9e-4cf4-91d2-db3edc61ebc8",
        "slug": "wangala-ngala",
        "name": "Wang'ala ng'ala",
        "description": "<p>He is shining through me</p>",
        "country": "",
        "price": 100,
        "prices": [
            {
                "price": "100.00",
                "price_currency": "KES"
            }
        ],
        "no_of_tracks": 1,
        "pick_start_date": "2020-01-09T10:42:00+03:00",
        "pick_end_date": "2020-02-12T10:42:00+03:00",
        "thumbnail": "https://files.mookh.com/uploads/ngala-01_9ajvEZr.jpg",
        "store": "PartrawKe",
        "category_name": "AFROLECTRIC",
        "category_type": "MUSIC SINGLE",
        "type_name": "digital_content.album",
        "created": "2019-10-16T13:20:15.486516+03:00"
    }
]
```
##1.2. Filtering / Sorting Feature Items
You can filter featured items APIs supplying query parameters.

- **country** Filter feature items by country code. Options are **KE**, **UG** and **RW**.
- **type** Filter items by predefined types. Options are **events**, **music** and **ebooks**.
- **category_name=value** (case insensitive) filter by category name, **value**. Ticketing categories are accessible via `API_URL/stores/event_category/` and music categories via `API_URL/digital_media/category/`.
- **sort_by=value** this param enables filtering and sorting. **value** options are predefined as **today**, **tomorrow**, **this_weekend**, **this_week**, **next_week**, **this_month**, **next_month**, **newest** and **oldest**.

Example usage [Featured this week](https://api-v2.mookh.com/stores/featured/?sort_by=this_week) `https://api-v2.mookh.com/stores/featured/?sort_by=this_week`
###1.2.1. Important notes
* All date params must take the format **YYYY-MM-DD**.
