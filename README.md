# Sotap

**Sotap** — A lightweight `.so` library for logging the behavior of JNI libraries.

---

## ✨ Highlights
- Logs JNI `.so` library activities automatically.
- Stores logs within the app's internal storage: `/data/user/0/<YourAppPackageName>/files/sotap.log`.
- Can be customized or extended via `sotap.c`.
- **No root required** — MT Manager can grant necessary access without root.

---

## 📄 Description
**Sotap** is a library (`.so` file) designed for logging and monitoring JNI (`.so`) files within your application.

---

## ▶️ Usage

**Step 1: Download and Add Library**  
- Download the file **`libs.zip`** from the [Releases](../../releases) section.  
- Extract and move the proper architecture folder (e.g., `arm64-v8a`, `armeabi-v7a`) into your app.  

---

**Step 2: Load Sotap Before Everything Else**  
In your **smali** code, make sure to load `sotap` first:  

```smali
const-string v0, "sotap"

invoke-static {v0}, Ljava/lang/System;->loadLibrary(Ljava/lang/String;)V```
---

**Step 3: Run Your App

Launch your application.

Logs will be generated automatically and saved at:


/data/user/0/YourAppPackageName/files/sotap.log
