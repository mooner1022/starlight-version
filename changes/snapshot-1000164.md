## 1.1.0-261111 (1000164)
+ fix(settings): refuse to save manual notification rules with no rule and apply the automatic switch on save
+ fix(diagnostics): don't ask for package rules while automatic rules are on
+ fix(app): show the crash report again when a blocked start is opened from the launcher
+ fix(debugroom): open the room when its saved chat can't be read and write the chat atomically
+ fix(agent): keep a conversation that can't be read from being overwritten by a new one
+ fix(agent): say that the chosen AI lost its connection instead of quietly using another
+ fix(scripts): take numeric strings as timer delays and keep a zero interval from spinning
+ fix(projects): import a project turned off instead of running it at once
+ fix(NotificationListener): stop dropping every message after the first from messengers without chat log ids
+ fix(PluginCore): keep a plugin's id or name from reaching folders outside the plugins directory
+ style(app): show every alert as one quiet card and tell its kind by the icon alone
+ build(deps): update PeekAlert to mooner1022/PeekAlert@56ecd79 and drop the workarounds it makes needless
