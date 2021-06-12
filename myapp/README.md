# myapp

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## Build and Run
```
flutter run -d chrome
flutter build web
```

## Run in Nginx Docker
* Build flutter for web and docker image. 
  ```
  flutter build web
  docker build -f nginx/Dockerfile -t flutter-myapp-web .
  docker run -d -p 8060:8060 --name flutter-myapp-web flutter-myapp-web
  ```
* Open app in your browser.
  ```
  http://localhost:8060
  ```
* Stop flutter app in docker.
  ```
  docker stop flutter-myapp-web
  docker rm flutter-myapp-web
  ```
