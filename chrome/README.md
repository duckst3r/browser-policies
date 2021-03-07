# Chrome Policies

This is an optimized JSON configuration for Chrome to meet best security and privacy practices.

## Installation

### Linux

1. Change both file mode to allow write access only to admin user.
2. Put the `test_policies.json` file in `/etc/chrome/policies/managed/` directory (`/etc/chromium/policies/managed/` for Chromium).
3. Put the `master_preferences` file in `/usr/share/chrome/` directory (`/usr/share/chromium` for Chromium).

### MacOS

1. Change both file mode to allow write access only to admin user.
2. Put the `test_policies.json` file in `/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome` directory.
3. Put the `master_preferences` file in `~/Library/Application\ Support/Google/Chrome/Google\ Chrome\ Master\ Preferences` directory or `/Library/Google/Google\ Chrome\ Master\ Preferences`.

### Windows Users 💩

1. Create entries with regedit (e.g. Software\Policies\Chromium\<Parameter> = <Value>).
2. That's all folks!

## Documentation Reference

- https://support.google.com/chrome/a/answer/187948?hl=en
- https://www.chromium.org/administrators/policy-list-3

## Default Configuration

| Policy Name                         | Description                                                   | Value                                    |
|-------------------------------------|---------------------------------------------------------------|------------------------------------------|
| **AllowCrossOriginAuthPrompt**          | Cross-origin HTTP Basic Auth prompts                          | `FALSE`                                    |
| **AllowOutdatedPlugins**                | Allow running plugins that are outdated                       | `FALSE`                                    |
| **ApplicationLocaleValue**              | Application locale                                            | `en`                                       |
| **AutoFillEnabled**                    | Enable AutoFill in forms                                      | `FALSE`                                    |
| **BackgroundModeEnabled**               | Continue running background apps when Google Chrome is closed | `FALSE`                                    |
| **BlockThirdPartyCookies**              | Block third party cookies                                     | `TRUE`                                     |
| **BookmarkBarEnabled**                  | Enable Bookmark Bar                                           | `TRUE`                                     |
| **ClearSiteDataOnExit**                 | Clear site data and cache on exit                             | `TRUE`                                     |
| **DefaultBrowserSettingEnabled**        | Set Google Chrome as Default Browser                          | `TRUE`                                     |
| **DefaultGeolocationSetting**           | Default geolocation setting                                   | `0 (disabled)`                             |
| **DefaultNotificationsSetting**         | Default notification setting                                  | `2 (do not allow)`                         |
| **DefaultPopupsSetting**                | Default popups setting                                        | `2 (do not allow)`                         |
| **DeveloperToolsDisabled**          | Disable Developer Tools                                       | `TRUE`                                     |
| **DisabledPlugins**                 | Specify a list of disabled plugins                            | `Chrome PDF Viewer, Java, Shockwave Flash` |
| **DisablePluginFinder**                 | Disable the plugin finder                                     | `TRUE`                                     |
| **DisableSafeBrowsingProceedAnyway**    | Disable proceeding from the Safe Browsing warning page        | `TRUE`                                     |
| **DnsPrefetchingEnabled**              | Enable DNS prefetching                                        | `FALSE`                                    |
| **ExtensionInstallBlacklist**           | Configure extension installation blacklist                    | `* (all)`                                  |
| **ExtensionInstallForcelist**           | Configure the list of force-installed apps and extensions     | `uBlock Origin, HTTPS Everywhere`          |
| **HomepageIsNewTabPage**                | Use New Tab Page as homepage                                  | `TRUE`                                     |
| **HomepageLocation**                    | Configure the home page URL                                   | `https://tracelabs.org/`                   |
| **ImportBookmarks**                     | Import bookmarks from default browser on first run            | `TRUE`                                     |
| **ImportHistory**                       | Import browsing history from default browser on first run     | `FALSE`                                    |
| **ImportHomepage**                      | Import of homepage from default browser on first run          | `FALSE`                                    |
| **ImportSavedPasswords**                | Import saved passwords from default browser on first run      | `FALSE`                                    |
| **ImportSearchEngine**                  | Import search engines from default browser on first run       | `FALSE`                                    |
| **MetricsReportingEnabled**             | Enable reporting of usage and crash-related data              | `FALSE`                                    |
| **PasswordManagerAllowShowPasswords**   | Allow to show passwords in password manager                   | `FALSE`                                    |
| **PasswordManagerEnabled**              | Enable saving passwords to the password manager               | `FALSE`                                    |
| **RemoteAccessClientFirewallTraversal** | Enable firewall traversal from remote client                  | `FALSE`                                    |
| **RemoteAccessHostFirewallTraversal**   | Enable firewall traversal from remote access host             | `FALSE`                                    |
| **RestoreOnStartup**                    | Action on startup                                             | `5`                                        |
| **SafeBrowsingEnabled**                 | Enable Safe Browsing                                          | `TRUE`                                     |
| **SavingBrowserHistoryDisabled**        | Disable saving browser history                                | `TRUE`                                     |
| **SearchSuggestEnabled**                | Enable search suggestions                                     | `TRUE`                                     |
| **ShowHomeButton**                      |  Show the Home button                                                             | `FALSE`                                    |
| **SyncDisabled**                        | Disable synchronization of data with Google                                                              | `TRUE`                                     |
| **TranslateEnabled**                    | Enable Translate Feature                                                              | `FALSE`                                    |

## Notes

- Feel free to add a default homepage (`homepage` config) in `master_preferences`.
- You can import a HTML bookmark file automatically using `import_bookmarks_from_file` in `master_preferences`.
