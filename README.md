# CHECKME - Plan • Task • Achieve (ECST Edition)

Java, ViewBinding, Groovy DSL. Android Studio Ladybug, min API 28, target/compile 35.

Open in Android Studio (File > Open > CHECKME). Studio generates the Gradle wrapper jar and syncs.
AGP 8.8.2 / Gradle 8.10.2. Run on a Pixel 6 emulator (API 34).

Notes
- res/raw: your 10 mp3 clips (22.mp3 became sfx_22.mp3 because resource names can't start with a digit).
- pet/SoundCatalog.java: edit the HAPPY / MAD lists to match how each clip actually sounds.
- Developer names: res/values/strings.xml (dev_name_1..6).
- Accounts and tasks are stored on-device (SharedPreferences). Swap in Firebase/Room for sync.

Accounts (this version)
- Several accounts can be registered on one device; each has its own tasks, pet and palette.
- Forgot Password: the security question chosen at sign-up resets the password (answers are stored hashed).
  Accounts made by older builds have no question and cannot be reset; create a new account instead.
- Profile > My Account lists every account; other accounts open only with their own password.
- The info button on Home (top right) opens a short description of CHECK ME.
- Tapping the pet on Home pops up a chat head with a motivational quote; a sad/mad/happy pet also says why ("Foxy is sad because...").
- Progress screen: themed card per palette + pet ("SAGE FOX 2026 PROGRESS"), tappable pet, statuses and week faces.
