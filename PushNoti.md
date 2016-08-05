#google Firebase를 이용한 푸쉬 노티 보내기

- server 
https://firebase.google.com/docs/cloud-messaging/server

```
Map<String,Object> info = new HashMap<String,Object>();
Map<String,Object> notification = new HashMap<String,Object>();
notification.put("title", "notification test");
notification.put("body", "abcd123");
info.put("notification", notification);
info.put("to", #{firebase_user_token});
String url = "https://fcm.googleapis.com/fcm/send";

HttpHeaders headers = new HttpHeaders();
headers.setContentType(MediaType.APPLICATION_JSON);
headers.add("Authorization", "key=" + #{server key});
HttpEntity<Object> request = new HttpEntity<Object>(info,headers);

restTemplate.postForLocation(url, request);

```

- app
https://firebase.google.com/docs/notifications/android/console-device

