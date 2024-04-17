# appium-error
diiferent error and finding the soln

1.Errror 1:-User
Failed to create session. An unknown server-side error occurred while processing the command. Original error: Error executing adbExec. Original error: 'Command 'C:\\Users\\Admin\\AppData\\Local\\Android\\Sdk\\platform-tools\\adb.exe -P 5037 -s 8bc7c3ea shell 'settings delete global hidden_api_policy_pre_p_apps;settings delete global hidden_api_policy_p_apps;settings delete global hidden_api_policy'' exited with code 255'; Command output: Exception occurred while executing 'delete': java.lang.SecurityException: Permission denial, must have one of: [android.permission.WRITE_SECURE_SETTINGS] at com.android.providers.settings.SettingsProvider.enforceHasAtLeastOnePermission(SettingsProvider.java:2642) at com.android.providers.settings.SettingsProvider.mutateGlobalSetting(SettingsProvider.java:1605) at com.android.providers.settings.SettingsProvider.mutateGlobalSetting(SettingsProvider.java:1597) at com.android.providers.settings.SettingsProvider.deleteGlobalSetting(SettingsProvider.java:1568) at com.android.providers.settings.SettingsProvider.call(SettingsProvider.java:592) at android.content.ContentProvider.call(ContentProvider.java:2716) at android.content.ContentProvider$Transport.call(ContentProvider.java:641) at com.android.providers.settings.SettingsService$MyShellCommand.deleteForUser(SettingsService.java:411) at com.android.providers.settings.SettingsService$MyShellCommand.onCommand(SettingsService.jav
=============Soln=============================================================================================================================================
{
  "platformName": "Android",
  "appium:automationName": "UiAutomator2",
  "appium:deviceName": "d695bb5d",
  "appium:ignoreHiddenApiPolicyError": "true",
  "appium:noReset": "true"
}

you need to add  { "appium:ignoreHiddenApiPolicyError": "true",
  "appium:noReset": "true"
} to desired Capability
