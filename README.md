## Project Structure
**Multi Modules Single Project**
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

## Build the Project
```bash
./gradlew :module-api:build
```

<br>

## Modules
- **module-api**: This moudle is reponsible for the API Server.
- **module-domain**: This module is responsible for the domain logic
- **module-common**: This moudle is responsible for common utilities and libraries.

<br>

## Dependency Flow
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
