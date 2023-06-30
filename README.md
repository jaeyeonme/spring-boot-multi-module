## Project Structure
```
root (com.example)
├── build.gradle
└── settings.gradle
└── module-api
│   ├── build.gradle
│   └── src
│       └── main
│           └── java
│               └── com
│                   └── example
│                       └── moduleapi
│                           └── ApiApplication.java (Spring Boot Application)
└── module-common
│   ├── build.gradle
│   └── src
│       └── main
│           └── java
│               └── com
│                   └── example
│                       └── modulecommon
└── module-domain
    ├── build.gradle
    └── src
        └── main
            └── java
                └── com
                    └── example
                        └── moduledomain
```

<br>

## 프로젝트 빌드
```bash
./gradlew :module-api:build
```

<br>

## 모듈의 역할
- **module-api**: API 서버를 담당하는 모듈
- **module-domain**: 도메인 로직을 담당하는 모듈
- **module-common**: 공통 유틸리티 및 라이브러리를 담당하는 모듈

<br>

## 모듈 간 의존성 흐름
```lua
+----------------+
|  module-api    |
|                |
+----------------+
        ^
        |
+-------------------+
|  module-domain   |
|                  |
+-------------------+
        ^
        |
+----------------+
| module-common  |
|                |
+----------------+
```
