# iOS ARM64 Protocol Buffers

Adapted from https://gist.github.com/BennettSmith/9487468ae3375d0db0cc

This modification only builds the ARM64 bytecode for Google Protobuf Buffers v3.0.0-beta-2.

Creates include directories and .a static libs appropriate for static linking into an iOS app.

Example CMake integration:
- run `./build-protofbuf.sh`
- add CMake statement `INCLUDE_DIRECTORIES(./protobuf/include)`
- add Cmake statement `TARGET_LINK_LIBRARY(${APP_NAME} ${PROJECT_SOURCE_DIR}/protobuf/platform/arm64-ios/lib/lib-protobuf-lite.a)`

And your app will have a c++ protocol buffers runtime! (on arm64, of course)

