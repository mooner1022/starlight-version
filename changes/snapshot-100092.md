## 1.0.0-261030 (100092)
+ build(app): change version to 1.0.0
+ fix(ConfigDSL): let info values use the free row width before truncating
+ fix(plugins): contain plugin API mismatches in settings and widgets
+ refactor(plugins): check plugin API compatibility through ApiCompatibility
+ build(PluginCore): version PluginCore 1.0.0 with the app
+ feat(PluginCore): accept plugins within a supported API range
+ chore(ConfigDSL): deprecate the unused button background color
+ refactor(WidgetSettings): use the choice option for widget settings
+ refactor(*): replace remaining snackbars with peeks
+ refactor(DebugRoomFragment): confirm clearing chats and show errors as peeks
+ refactor(DevModeActivity): show debug info as copyable info rows
+ refactor(AppInfoActivity): show versions as copyable info rows and use peeks
+ refactor(DialogUtils): hide the previous peek before showing a new one
+ refactor(PluginInfoActivity): show plugin details with info and text list rows
+ refactor(projectInfo): show values, live state and lists with info and text list rows
+ refactor(settings): show notification access and battery optimization as status rows
+ refactor(problemSolver): show states and package rule checks as status rows
+ refactor(CheckUpdateConfigActivity): run the update check as a button action
+ refactor(ProjectConfigActivity): use info, live and danger rows with peek notices
+ build(PluginCore): bump PLUGINCORE_VERSION to 0.3.3
+ feat(DevModeActivity): add ConfigDSL preview screen
+ feat(SheetDialogProvider): add card selection sheets and PeekAlert notices
+ feat(ConfigDSL): add choice and multi choice options
+ feat(ConfigDSL): add button styles, confirmation and suspend actions
+ feat(ConfigDSL): add info, progress and text list options
+ feat(ConfigDSL): add live bindings and value-based visibility
+ fix(ConfigDSL): combine flags in flagOf and hide dev-mode-only categories
