# The Android SDK docker build file

Android SD docker image for building Android apps. May be used for CI systems as GitLab, Teamcity, Jenkins...

## Preinstalled packages

- Android SDK Tools
- Android SDK Platform-tools
- Android SDK Build-tools, revision 28.0.3
- SDK Platform Android 9.0, API 28
- Android Support Repository
- Google Repository
- Google APIs Intel x86 Atom System Image (API 28)
- Emulator

## Build Docker

`docker build -t hannesa2/android-sdk .`

and upload it to https://hub.docker.com/ and maybe you have to ``docker login`` in advance

```
TAG_NAME=api28 # <-- change this
docker tag hannesa2/android-sdk hannesa2/android-sdk:$TAG_NAME
docker push hannesa2/android-sdk:$TAG_NAME
```

## Emulator

The build has preinstalled default emulator with Google APIs Intel x86 Atom System Image (API 28) running on Pixel hardware profile.
Emulator can be started as following:

```
/opt/start-default-emulator.sh
```
