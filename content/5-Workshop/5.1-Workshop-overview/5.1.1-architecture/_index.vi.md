---
title: "Kiáº¿n trÃºc tá»•ng quan"
date: 2026-07-10
weight: 1
chapter: false
pre: " <b> 5.1.1. </b> "
---

#### Má»¥c tiÃªu kiáº¿n trÃºc

Kiáº¿n trÃºc Netflop tÃ¡ch á»©ng dá»¥ng web, database, lÆ°u trá»¯ media, xá»­ lÃ½ video, phÃ¡t ná»™i dung vÃ  giÃ¡m sÃ¡t thÃ nh cÃ¡c lá»›p riÃªng. CÃ¡ch tÃ¡ch nÃ y giÃºp há»‡ thá»‘ng dá»… váº­n hÃ nh hÆ¡n, háº¡n cháº¿ viá»‡c lÆ°u file lá»›n trÃªn EC2 vÃ  táº¡o ná»n táº£ng Ä‘á»ƒ má»Ÿ rá»™ng vá» sau.

#### Luá»“ng truy cáº­p chÃ­nh

```text
User / Admin
   |
   v
Cloudflare DNS + HTTPS
   |
   v
netflop.win
   |
   v
EC2 netflop-web
   |-- Nginx reverse proxy
   |-- React frontend build
   |-- Node.js backend API
   |
   |---- RDS MySQL netflop-db
   |
   |---- S3 netflop-input-source
   |          |
   |          v
   |      AWS Elemental MediaConvert
   |          |
   |          v
   |---- S3 netflop-output-source
              |
              v
        CloudFront protected HLS
              |
              v
        Video Player
```

#### Luá»“ng ngÆ°á»i dÃ¹ng

1. NgÆ°á»i dÃ¹ng truy cáº­p `https://netflop.win`.
2. Cloudflare xá»­ lÃ½ DNS vÃ  HTTPS phÃ­a public domain.
3. Request Ä‘Æ°á»£c chuyá»ƒn Ä‘áº¿n EC2.
4. Nginx tráº£ frontend React hoáº·c proxy request `/api/*` Ä‘áº¿n backend Node.js.
5. Backend Ä‘á»c/ghi dá»¯ liá»‡u phim, tÃ i khoáº£n, lá»‹ch sá»­ xem, tiáº¿p tá»¥c xem, yÃªu thÃ­ch, Ä‘Ã¡nh giÃ¡ vÃ  bÃ¬nh luáº­n trong RDS MySQL.
6. Khi ngÆ°á»i dÃ¹ng xem phim, backend cáº¥p phiÃªn stream vÃ  trÃ¬nh phÃ¡t láº¥y HLS tá»« CloudFront.

#### Luá»“ng admin upload video

1. Admin chá»n phim, táº­p phim vÃ  file video MP4/MKV trÃªn trang quáº£n trá»‹.
2. Backend táº¡o báº£n ghi táº­p phim á»Ÿ tráº¡ng thÃ¡i Ä‘ang xá»­ lÃ½.
3. File gá»‘c Ä‘Æ°á»£c upload lÃªn S3 bucket `netflop-input-source`.
4. Backend táº¡o job MediaConvert.
5. MediaConvert chuyá»ƒn video sang HLS nhiá»u Ä‘á»™ phÃ¢n giáº£i: 360p, 480p, 720p vÃ  1080p.
6. Output HLS Ä‘Æ°á»£c lÆ°u vÃ o S3 bucket `netflop-output-source`.
7. EventBridge báº¯t tráº¡ng thÃ¡i MediaConvert vÃ  gá»i Lambda.
8. Lambda gá»i webhook backend Ä‘á»ƒ cáº­p nháº­t tráº¡ng thÃ¡i táº­p phim trong database.
9. Website tá»± hiá»ƒn thá»‹ tráº¡ng thÃ¡i hoÃ n thÃ nh, khÃ´ng cáº§n admin báº¥m sync thá»§ cÃ´ng.

#### Luá»“ng tá»± Ä‘á»™ng cáº­p nháº­t tráº¡ng thÃ¡i

```text
MediaConvert COMPLETE / ERROR / CANCELED
   |
   v
EventBridge rule netflop-mediaconvert-job-state-change
   |
   v
Lambda netflop-mediaconvert-notifier
   |
   v
Backend webhook /api/uploads/mediaconvert/events
   |
   v
Update episode upload_status in RDS
```

#### Luá»“ng phá»¥ Ä‘á»

```text
Admin upload .srt hoáº·c .vtt
   |
   v
S3 input/output
   |
   v
Lambda chuyá»ƒn .srt sang .vtt náº¿u cáº§n
   |
   v
Video Player load subtitle track
```

![](/2280600178_huynhduybao_workshopaws/images/5-Workshop/5.1-Workshop-overview/5.1.1-architecture/sodo.png)

<!-- NETFLOP_DETAIL_START -->
#### CÃ¡ch thá»±c hiá»‡n kiáº¿n trÃºc

Kiáº¿n trÃºc Ä‘Æ°á»£c triá»ƒn khai theo tá»«ng lá»›p:

1. Lá»›p domain: Cloudflare quáº£n lÃ½ DNS cá»§a <code>netflop.win</code>.
2. Lá»›p application: EC2 cháº¡y Nginx, frontend React build vÃ  backend Node.js.
3. Lá»›p database: RDS MySQL lÆ°u dá»¯ liá»‡u phim vÃ  ngÆ°á»i dÃ¹ng.
4. Lá»›p media: S3 input lÆ°u video gá»‘c, MediaConvert táº¡o HLS, S3 output lÆ°u káº¿t quáº£.
5. Lá»›p delivery: CloudFront phÃ¢n phá»‘i HLS vÃ  báº£o vá»‡ stream báº±ng signed cookies.
6. Lá»›p automation: EventBridge vÃ  Lambda cáº­p nháº­t tráº¡ng thÃ¡i MediaConvert.
7. Lá»›p monitoring: CloudWatch vÃ  SNS theo dÃµi há»‡ thá»‘ng.

#### File code liÃªn quan trong source

| ThÃ nh pháº§n | File liÃªn quan |
| --- | --- |
| Káº¿t ná»‘i RDS | <code>backend/src/config/database.js</code> |
| Upload S3 | <code>backend/src/services/awsS3.service.js</code> |
| Táº¡o MediaConvert job | <code>backend/src/services/mediaConvert.service.js</code> |
| Webhook MediaConvert | <code>backend/src/controllers/upload.controller.js</code> |
| Signed cookies | <code>backend/src/services/cloudFrontSignedCookie.service.js</code> |
| Player HLS | <code>frontend/src/components/VideoPlayer.jsx</code> |
| Lambda phá»¥ Ä‘á» | <code>aws/lambda/subtitle-converter/index.mjs</code> |

#### Code máº«u: luá»“ng backend táº¡o job xá»­ lÃ½ video

~~~js
const uploaded = await awsS3Service.uploadVideo(req.file, { movieId, episodeName });
const pendingEpisode = await episodeModel.createUploadEpisode({
  movieId,
  name: episodeName,
  sourceUrl: uploaded.s3Uri,
  uploadStatus: 'uploaded'
});

const job = await mediaConvertService.createHlsJob({
  inputS3Uri: uploaded.s3Uri,
  movieId,
  episodeId: pendingEpisode.MaTap
});
~~~
<!-- NETFLOP_DETAIL_END -->

<!-- NETFLOP_IMPLEMENTATION_START -->
#### Kiáº¿n trÃºc triá»ƒn khai theo project Netflop

Kiáº¿n trÃºc hiá»‡n táº¡i váº«n lÃ  mÃ´ hÃ¬nh web truyá»n thá»‘ng cháº¡y trÃªn EC2, káº¿t há»£p cÃ¡c dá»‹ch vá»¥ managed cá»§a AWS cho database, media, CDN vÃ  monitoring. Backend Node.js khÃ´ng lÆ°u file video lá»›n trÃªn á»• Ä‘Ä©a EC2, mÃ  chá»‰ Ä‘iá»u phá»‘i upload vÃ  lÆ°u metadata vÃ o RDS.

#### Luá»“ng request chÃ­nh

1. NgÆ°á»i dÃ¹ng truy cáº­p <code>netflop.win</code> qua Cloudflare.
2. Nginx trÃªn EC2 phá»¥c vá»¥ frontend React Ä‘Ã£ build.
3. CÃ¡c request <code>/api/*</code> Ä‘Æ°á»£c reverse proxy vá» Node.js backend cháº¡y báº±ng PM2.
4. Backend Ä‘á»c/ghi dá»¯ liá»‡u phim, ngÆ°á»i dÃ¹ng, táº­p phim, lá»‹ch sá»­ xem trong RDS MySQL.
5. Video admin upload Ä‘i vÃ o S3 input bucket.
6. Backend táº¡o MediaConvert job Ä‘á»ƒ xuáº¥t HLS sang S3 output bucket.
7. Player phÃ¡t HLS qua CloudFront, cÃ³ thá»ƒ báº£o vá»‡ báº±ng signed cookies.

#### SÆ¡ Ä‘á»“ luá»“ng upload vÃ  xem phim

~~~text
Admin browser
  -> React admin
  -> Backend API /uploads/videos/multipart/*
  -> S3 input bucket
  -> MediaConvert
  -> S3 output bucket
  -> CloudFront
  -> Video player
~~~

#### File source thá»ƒ hiá»‡n kiáº¿n trÃºc

| Má»¥c | File |
| --- | --- |
| Khá»Ÿi táº¡o server | <code>backend/src/server.js</code> |
| Route tá»•ng | <code>backend/src/routes/index.js</code> |
| Káº¿t ná»‘i RDS | <code>backend/src/config/database.js</code> |
| Upload S3 | <code>backend/src/services/awsS3.service.js</code> |
| Táº¡o MediaConvert job | <code>backend/src/services/mediaConvert.service.js</code> |
| Player HLS | <code>frontend/src/components/VideoPlayer.jsx</code> |

#### Code máº«u káº¿t ná»‘i database

~~~js
const pool = mysql.createPool({
  host: env.db.host,
  port: env.db.port,
  database: env.db.database,
  user: env.db.user,
  password: env.db.password,
  waitForConnections: true,
  connectionLimit: env.db.connectionLimit,
  charset: 'utf8mb4',
  namedPlaceholders: true
});

pool.execute = pool.query.bind(pool);
~~~

<!-- NETFLOP_IMPLEMENTATION_END -->

