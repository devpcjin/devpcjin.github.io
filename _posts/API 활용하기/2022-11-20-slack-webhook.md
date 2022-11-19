---
title: "Slack WeebHook"

categories: [API 활용하기, Slack]
tags: [Slack, API, Weebhook, incoming]

date: 2022-11-20
last_modified_at: 2022-11-20
---

Slack webhook incoming API 활용
{:.notice--primary}

## 1. Webhook 생성
### 원하는 채널에 Webhook app 추가
1. 해당 채널 통합에서 앱추가 클릭
![](https://velog.velcdn.com/images/pc_jin/post/22fdd294-ce6c-4cd7-bf4d-fab28b181346/image.png)
2. Webhook 검색 및 설치
![](https://velog.velcdn.com/images/pc_jin/post/1eb3dfa9-ec7d-4f66-b118-ac6a18f94a07/image.png)
3. 원하는 채널 선택 후 앱 추가
![](https://velog.velcdn.com/images/pc_jin/post/3d5be1a1-7033-4f56-8b46-ecb0b81a155d/image.png)
4. Webhook URL 기억하기
![](https://velog.velcdn.com/images/pc_jin/post/3f333bdb-2217-4557-bca2-c5ef8df2ed48/image.png)




## 2. Kotlin 코드 작성
### SlackWebhookService.kt
<script src="https://gist.github.com/devpcjin/a6739da8cf373d53743faa2a143c8c0f.js"></script>

### SlackWebhookController.kt
<script src="https://gist.github.com/devpcjin/4ce6428e850aa52559ab7f3bf1d5c86e.js"></script>

추가로 `RestTemplate`를 빈으로 주입 시켜야하는데, 그것은 다시 정리해서 따로 올리도록 하겠다!

자세한 내용은 [github](https://github.com/devpcjin/SlackApi_webhook) 참고

## 3. 테스트
### 1) Post man으로 전송
![](https://velog.velcdn.com/images/pc_jin/post/e47e823c-096e-4345-8bbe-d7a8db016d41/image.png)

### 2) Slack에서 전송 확인
![](https://velog.velcdn.com/images/pc_jin/post/17fa4288-7e1d-4aab-9da8-6d1d98a265a6/image.png)

> 메시지 전송 형식(`attachments`)은 
https://roseline.oopy.io/4d14964c-53fc-4b65-9e53-026fc52cb9cb
이곳을 참고