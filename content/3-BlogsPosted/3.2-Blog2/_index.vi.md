---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
![S3, MediaConvert, CloudFront va website streaming flow](/images/3-BlogsPosted/3.2-Blog2/s3-cloudfront-streaming.png)

ðŸ“ BÃ i 2: Chia sáº» má»™t kinh nghiá»‡m nhá» khi xÃ¢y dá»±ng website xem phim trÃªn AWS

Xin chÃ o má»i ngÆ°á»i,

Trong quÃ¡ trÃ¬nh phÃ¡t triá»ƒn dá»± Ã¡n **Netflop**, nhÃ³m mÃ¬nh tá»«ng Ä‘áº·t cÃ¢u há»i:

**Táº¡i sao khÃ´ng phÃ¡t video trá»±c tiáº¿p tá»« Amazon S3 mÃ  láº¡i pháº£i dÃ¹ng thÃªm Amazon CloudFront?**

Sau khi tÃ¬m hiá»ƒu vÃ  triá»ƒn khai thá»±c táº¿, nhÃ³m nháº­n tháº¥y CloudFront mang láº¡i ráº¥t nhiá»u lá»£i Ã­ch.

Thay vÃ¬ ngÆ°á»i dÃ¹ng truy cáº­p trá»±c tiáº¿p vÃ o S3, toÃ n bá»™ video **HLS** Ä‘Æ°á»£c phÃ¢n phá»‘i thÃ´ng qua **Amazon CloudFront**.

Má»™t sá»‘ lá»£i Ã­ch mÃ  nhÃ³m nháº­n tháº¥y:

âœ… Giáº£m Ä‘á»™ trá»… khi xem video.

âœ… TÄƒng tá»‘c Ä‘á»™ táº£i nhá» cÆ¡ cháº¿ Cache táº¡i Edge Locations.

âœ… Giáº£m sá»‘ lÆ°á»£ng request trá»±c tiáº¿p Ä‘áº¿n S3.

âœ… Há»— trá»£ HTTPS máº·c Ä‘á»‹nh.

âœ… CÃ³ thá»ƒ báº£o vá»‡ ná»™i dung báº±ng **CloudFront Signed Cookies**, chá»‰ ngÆ°á»i dÃ¹ng Ä‘Ã£ Ä‘Æ°á»£c xÃ¡c thá»±c má»›i xem Ä‘Æ°á»£c video.

Äá»‘i vá»›i cÃ¡c website cÃ³ nhiá»u ná»™i dung media nhÆ° xem phim hoáº·c há»c trá»±c tuyáº¿n, CloudFront thá»±c sá»± lÃ  má»™t dá»‹ch vá»¥ ráº¥t Ä‘Ã¡ng Ä‘á»ƒ tÃ¬m hiá»ƒu.

ðŸ‘‰ KhÃ´ng biáº¿t má»i ngÆ°á»i thÆ°á»ng sá»­ dá»¥ng **CloudFront**, **S3 trá»±c tiáº¿p** hay CDN khÃ¡c khi xÃ¢y dá»±ng há»‡ thá»‘ng streaming? Ráº¥t mong Ä‘Æ°á»£c há»c há»i thÃªm tá»« má»i ngÆ°á»i.

ðŸ“š Link tham kháº£o
[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)
[https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)
[https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html?utm_source=chatgpt.com)
[https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html?utm_source=chatgpt.com)



