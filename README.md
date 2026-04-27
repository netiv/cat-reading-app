# 고양이 독서일지 - Android APK 빌드 가이드

## 프로젝트 구조
```
cat-reading-app/
├── www/                  ← 웹 앱 소스 (index.html)
├── android/              ← Android 프로젝트 (Android Studio에서 열기)
├── capacitor.config.json
└── package.json
```

## APK 빌드 방법 (Android Studio)

### 1단계: Android Studio 설치
- https://developer.android.com/studio 에서 다운로드

### 2단계: 프로젝트 열기
- Android Studio 실행
- [Open] 클릭 → `android/` 폴더 선택
- Gradle sync 자동 실행 (인터넷 연결 필요, 5~10분 소요)

### 3단계: APK 빌드
- 메뉴: Build → Build Bundle(s) / APK(s) → Build APK(s)
- 완료 후 우하단 팝업에서 [locate] 클릭
- 경로: android/app/build/outputs/apk/debug/app-debug.apk

### 4단계: 기기에 설치
- APK 파일을 카카오톡, 구글 드라이브 등으로 기기 전송
- 기기에서 파일 탭 → 설치
- (최초 1회) 설정 → 보안 → 출처를 알 수 없는 앱 허용

## 앱 수정 후 재빌드 방법
1. `www/index.html` 수정
2. 터미널에서: `npx cap sync`
3. Android Studio에서 APK 재빌드

## 앱 정보
- 패키지명: com.catreading.momo
- 최소 Android: API 22 (Android 5.1)
- 대상 Android: API 최신
