# Sotap

**Sotap** — A lightweight `.so` library for logging the behavior of JNI libraries.

---

## ✨ Highlights
- 📝 Logs JNI `.so` library activities automatically.
- 📂 Stores logs within the app's internal storage:  
  `/data/user/0/<YourAppPackageName>/files/sotap.log`
- ⚙️ Can be customized or extended via `sotap.c`.
- 🔓 **No root required** — MT Manager can grant necessary access without root.

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
