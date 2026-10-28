## 0.3.4b-261028 (100076)
+ ci: publish a signed snapshot build to Releases and starlight-version on nightly pushes
+ feat(PluginInstaller): record where each plugin was installed from and show it in the plugin info
+ feat(PluginStore): download, verify and install plugins from the store
+ feat(PluginStore): read release files from absolute Release URLs in the index
+ chore(PluginStore): remove the unused bubble drawable
+ fix(StoreHomeFragment): cancel pending fades so a quick reload doesn't hide the content
+ feat(PluginStore): load the store index from the starlight-plugins repository
+ feat(StoreSheet): keep the sheet buttons fixed while the content scrolls
+ fix(SlideBottomSheetDialog): draw the dim on the sheet scrim so it doesn't flicker
+ feat(SlideBottomSheetDialog): add a bottom sheet that slides in and out without fading
+ feat(PluginStore): style the store bottom sheets like the store screens
+ fix(PluginStore): even out the category chip padding
+ feat(PluginStore): add a plugin store mockup with sample data
+ chore(JSRhino): improve language name consistency
+ feat(MainActivity): check for updates once on app start
+ refactor(update): move update checking, download and install into AppUpdater
+ fix(PluginListItem): keep the row height when the switch appears on expand
+ feat(settings): merge permissions into general and projects with plugins
+ feat(settings): remove easy mode and add permission status and log settings
+ chore(DevModeActivity): remove leftover moved and commented-out entries
