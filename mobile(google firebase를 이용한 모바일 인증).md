- google docs
https://developers.google.com/identity/sign-in/android/start

- github
https://github.com/googlesamples/google-services.git

- 인증 플로우

1. 구글에서 프로젝트 생성 서버 Credential 등록

2. firebase의 모바일 프로젝트 등록

3. 모바일 앱에서 발급받은 idToken을 api호출시 서버에 Request해서 서버에서 idToken을 검증하여 사용자를 검증하는 방식

4. idToken을 발급받기위해 firebase의 모바일앱 프로젝트 등록시 Certificate Fingerprints에 해당 기기에 해당하는 키등록 필요


