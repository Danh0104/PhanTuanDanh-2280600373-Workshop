---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
![AWS media workflow with S3, MediaConvert, CloudFront, Lambda, EventBridge, CloudWatch va SNS](/images/3-BlogsPosted/3.3-Blog3/mediaconvert-workflow.png)

ðŸ“ BÃ i 3: Chia sáº» má»™t tráº£i nghiá»‡m khi xÃ¢y dá»±ng Media Pipeline trÃªn AWS

Xin chÃ o má»i ngÆ°á»i,

Trong dá»± Ã¡n **Netflop**, sau khi video Ä‘Æ°á»£c **AWS Elemental MediaConvert** xá»­ lÃ½ xong, nhÃ³m cáº§n cáº­p nháº­t tráº¡ng thÃ¡i phim Ä‘á»ƒ ngÆ°á»i dÃ¹ng cÃ³ thá»ƒ xem ngay.

Ban Ä‘áº§u nhÃ³m nghÄ© Ä‘áº¿n viá»‡c Backend liÃªn tá»¥c kiá»ƒm tra tráº¡ng thÃ¡i Job (Polling), nhÆ°ng cÃ¡ch nÃ y vá»«a tá»‘n tÃ i nguyÃªn vá»«a khÃ´ng hiá»‡u quáº£.

Sau Ä‘Ã³ nhÃ³m chuyá»ƒn sang mÃ´ hÃ¬nh **Event-Driven Architecture** vá»›i:

**MediaConvert â†’ EventBridge â†’ Lambda â†’ Backend Webhook**

Luá»“ng hoáº¡t Ä‘á»™ng nhÆ° sau:

ðŸ“Œ MediaConvert hoÃ n thÃ nh Job.

ðŸ“Œ EventBridge tá»± Ä‘á»™ng nháº­n sá»± kiá»‡n.

ðŸ“Œ Lambda Ä‘Æ°á»£c kÃ­ch hoáº¡t vÃ  gá»i Webhook vá» Backend.

ðŸ“Œ Backend cáº­p nháº­t tráº¡ng thÃ¡i táº­p phim tá»« **Processing** sang **Ready**.

Nhá» Ä‘Ã³:

âœ… KhÃ´ng cáº§n Polling liÃªn tá»¥c.

âœ… Backend nháº¹ hÆ¡n.

âœ… Há»‡ thá»‘ng pháº£n há»“i gáº§n nhÆ° ngay khi encode hoÃ n táº¥t.

Qua dá»± Ã¡n nÃ y, nhÃ³m mÃ¬nh tháº¥y **EventBridge** lÃ  má»™t dá»‹ch vá»¥ ráº¥t há»¯u Ã­ch Ä‘á»ƒ xÃ¢y dá»±ng cÃ¡c workflow tá»± Ä‘á»™ng giá»¯a cÃ¡c dá»‹ch vá»¥ AWS.

ðŸ‘‰ Anh/chá»‹ vÃ  cÃ¡c báº¡n thÆ°á»ng sá»­ dá»¥ng **EventBridge**, **Amazon SQS** hay **AWS Step Functions** trong cÃ¡c há»‡ thá»‘ng Event-Driven? Ráº¥t mong Ä‘Æ°á»£c trao Ä‘á»•i thÃªm!

ðŸ“š Link tham kháº£o
[https://docs.aws.amazon.com/mediaconvert/latest/ug/eventbridge_events.html](https://docs.aws.amazon.com/mediaconvert/latest/ug/eventbridge_events.html?utm_source=chatgpt.com)
[https://docs.aws.amazon.com/eventbridge/latest/ref/events-ref-mediaconvert.html](https://docs.aws.amazon.com/eventbridge/latest/ref/events-ref-mediaconvert.html?utm_source=chatgpt.com)
[https://docs.aws.amazon.com/mediaconvert/latest/ug/mediaconvert_event_list.html](https://docs.aws.amazon.com/mediaconvert/latest/ug/mediaconvert_event_list.html?utm_source=chatgpt.com)
[https://docs.aws.amazon.com/lambda/latest/dg/welcome.html](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)

