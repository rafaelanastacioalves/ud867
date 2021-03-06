# Gradle for Android and Java Final Project
## Summary

### Structure

<img src="/FinalProject/photos/main_screen.png" width="200"> <img src="/FinalProject/photos/joke_phrase_screen.png" width="200"> 

In this project, it was created a very simple app that has multiple flavors, uses multiple libraries and uses local Google Could Endpoints. The app just shows a simple phrase after clicking a button. There is the "free" version that shows embedded "Ads" and a "paid" fake version without the "Ads". The purpose is to make an Android project that consists of four modules structured by me:

<img src="/FinalProject/photos/photo_build_it_bigger.png" width="600">

* A Java library that provides jokes phrases (just "a Joke"), 
* a Google Cloud Endpoints (GCE) project that serves those jokes (adapted from this [template](https://github.com/GoogleCloudPlatform/gradle-appengine-templates/tree/master/HelloEndpoints)),
* an Android Library containing an activity for displaying jokes,
* and an Android app that fetches jokes from the GCE module and passes them to the Android Library for display.

### Gradle Integration Task

Additionally, I've created a gradle task, called "integrationTest" that does the following:
* Starts a local development GCE;
* Execute functional tests (I've added just a simple one);
* Shutdown the local development GCE.


## Instructions

### To see the app in action

1. Start the local development GCE: run `./gradlew :backend:appengineRun`;
2. Deploy the free or the paid version of the app to an emulator connected;
to the same wifi as of the started GCE;

### To see the "integrationTest" task in action

1. Shutdown any local development GCE, if started: run `./gradlew :backend:appengineStop`;
2. Start an AVD (recommended);
3. Run: `./gradlew integrationTest`;
