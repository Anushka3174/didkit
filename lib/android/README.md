# DIDKit - Android

[Android Library (AAR file)][AAR] for DIDKit. The AAR file includes Java class files using [JNI][], and binary shared libraries for Android's supported architectures (x86, armeabi-v7a, arm64-v8a, x86\_64). The AAR can be added to existing Android projects using Android Studio or Gradle.

## Requires

Android SDK and NDK for Linux x86\_64. The Android SDK is expected to be installed at `~/Android/Sdk`. If it is somewhere else instead, you can specify it with a Make variable, e.g. `make ANDROID_SDK_ROOT=/other/location/android-sdk`

Rust Android targets are also required. To install those with `rustup`, run:
```sh
$ make -C ../ install-rustup-android
```

## Build

```sh
$ make -C ../ ../target/test/aar.stamp
```

### Make variables

- `ANDROID_SDK_ROOT` - path to Android SDK. Default: `~/Android/Sdk`
- `ANDROID_TOOLS` - Android tools directory. Default is to pick one matching `$(ANDROID_SDK_ROOT)/build-tools/*`.
- `ANDROID_NDK_HOME` - Android NDK directory. Default is `$(ANDROID_SDK_ROOT)/ndk-bundle)` if exists, or one matching `$(ANDROID_SDK_ROOT)/ndk/*`.

[AAR]: https://developer.android.com/studio/projects/android-library.html#aar-contents
[JNI]: https://en.wikipedia.org/wiki/Java_Native_Interface
