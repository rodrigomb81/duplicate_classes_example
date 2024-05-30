# Description

This repo demonstrates a build error on Android that shows up when share_plus is added to the project.

This project was created running `flutter create --platforms android` and share_plus was added to pubspec.
No other modifications were made.

## Output of flutter doctor -v

```
[✓] Flutter (Channel stable, 3.22.0, on Ubuntu 24.04 LTS 6.8.0-31-generic, locale en_US.UTF-8)
    • Flutter version 3.22.0 on channel stable at /home/rodri/fvm/versions/3.22.0
    • Upstream repository https://github.com/flutter/flutter.git
    • Framework revision 5dcb86f68f (3 weeks ago), 2024-05-09 07:39:20 -0500
    • Engine revision f6344b75dc
    • Dart version 3.4.0
    • DevTools version 2.34.3

[✓] Android toolchain - develop for Android devices (Android SDK version 34.0.0)
    • Android SDK at /home/rodri/Android/Sdk
    • Platform android-34, build-tools 34.0.0
    • Java binary at: /home/rodri/Programas/android-studio-2023.3.1.19-linux/android-studio/jbr/bin/java
    • Java version OpenJDK Runtime Environment (build 17.0.10+0-17.0.10b1087.21-11572160)
    • All Android licenses accepted.

[✓] Chrome - develop for the web
    • Chrome at google-chrome

[✓] Linux toolchain - develop for Linux desktop
    • Ubuntu clang version 18.1.3 (1)
    • cmake version 3.28.3
    • ninja version 1.11.1
    • pkg-config version 1.8.1

[✓] Android Studio (version 2023.3)
    • Android Studio at /home/rodri/Programas/android-studio-2023.3.1.19-linux/android-studio
    • Flutter plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/9212-flutter
    • Dart plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/6351-dart
    • Java version OpenJDK Runtime Environment (build 17.0.10+0-17.0.10b1087.21-11572160)

[✓] IntelliJ IDEA Community Edition (version 2024.1)
    • IntelliJ at /home/rodri/Programas/idea/idea-IC-241.17011.79
    • Flutter plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/9212-flutter
    • Dart plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/6351-dart

[✓] VS Code (version 1.89.1)
    • VS Code at /usr/share/code
    • Flutter extension version 3.90.0

[✓] Connected device (2 available)
    • Linux (desktop) • linux  • linux-x64      • Ubuntu 24.04 LTS 6.8.0-31-generic
    • Chrome (web)    • chrome • web-javascript • Google Chrome 125.0.6422.60

[✓] Network resources
    • All expected network resources are available.

• No issues found!
```

## Output of flutter build apk --release

```
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:checkReleaseDuplicateClasses'.
> A failure occurred while executing com.android.build.gradle.internal.tasks.CheckDuplicatesRunnable
   > Duplicate class kotlin.collections.jdk8.CollectionsJDK8Kt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.internal.jdk7.JDK7PlatformImplementations found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.internal.jdk7.JDK7PlatformImplementations$ReflectSdkVersion found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.internal.jdk8.JDK8PlatformImplementations found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.internal.jdk8.JDK8PlatformImplementations$ReflectSdkVersion found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.io.path.ExperimentalPathApi found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.io.path.PathRelativizer found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.io.path.PathsKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.io.path.PathsKt__PathReadWriteKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.io.path.PathsKt__PathUtilsKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.jdk7.AutoCloseableKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk7-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk7:1.7.10)
     Duplicate class kotlin.jvm.jdk8.JvmRepeatableKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.jvm.optionals.OptionalsKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.random.jdk8.PlatformThreadLocalRandom found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.streams.jdk8.StreamsKt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.streams.jdk8.StreamsKt$asSequence$$inlined$Sequence$1 found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.streams.jdk8.StreamsKt$asSequence$$inlined$Sequence$2 found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.streams.jdk8.StreamsKt$asSequence$$inlined$Sequence$3 found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.streams.jdk8.StreamsKt$asSequence$$inlined$Sequence$4 found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.text.jdk8.RegexExtensionsJDK8Kt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)
     Duplicate class kotlin.time.jdk8.DurationConversionsJDK8Kt found in modules jetified-kotlin-stdlib-1.8.22 (org.jetbrains.kotlin:kotlin-stdlib:1.8.22) and jetified-kotlin-stdlib-jdk8-1.7.10 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.7.10)

     Go to the documentation to learn how to <a href="d.android.com/r/tools/classpath-sync-errors">Fix dependency resolution errors</a>.

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 25s
Running Gradle task 'assembleRelease'...                           26.0s
Gradle task assembleRelease failed with exit code 1
```