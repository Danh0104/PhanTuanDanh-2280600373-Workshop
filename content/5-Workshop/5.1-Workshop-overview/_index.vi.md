---
title: "Tá»•ng quan workshop"
date: 2026-07-10
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

Pháº§n nÃ y giá»›i thiá»‡u kiáº¿n trÃºc tá»•ng thá»ƒ cá»§a website xem phim **Netflop** trÃªn AWS vÃ  vai trÃ² cá»§a tá»«ng nhÃ³m dá»‹ch vá»¥. ÄÃ¢y lÃ  pháº§n ná»n Ä‘á»ƒ ngÆ°á»i Ä‘á»c hiá»ƒu cÃ¡ch request Ä‘i tá»« ngÆ°á»i dÃ¹ng Ä‘áº¿n há»‡ thá»‘ng, cÃ¡ch admin upload video vÃ  cÃ¡ch video Ä‘Æ°á»£c xá»­ lÃ½ tá»± Ä‘á»™ng trÆ°á»›c khi phÃ¡t trÃªn web.

Netflop khÃ´ng chá»‰ lÃ  má»™t website CRUD Ä‘Æ¡n giáº£n. Há»‡ thá»‘ng cÃ³ pipeline media riÃªng gá»“m upload file lá»›n, lÆ°u file gá»‘c, chuyá»ƒn mÃ£, lÆ°u HLS output, phÃ¡t qua CDN, báº£o vá»‡ link stream vÃ  cáº­p nháº­t tráº¡ng thÃ¡i táº­p phim tá»± Ä‘á»™ng.

![](/2280600178_huynhduybao_workshopaws/images/5-Workshop/5.1-Workshop-overview/sodo.png)

#### Ná»™i dung

1. [Kiáº¿n trÃºc tá»•ng quan](5.1.1-architecture/)
2. [Báº£ng dá»‹ch vá»¥ vÃ  vai trÃ²](5.1.2-service-map/)

<!-- NETFLOP_DETAIL_START -->
#### CÃ¡ch trÃ¬nh bÃ y tá»•ng quan

á»ž pháº§n tá»•ng quan, nÃªn trÃ¬nh bÃ y theo hai gÃ³c nhÃ¬n:

1. GÃ³c nhÃ¬n ngÆ°á»i dÃ¹ng: má»Ÿ web, Ä‘Äƒng nháº­p, chá»n phim, xem phim, tiáº¿p tá»¥c xem.
2. GÃ³c nhÃ¬n admin: thÃªm phim, upload táº­p phim, theo dÃµi tiáº¿n trÃ¬nh convert, thÃªm phá»¥ Ä‘á».

Sau Ä‘Ã³ liÃªn káº¿t tá»«ng chá»©c nÄƒng vá»›i dá»‹ch vá»¥ AWS tÆ°Æ¡ng á»©ng. VÃ­ dá»¥, chá»©c nÄƒng upload táº­p phim khÃ´ng chá»‰ náº±m á»Ÿ frontend mÃ  cÃ²n Ä‘i qua backend, S3 input, MediaConvert, S3 output, CloudFront vÃ  RDS.

#### Máº«u mÃ´ táº£ ngáº¯n trong bÃ¡o cÃ¡o

Netflop Ä‘Æ°á»£c triá»ƒn khai theo mÃ´ hÃ¬nh á»©ng dá»¥ng web káº¿t há»£p media pipeline. EC2 cháº¡y á»©ng dá»¥ng chÃ­nh, RDS lÆ°u dá»¯ liá»‡u nghiá»‡p vá»¥, S3 lÆ°u file media, MediaConvert xá»­ lÃ½ video, CloudFront phÃ¢n phá»‘i HLS vÃ  Lambda xá»­ lÃ½ cÃ¡c tÃ¡c vá»¥ tá»± Ä‘á»™ng. CÃ¡ch triá»ƒn khai nÃ y giÃºp giáº£m táº£i cho EC2 vÃ¬ file video lá»›n khÃ´ng Ä‘Æ°á»£c lÆ°u lÃ¢u dÃ i trÃªn á»• Ä‘Ä©a mÃ¡y chá»§.
<!-- NETFLOP_DETAIL_END -->

<!-- NETFLOP_IMPLEMENTATION_START -->
#### Ká»‹ch báº£n thá»±c hiá»‡n workshop

Workshop Ä‘Æ°á»£c xÃ¢y dá»±ng theo ká»‹ch báº£n má»™t website xem phim cÃ³ hai nhÃ³m ngÆ°á»i dÃ¹ng:

* NgÆ°á»i dÃ¹ng thÆ°á»ng: Ä‘Äƒng kÃ½, Ä‘Äƒng nháº­p, xem phim, chá»n táº­p, báº­t phá»¥ Ä‘á», tiáº¿p tá»¥c xem, yÃªu thÃ­ch vÃ  Ä‘Ã¡nh giÃ¡ phim.
* Quáº£n trá»‹ viÃªn: thÃªm phim, thÃªm táº­p phim, upload video lá»›n lÃªn S3, theo dÃµi tiáº¿n trÃ¬nh MediaConvert vÃ  quáº£n lÃ½ phá»¥ Ä‘á»/banner táº­p.

#### Luá»“ng demo nÃªn trÃ¬nh bÃ y

1. Truy cáº­p domain <code>https://netflop.win</code>.
2. Kiá»ƒm tra danh sÃ¡ch phim, trang chi tiáº¿t phim vÃ  trang xem phim.
3. ÄÄƒng nháº­p tÃ i khoáº£n admin.
4. Upload má»™t táº­p phim MP4/MKV á»Ÿ trang quáº£n trá»‹.
5. Kiá»ƒm tra file Ä‘Ã£ vÃ o S3 input bucket.
6. Kiá»ƒm tra MediaConvert táº¡o HLS trong S3 output bucket.
7. Má»Ÿ táº­p phim trÃªn website Ä‘á»ƒ phÃ¡t tá»« CloudFront.
8. Upload phá»¥ Ä‘á» SRT/VTT vÃ  kiá»ƒm tra subtitle selector.
9. Kiá»ƒm tra lá»‹ch sá»­ xem lÆ°u theo tÃ i khoáº£n.

#### CÃ¡c thÃ nh pháº§n project liÃªn quan

| ThÃ nh pháº§n | ÄÆ°á»ng dáº«n trong source |
| --- | --- |
| Backend API | <code>backend/src</code> |
| Frontend React | <code>frontend/src</code> |
| Admin upload | <code>frontend/src/admin</code> |
| Lambda MediaConvert notifier | <code>aws/lambda/mediaconvert-notifier</code> |
| Lambda subtitle converter | <code>aws/lambda/subtitle-converter</code> |
| Database dump | <code>database/web_xem_phim_final_dump.sql</code> |

<!-- NETFLOP_IMPLEMENTATION_END -->

