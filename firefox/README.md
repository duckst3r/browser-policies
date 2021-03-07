# Firefox Policies

This is an optimized JSON configuration for Firefox/Firefox ESR to meet best security practices.

## Installation

### Linux

1. Change file mode to allow write access only to admin user.
2. Put the `policies.json` file in `/usr/share/firefox/distribution/` directory (`/usr/share/firefox-esr/distribution/` for Firefox ESR).
   It varies by distribution. You can specify system-wide policy by placing the file in `/etc/firefox/policies/`.

### MacOS

1. Change file mode to allow write access only to admin user.
2. Put the `policies.json` file in `Firefox.app/Contents/Resources/distribution`.

### Windows Users 💩

1. Create a directory called distribution where the EXE is located and place the file there
2. That's all folks!

## Documentation Reference

- https://support.mozilla.org/en-US/kb/customizing-firefox-using-policiesjson
- https://github.com/mozilla/policy-templates/blob/master/README.md

## Default Configuration

| Policy Name                  | Description | Value                                                                  |
|------------------------------|-------------|------------------------------------------------------------------------|
| **AppAutoUpdate**            | Enable or disable automatic application update.            | `TRUE`                                                                   |
| **BlockAboutAddons**             | Block access to the Add-ons Manager (about:addons).            | `TRUE`                                                                   |
| **BlockAboutConfig**             | Block access to about:config.            | `TRUE`                                                                   |
| **BlockAboutProfiles**           | Block access to About Profiles (about:profiles).            | `TRUE`                                                                   |
| **BlockAboutSupport**            | Block access to Troubleshooting Information (about:support).            | `TRUE`                                                                   |
| **DefaultDownloadDirectory**     | Set the default download directory.            | `${home}/Downloads`                                                      |
| **DisableAppUpdate**             | Turn off application updates.            | `FALSE`                                                                  |
| **DisableBuiltinPDFViewer**      | Disable the built in PDF viewer.            | `TRUE`                                                                   |
| **DisabledCiphers**              | Disable ciphers.            | `TLS_RSA_WITH_3DES_EDE_CBC_SHA`                                          |
| **DisableDefaultBrowserAgent**   | Prevent the default browser agent from taking any actions (Windows only).            | `TRUE`                                                                   |
| **DisableFormHistory**           | Turn off saving information on web forms and the search bar.            | `TRUE`                                                                   |
| **DisablePasswordReveal**        | Do not allow passwords to be revealed in saved logins.            | `TRUE`                                                                   |
| **DisableProfileImport**         | Disables the "Import data from another browser" option in the bookmarks window.            | `TRUE`                                                                   |
| **DisableProfileRefresh**        | Disable the Refresh Firefox button on about:support and support.mozilla.org            | `TRUE`                                                                   |
| **DisableSafeMode**              | Disable safe mode within the browser.            | `TRUE`                                                                   |
| **DisableSecurityBypass**        | Prevent the user from bypassing security in certain cases.            | `InvalidCertificate` = `TRUE` `SafeBrowsing` = `TRUE`                          |
| **DisableSystemAddonUpdate**     | Prevent system add-ons from being installed or update.            | `FALSE`                                                                  |
| **DisplayMenuBar**               | Set the initial state of the menubar.            | `default-on`                                                             |
| **DontCheckDefaultBrowser**      | Don't check if Firefox is the default browser at startup.            | `TRUE`                                                                   |
| **DownloadDirectory**            | Set and lock the download directory.            | `${home}/Downloads`                                                      |
| **EnableTrackingProtection**     | Configure tracking protection.            | Tracking Protection `Enabled`: `Cryptomining` = `TRUE` `Fingerprinting` = `TRUE` |
| **EncryptedMediaExtensions**     | Configure tracking protection.            | `DISABLED`                                                               |
| **Extensions/ExtensionSettings** | Control the installation, uninstallation and locking of extensions.            | `Disable All` / Force install `uBlock Origin`, `HTTPS Everywhere`            |
| **FlashPlugin**                  | Configure the default Flash plugin policy as well as origins for which Flash is allowed.            | `Block All`                                                      |
| **InstallAddonsPermission**      | Configure the default extension install policy as well as origins for extension installs are allowed.            | `Disallow All`                                                           |
| **OfferToSaveLogins**            | Control whether or not Firefox offers to save passwords.            | `FALSE`                                                                  |
| **OfferToSaveLoginsDefault**     | Set the default value for whether or not Firefox offers to save passwords.            | `FALSE`                                                                  |
| **OverrideFirstRunPage**     | Override the first run page.            |                                                                        |
| **OverridePostUpdatePage**   | Override the upgrade page.            |                                                                        |
| **PasswordManagerEnabled**       | Remove (some) access to the password manager.            | `FALSE`                                                                  |
| **PDFjs**                        | Disable or configure PDF.js, the built-in PDF viewer.            | `DISABLED`                                                               |
| **Permissions: Autoplay**        | Set permissions associated with video autoplay.            | `Block All` / `Block New Requests`                                         |
| **Permissions: Camera**          | Set permissions associated with camera.            | `Block All` / `Block New Requests`                                         |
| **Permissions: Location**        | Set permissions associated with location.            | `Block All` / `Block New Requests`                                         |
| **Permissions: Microphone**      | Set permissions associated with microphone.            | `Block All` / `Block New Requests`                                         |
| **Permissions: Notifications**   | Set permissions associated with notifications.            | `Block All` / `Block New Requests`                                         |
| **Permissions: VirtualReality**  | Set permissions associated with virtual reality.            | `Block All` / `Block New Requests`                                         |
| **PopupBlocking**                | Configure the default pop-up window policy as well as origins for which pop-up windows are allowed.            | `Block All` / `Block New Requests`                                         |
| **PromptForDownloadLocation**    | Ask where to save each file before downloading.            | `FALSE`                                                                  |
| **SSLVersionMax**                | Set and lock the maximum version of TLS.            | `tls1.3`                                                                 |
| **SSLVersionMin**                | Set and lock the minimum version of TLS.            | `tls1.2`                                                                 |

**Notes:**
- Disabled weak cipher suite `TLS_RSA_WITH_3DES_EDE_CBC_SHA` (see https://ciphersuite.info/cs/TLS_RSA_WITH_3DES_EDE_CBC_SHA/)
- Minimum TLS version allowed: `tls1.2`
