# Get your School Chat APK (no Android Studio needed)

This uses **GitHub** (free) to build the APK for you. About 5–10 minutes the first time.

---

## Step 1 – Make a free GitHub account
If you don’t have one: https://github.com/signup

## Step 2 – Create a new repository
1. Go to https://github.com/new  
2. **Repository name:** `school-chat-android` (or anything)  
3. Leave it **Public**  
4. Click **Create repository**

## Step 3 – Upload this project
### Easy way (browser)
1. On the new empty repo page, click **uploading an existing file**  
2. Open the unzipped `school-chat-android` folder on your computer  
3. Select **all** files and folders inside it (including `.github`)  
4. Drop them on the page  
5. Click **Commit changes**

> Tip: Make sure `app/`, `.github/`, `gradlew`, and `build.gradle.kts` are all in the **root** of the repo (not inside another folder).

### Or with GitHub Desktop
1. Install https://desktop.github.com  
2. File → Add local repository → choose the `school-chat-android` folder  
3. Publish to GitHub

## Step 4 – Build the APK
1. Open your repo on GitHub  
2. Click the **Actions** tab  
3. Click **Build School Chat APK** on the left  
4. Click **Run workflow** → **Run workflow**  
5. Wait until the yellow dot turns **green** (2–5 minutes)

## Step 5 – Download
1. Click the finished green workflow run  
2. Scroll to **Artifacts**  
3. Download **SchoolChat-APK**  
4. Unzip it – inside is `app-debug.apk`

## Step 6 – Install on your phone
1. Copy `app-debug.apk` to your Android phone (USB, Google Drive, email, etc.)  
2. On the phone, open the file  
3. If it says “blocked”, allow **Install unknown apps** for that app (Files / Chrome / Drive)  
4. Tap **Install**

Done. School Chat opens like a normal app and loads your site.

---

## Optional: change the website URL
Edit `app/src/main/res/values/strings.xml` before uploading:

```xml
<string name="chat_url">https://text-world.nekoweb.org/chat.html</string>
<string name="allowed_host">text-world.nekoweb.org</string>
```

Then commit again – Actions will build a new APK.

---

## Why not a finished APK from me?
Building an Android APK needs Google’s Android SDK and a few GB of memory.  
This chat environment doesn’t have that, so GitHub’s free builders do the compile for you instead.
