
# Sotap

**Sotap** — A lightweight `.so` library for logging the behavior of JNI libraries.

---

##  Highlights
- Logs JNI `.so` library activities automatically.
- Stores logs within the app's internal storage: `/data/user/0/<YourAppPackageName>/files/sotap.log`.
- Can be customized or extended via `sotap.c`.
- **No root required** — MT Manager can grant necessary access without root.

---

##  Table of Contents
- [Description](#description)
- [Usage](#usage)
- [Customization](#customization)
- [Notes](#notes)
- [License](#license)
- [Author](#author)

---

##  Description
**Sotap** is a library (`.so` file) designed for logging and monitoring JNI (`.so`) files within your application.

---

##  Usage
1. Include `Sotap` in your application.
2. Run your app — logs are auto-generated and saved here:

/data/user/0/YourAppPackageName/files/sotap.log

3. If you lack access to the root directory of the app, you can use **MT Manager** to add the necessary permissions — even without root.

---

##  Customization
You can also update or extend the `sotap.c` file to customize or enhance the library for more advanced usage.
