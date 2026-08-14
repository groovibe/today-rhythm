## Android Test APK

이 저장소는 웹앱(GitHub Pages, `index.html`)과 Android 앱을 함께 관리합니다.
GitHub Actions에서 최신 Stage 2.3 Android 소스를 받아 Debug APK를 자동으로 만듭니다.

### 갤럭시에서 최신 테스트 APK 받기

1. GitHub에서 `groovibe/today-rhythm` 저장소 열기
2. 상단 **Actions** 탭 선택
3. 왼쪽 **Build Android Debug APK** 선택
4. 가장 위의 초록색 ✅ 성공 실행 선택
5. 아래 **Artifacts**의 **TodayRhythm-debug-apk** 선택
6. ZIP 다운로드 후 압축 해제
7. **TodayRhythm-v1.0-debug.apk**를 눌러 설치

처음 설치할 때는 다운로드에 사용한 브라우저 또는 파일 앱에 대해 “출처를 알 수 없는 앱 설치”를 한 번 허용해야 할 수 있습니다.

### 첫 GitHub APK 설치 주의

Mac의 Android Studio에서 설치한 기존 테스트 앱과 GitHub Actions APK는 서명이 다를 수 있습니다. 첫 GitHub APK가 기존 앱 위에 설치되지 않으면, 필요한 기록을 JSON으로 백업한 뒤 기존 테스트 앱을 삭제하고 설치하세요.

GitHub Actions는 테스트용 debug keystore를 캐시하므로, 그 이후 GitHub Actions에서 만든 APK끼리는 덮어쓰기 업데이트가 가능하도록 구성했습니다.

Debug APK는 내부 테스트 전용입니다. Play Store 배포용 AAB와 서명 키는 별도로 준비합니다.
