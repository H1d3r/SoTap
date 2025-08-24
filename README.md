# Sotap

**Sotap** — A lightweight `.so` library for logging the behavior of JNI libraries.

How to work with SoTap? https://t.me/ForYouTillEnd/13
---

## ✨ Highlights
- 📝 Logs JNI `.so` library activities automatically.
- 📂 Stores logs within the app's internal storage:  
  `/data/user/0/<YourAppPackageName>/files/sotap.log`
- ⚙️ Can be customized or extended via `sotap.c`.
- 🔓 **No root required** — MT Manager can grant necessary access without root.
- 🫠 SoTap 
uses multiple paths for storage. If it fails, it prints it in logcat.

 "/data/user/0/%s/files/sotap.log"
 
"/data/data/%s/files/sotap.log" 

"/sdcard/Android/data/%s/files/sotap.log" 

"/sdcard/Download/sotap-%s.log" 

"all writable paths failed; fallback to Logcat only.

---

## 📄 Description
**Sotap** is a library (`.so` file) designed for logging and monitoring JNI (`.so`) files within your application.

---

## ▶️ Usage

**📥 Step 1: Download and Add Library**  
- Download **`libs.zip`** from the [Releases](../../releases) section.  
- Extract and copy the proper ABI folder (`arm64-v8a`, `armeabi-v7a`, …) into your app.

---

**⚙️ Step 2: Load Sotap Before Everything Else**  
Add this to your **smali** so `sotap` loads first:
```smali
const-string v0, "sotap"
invoke-static {v0}, Ljava/lang/System;->loadLibrary(Ljava/lang/String;)V
