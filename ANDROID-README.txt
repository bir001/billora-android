BILLORA ANDROID APP — GitHub Actions build package

WHAT THIS PACKAGE DOES
- Builds the native Billora Android app from android-src.zip.
- Names the downloadable APK exactly: Billora.apk.
- Publishes Billora.apk in GitHub Releases and as a workflow artifact.
- Keeps the existing Android application label as "Billora".

UPLOAD THIS PACKAGE TO A NEW GITHUB REPOSITORY
1. Create a GitHub repository, for example: billora-android.
2. Extract this ZIP on your phone or computer.
3. Upload the extracted contents to the ROOT of the repository. The repository must show:
   .github/workflows/build.yml
   android-src.zip
   ANDROID-README.txt
4. Commit the files to the main branch.
5. Open the repository's Actions tab and select "Build Billora APK".
6. Wait for the workflow to finish with a green check.
7. Open Releases and download Billora.apk.
   You can also open the successful workflow run and download the
   "Billora-Android-APK" artifact.

BUILD AGAIN / CHANGE WEBSITE URL
Actions > Build Billora APK > Run workflow. Keep the trailing slash in the URL.
Default website: https://bir001.github.io/Billora/

IMPORTANT
- Upload android-src.zip as-is. Do not unzip it into the repository.
- The APK filename is set by the workflow after Gradle successfully builds it.
- The app's launcher/display name is already "Billora".
- This package preserves the existing application ID: app.billora.pos.
  Do not change it if you want Android to recognize this as the same app.
- The source archive contains the signing keystore used by the existing project.
  Keep the repository private if you do not want that signing material public.
- If GitHub reports a build failure, open the failed Actions run and share the
  first actual error section, not just the red cross.
