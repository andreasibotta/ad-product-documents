
# Events

## All event types in `vw_app_event_tracking`

`select distinct(event_type) from vw_app_event_tracking;`

|type|
|----|
|ACCOUNT|
|ACTIVE|
|ADD_FAVORITES|
|BONUS|
|BONUSES|
|CATEGORY|
|ENGAGEMENT|
|FEATURED|
|FEATURED_CATEGORY|
|FIND_REBATES|
|GALLERY|
|INACTIVE|
|LINKED_OFFER|
|MINE|
|MINE_NAV|
|MODULE|
|MY_REBATES|
|NONE|
|NOTIFICATIONS|
|NOTIFICATIONS_BELL_CLICK|
|QUEST_PENDING|
|QUEST_START|
|QUEST_STATE_CHANGE|
|QUEST_STEP_CHANGE|
|QUEST_UNKNOWN|
|REGISTRATION_START|
|REGISTRATION_STOP|
|RETAILER_PICKER_CPG|
|RETAILER_PICKER_MCOMM|
|SEASONAL|
|SPOTLIGHT|
|TEAMMATES|
|TEAMMATES_NAV|
|account|
|app_review_or_feedback_prompt|
|bonus|
|category|
|cc_track|
|change_payment_method|
|changed_preference|
|click_action|
|connection_lost|
|copy_cardnumber|
|deal|
|deeplink|
|early_identifier_customer_id|
|encountered_dead_end|
|engagement_complete|
|engagement_start|
|enter_payment_amount|
|errors|
|gift_card_add_payment_method|
|launch_app|
|launch_partner_app|
|load_time|
|main_navigation|
|module|
|notification|
|offer|
|partner_app|
|pay_at_retailer|
|payment_history_click|
|payment_history_impression|
|product|
|pwi_add_payment_method|
|pwi_confirm_payment_cancelled|
|pwi_copy_cardnumber|
|pwi_double_purchase_prompt|
|pwi_help|
|pwi_manage_transactions|
|pwi_manage_txn_action|
|pwi_manage_txn_change_filter|
|pwi_onboarding_close|
|pwi_onboarding_next|
|pwi_pay_at_retailer|
|pwi_receive_order|
|pwi_retailer_transactions|
|pwi_reveal_card_number|
|pwi_spent_toggle|
|pwi_start_earning|
|pwi_submit_order|
|pwi_terms_and_conditions|
|pwi_time_to_complete_order|
|pwi_view_barcode|
|quest|
|receipt_offer_diff|
|receive_order|
|registration|
|retailer|
|reward|
|scanned_barcode|
|screenshot_taken|
|search|
|session|
|session_end|
|session_start|
|share_history|
|submit_order|
|text_entry|
|tile|

## What some events look like

`select * from vw_app_event_tracking where event_type like '%enga%' limit 30;`
| event_header | user_id |device_id|event_type|time|event_properties|user_properties|groups|app_version|platform|os_name|os_version|device_brand|device_manufacturer|device_model|carrier|country|region|city|dma|language|price|quantity|revenue|product_id|revenue_type|location_lat|location_lng|ip|idfa|idfv|adid|android_id|event_id|session_id|insert_id|day|created_day|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
| {"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560396259821"},"event_uri":{"dom":"IB_SCH","id":"531f6282-f72e-42ff-9ac3-dcc327795cb7","type":"ibotta_pb.tracking.TrackingEvent"},"fake":false,"host":"tracking-server-git-0.20.0-8-g4117656-blue-76db95b974-grzjp","priority":"LOW","revision":""} | 28906606 | 5dec2f1c665c73e1 | engagement_start | {"millis":"1560396184788"} | {"offer_id":{"value":["366929"]},"engagement_id":{"value":["402734"]},"type":{"value":["Fact"]}} | {} | {} | 5.65.0 | android | android | 9 | xiaomi | Xiaomi | Redmi 7 | AT&T | in |  |  |  | eng | 0.0 | 0 | 0.0 |  |  | 0.0 | 0.0 | 97.113.154.54 |  |  | 317525d9-ce0e-4c7e-8883-83d14f61f8a5 | 5dec2f1c665c73e1 | 193 | 1560396110745 | 531f6282-f72e-42ff-9ac3-dcc327795cb7 | 2019-06-13 | 2019-06-13 | 
| {"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560391757971"},"event_uri":{"dom":"IB_SCH","id":"dd2a2591-3328-468f-8f36-5248470e547b","type":"ibotta_pb.tracking.TrackingEvent"},"fake":true,"host":"tracking-server-git-0.20.0-8-g4117656-blue-76db95b974-qbgk7","priority":"LOW","revision":""} | 15005972 | 65FC251E-3433-473E-8AAC-0B4993D5879B | offer | {"millis":"1560391738700"} | {"offer_category_id":{"value":["344"]},"context":{"value":["gallery"]},"event_at":{"value":["1560391738.700187"]},"counter":{"value":["1"]},"current_value":{"value":["$5.00 back"]},"offer_id":{"value":["357608"]},"module_name":{"value":["All-Optional(\"Health & Wellness\")"]},"clicked":{"value":["0"]},"list_index":{"value":["61"]},"module_index":{"value":["22"]},"amount":{"value":["5.0"]},"retailer_id":{"value":["4"]}} | {} | {} | 5.64.1 | ios | ios | 12.3.1 | iPhone | Apple | iPhone 6 | AT&T | United States | NJ | Blackwood |  | English | 0.0 | 0 | 0.0 |  |  | 39.80848 | -75.05332 | 73.150.223.57 |  |  |  |  | 0 | 1560384767870 | dd2a2591-3328-468f-8f36-5248470e547b | 2019-06-13 | 2019-06-13 |
| {"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560391757979"},"event_uri":{"dom":"IB_SCH","id":"aa111b96-6544-4ff8-8b46-b249d7ec0994","type":"ibotta_pb.tracking.TrackingEvent"},"fake":true,"host":"tracking-server-git-0.20.0-8-g4117656-blue-76db95b974-qbgk7","priority":"LOW","revision":""} | 29510967 | 8875467bd51064b9 | search | {"millis":"1560391743765"} | {"category_id":{"value":["0"]},"click_type":{"value":["SEARCH"]},"engaged":{"value":["0"]},"context":{"value":["FIND_REBATES"]},"search_type":{"value":["TYPED"]},"counter":{"value":["1"]},"term":{"value":[" pretzel crisps"]},"clicked":{"value":["true"]},"quest_step":{"value":["0"]},"amount":{"value":["0.0"]}} | {} | {} | 5.64.1 | android | android | 8.0.0 | samsung | samsung | SM-G930T | T-Mobile | us |  |  |  | eng | 0.0 | 0 | 0.0 |  |  | 35.789818 | -86.440155 | 99.153.47.179 |  |  | 75ee504f-81e3-4984-8de8-1afc212fc073 | 8875467bd51064b9 | 533 | 1560391588125 | aa111b96-6544-4ff8-8b46-b249d7ec0994 | 2019-06-13 | 2019-06-13 |
| {"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560391758095"},"event_uri":{"dom":"IB_SCH","id":"ae6451ed-78a0-4072-a570-c1a2b243b6c5","type":"ibotta_pb.tracking.TrackingEvent"},"fake":true,"host":"tracking-server-git-0.20.0-8-g4117656-blue-76db95b974-qbgk7","priority":"LOW","revision":""} | 22366386 | 956C024A-F122-4CEC-A073-DBD74097A05C | retailer | {"millis":"1560391603029"} | {"context":{"value":["featured"]},"event_at":{"value":["1560391603.0299459"]},"counter":{"value":["1"]},"module_name":{"value":["New! Pay with Ibotta"]},"module_id":{"value":["635"]},"clicked":{"value":["0"]},"list_index":{"value":["1"]},"module_index":{"value":["3"]},"retailer_id":{"value":["1059"]}} | {} | {} | 5.64.1 | ios | ios | 12.3.1 | iPhone | Apple | iPhone 7 Plus | T-Mobile | United States | UT | Sandy |  | English | 0.0 | 0 | 0.0 |  |  | 40.585915 | -111.86894 | 73.98.252.46 |  |  |  |  | 0 | 1560391589205 | ae6451ed-78a0-4072-a570-c1a2b243b6c5 | 2019-06-13 | 2019-06-13 |
| {"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560391758096"},"event_uri":{"dom":"IB_SCH","id":"d4188c55-f3ce-4e90-b0cf-c715fda4aea8","type":"ibotta_pb.tracking.TrackingEvent"},"fake":true,"host":"tracking-server-git-0.20.0-8-g4117656-blue-76db95b974-qbgk7","priority":"LOW","revision":""} | 22366386 | 956C024A-F122-4CEC-A073-DBD74097A05C | tile | {"millis":"1560391603687"} | {"event_at":{"value":["1560391603.687635"]},"counter":{"value":["1"]},"tile_id":{"value":["9602"]},"module_name":{"value":["Featured Banner"]},"module_id":{"value":["4"]},"clicked":{"value":["0"]},"module_index":{"value":["0"]},"context":{"value":["featured"]}} | {} | {} | 5.64.1 | ios | ios | 12.3.1 | iPhone | Apple | iPhone 7 Plus | T-Mobile | United States | UT | Sandy |  | English | 0.0 | 0 | 0.0 |  |  | 40.58593 | -111.868935 | 73.98.252.46 |  |  |  |  | 0 | 1560391589205 | d4188c55-f3ce-4e90-b0cf-c715fda4aea8 | 2019-06-13 | 2019-06-13 |
| {"agent":"ApiGateway","environment":"PROD","event_at":{"millis":"1560391758148"},"event_uri":{"dom":"IB_SCH","id":"400db06a-8d80-11e9-bbcf-6145041cb0ca","type":"ibotta_pb.tracking.TrackingEvent"},"fake":false,"host":"0s18we9eo2.execute-api.us-east-1.amazonaws.com","priority":"LOW","revision":""} | 19539982 |  | cc_track | {"millis":"1560391758148"} | {"retailer_id":{"value":["884","932","890","794","805"]},"campaign_id":{"value":["c35dac38-150e-4cf8-9cf4-61a36027f97d"]}} | {} | {} |  | connected_content |  |  |  |  |  |  |  |  |  |  |  | 0.0 | 0 | 0.0 |  |  | 0.0 | 0.0 | 50.16.249.9 |  |  |  |  | 1560391758 | 1560391758148 | 400db06a-8d80-11e9-bbcf-6145041cb0ca | 2019-06-13 | 2019-06-13 |
{"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560810296348"},"event_uri":{"dom":"IB_SCH","id":"efc1eee9-19cb-45bc-8f81-434698b4297b","type":"ibotta_pb.tracking.TrackingEvent"},"fake":true,"host":"tracking-server-5b457c4d47-psrkt","priority":"LOW","revision":""} | 9475166 | 64980C3F-7433-46A7-B9C3-A2994EB600CD | module | {"millis":"1560810274202"} | {"event_at":{"value":["1560810274.20225"]},"counter":{"value":["1"]},"module_name":{"value":["Popular Bonuses"]},"module_id":{"value":["7"]},"clicked":{"value":["1"]},"module_index":{"value":["18"]},"context":{"value":["featured"]}} | {} | {} | 5.65.1 | ios | ios | 12.3.1 | iPhone | Apple | iPhone 7 | Appalachian | United States | KY | Salyersville |  | English | 0.0 | 0 | 0.0 |  |  | 37.803375 | -83.11481 | 172.97.22.169 |  |  |  |  | || 0 | 1560766471764 | efc1eee9-19cb-45bc-8f81-434698b4297b | 2019-06-17 | 2019-06-17
{"agent":"tracking-server","environment":"PROD","event_at":{"millis":"1560810296583"},"event_uri":{"dom":"IB_SCH","id":"96f8a788-eb05-4375-8616-b8ca76f4bde8","type":"ibotta_pb.tracking.TrackingEvent"},"fake":true,"host":"tracking-server-5b457c4d47-whhr8","priority":"LOW","revision":""} | 18245208 | 3417b29b10e7015 | module | {"millis":"1560810225509"} | {"category_id":{"value":["0"]},"engaged":{"value":["0"]},"context":{"value":["FEATURED"]},"counter":{"value":["1"]},"module_name":{"value":["Recommended Retailers "]},"module_id":{"value":["279"]},"clicked":{"value":["false"]},"module_index":{"value":["1"]},"quest_step":{"value":["0"]},"amount":{"value":["0.0"]}} | {} | {} | 5.65.1 | android | android | 7.0 | samsung | samsung | SAMSUNG-SM-G925A | AT&T | us |  |  |  | eng | 0.0 | 0 | 0.0 |  |  | 33.583225 | -112.24565 | 184.98.196.207 |  |  | 938c18c7-033b-4d20-9f6b-3451746fbd87 | 3417b29b10e7015 | 14 | 1560810212256 | 96f8a788-eb05-4375-8616-b8ca76f4bde8 | 2019-06-17 | 2019-06-17 |
