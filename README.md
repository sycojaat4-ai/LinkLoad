<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/a815b5b5-140b-4629-ab47-b6ca8ccb1ea8

## Run Locally

**Prerequisites:**  [Android Studio](https://developer.android.com/studio)


1. Open Android Studio
2. Select **Open** and choose the directory containing this project
3. Allow Android Studio to fix any incompatibilities as it imports the project.
4. Create a file named `.env` in the project directory and set `GEMINI_API_KEY` in that file to your Gemini API key (see `.env.example` for an example)
5. Remove this line from the app's `build.gradle.kts` file: `signingConfig = signingConfigs.getByName("debugConfig")`
6. Run the app on an emulator or physical device
7. If you have already published your app in AI Studio, please [request upload key reset](https://support.google.com/googleplay/android-developer/answer/9842756#zippy=%2Crequest-an-upload-key-reset) in Google Play Console.


## Mobile cloud build (GitHub Actions)

1. Upload the contents of this project folder to the root of a GitHub repository (not the outer ZIP).
2. Keep `.github/workflows/build-apk.yml` in the repository.
3. Open the repository's **Actions** tab and run **Build LinkLoad Debug APK**, or push a commit to `main`.
4. When the run succeeds, open the run and download the `LinkLoad-debug-APK` artifact. Extract that ZIP to get the debug APK.

This workflow uses Gradle 9.3.1 and Java 17 and does not require a Gradle wrapper in the source archive. A successful workflow is not guaranteed until the actual build runs.
