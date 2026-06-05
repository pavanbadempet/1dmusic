## 2024-06-05 - Disabled android:allowBackup in AndroidManifest.xml
**Vulnerability:** The application was configured with `android:allowBackup="true"`. This allows application data to be backed up via `adb backup`, potentially exposing sensitive user data to an attacker with physical access to the device or debugging capabilities.
**Learning:** Found that this default configuration is an easy oversight in Android applications.
**Prevention:** Always verify `android:allowBackup` is explicitly set to `false` in `AndroidManifest.xml` unless specifically required and configured securely.
