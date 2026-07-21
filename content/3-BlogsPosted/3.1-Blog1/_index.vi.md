---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
![So sanh FFmpeg tren EC2 voi AWS Elemental MediaConvert](/images/3-BlogsPosted/3.1-Blog1/ffmpeg-vs-mediaconvert.png)

BÃ i 1: Táº¡i sao nhÃ³m mÃ¬nh chá»n AWS Elemental MediaConvert thay vÃ¬ FFmpeg?

Xin chÃ o má»i ngÆ°á»i,

Trong quÃ¡ trÃ¬nh thá»±c hiá»‡n dá»± Ã¡n **Netflop - Website xem phim trÃªn ná»n táº£ng AWS**, nhÃ³m mÃ¬nh Ä‘Ã£ cÃ³ cÆ¡ há»™i tÃ¬m hiá»ƒu vÃ  triá»ƒn khai nhiá»u dá»‹ch vá»¥ AWS Ä‘á»ƒ xÃ¢y dá»±ng má»™t media pipeline hoÃ n chá»‰nh. Má»™t trong nhá»¯ng quyáº¿t Ä‘á»‹nh khiáº¿n nhÃ³m máº¥t khÃ¡ nhiá»u thá»i gian Ä‘á»ƒ cÃ¢n nháº¯c lÃ  lá»±a chá»n giáº£i phÃ¡p encode video.

Ban Ä‘áº§u, nhÃ³m dá»± Ä‘á»‹nh sá»­ dá»¥ng **FFmpeg cháº¡y trá»±c tiáº¿p trÃªn Amazon EC2** Ä‘á»ƒ chuyá»ƒn Ä‘á»•i video sau khi upload. Tuy nhiÃªn, sau khi thá»­ nghiá»‡m vá»›i nhiá»u video cÃ³ dung lÆ°á»£ng lá»›n, CPU cá»§a EC2 thÆ°á»ng xuyÃªn hoáº¡t Ä‘á»™ng á»Ÿ má»©c cao, thá»i gian xá»­ lÃ½ kÃ©o dÃ i vÃ  viá»‡c quáº£n lÃ½ nhiá»u tÃ¡c vá»¥ encode Ä‘á»“ng thá»i trá»Ÿ nÃªn khÃ¡ phá»©c táº¡p.

Sau khi tÃ¬m hiá»ƒu thÃªm, nhÃ³m quyáº¿t Ä‘á»‹nh chuyá»ƒn sang sá»­ dá»¥ng **AWS Elemental MediaConvert**, káº¿t há»£p vá»›i **Amazon S3, Amazon CloudFront, Amazon EventBridge vÃ  AWS Lambda** Ä‘á»ƒ xÃ¢y dá»±ng quy trÃ¬nh xá»­ lÃ½ video tá»± Ä‘á»™ng.

Sau má»™t thá»i gian triá»ƒn khai, nhÃ³m nháº­n tháº¥y má»™t sá»‘ lá»£i Ã­ch rÃµ rá»‡t:

âœ… Tá»± Ä‘á»™ng chuyá»ƒn Ä‘á»•i video sang chuáº©n **HLS** vá»›i nhiá»u cháº¥t lÆ°á»£ng (360p, 480p, 720p, 1080p).

âœ… Giáº£m táº£i Ä‘Ã¡ng ká»ƒ cho EC2 vÃ¬ toÃ n bá»™ quÃ¡ trÃ¬nh encode Ä‘Æ°á»£c thá»±c hiá»‡n bá»Ÿi MediaConvert.

âœ… Tá»± Ä‘á»™ng cáº­p nháº­t tráº¡ng thÃ¡i phim sau khi encode hoÃ n táº¥t thÃ´ng qua **EventBridge + Lambda**.

âœ… Kiáº¿n trÃºc dá»… má»Ÿ rá»™ng khi sá»‘ lÆ°á»£ng video hoáº·c ngÆ°á»i dÃ¹ng tÄƒng lÃªn.

Qua dá»± Ã¡n nÃ y, nhÃ³m mÃ¬nh nháº­n ra ráº±ng viá»‡c sá»­ dá»¥ng cÃ¡c **Managed Services** cá»§a AWS khÃ´ng chá»‰ giÃºp giáº£m khá»‘i lÆ°á»£ng váº­n hÃ nh mÃ  cÃ²n giÃºp há»‡ thá»‘ng á»•n Ä‘á»‹nh vÃ  dá»… má»Ÿ rá»™ng hÆ¡n so vá»›i viá»‡c tá»± triá»ƒn khai má»i thá»© trÃªn mÃ¡y chá»§.

ÄÃ¢y lÃ  má»™t tráº£i nghiá»‡m ráº¥t thÃº vá»‹ Ä‘á»‘i vá»›i nhÃ³m trong quÃ¡ trÃ¬nh há»c táº­p vÃ  thá»±c hiá»‡n dá»± Ã¡n.

KhÃ´ng biáº¿t anh/chá»‹ vÃ  cÃ¡c báº¡n trong cá»™ng Ä‘á»“ng Ä‘Ã£ tá»«ng sá»­ dá»¥ng **AWS Elemental MediaConvert** hoáº·c giáº£i phÃ¡p nÃ o khÃ¡c cho há»‡ thá»‘ng video streaming chÆ°a? Ráº¥t mong Ä‘Æ°á»£c láº¯ng nghe nhá»¯ng chia sáº» vÃ  gÃ³p Ã½ Ä‘á»ƒ nhÃ³m cÃ³ thá»ƒ tiáº¿p tá»¥c hoÃ n thiá»‡n dá»± Ã¡n.

Xin cáº£m Æ¡n má»i ngÆ°á»i Ä‘Ã£ dÃ nh thá»i gian Ä‘á»c bÃ i!

ðŸ“š Link tham kháº£o
[https://aws.amazon.com/mediaconvert/](https://aws.amazon.com/mediaconvert/)
[https://docs.aws.amazon.com/mediaconvert/latest/ug/what-is.html](https://docs.aws.amazon.com/mediaconvert/latest/ug/what-is.html?utm_source=chatgpt.com)
[https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-jobs.html](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-jobs.html)

