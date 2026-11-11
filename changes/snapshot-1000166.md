## 1.1.0-261111 (1000166)
+ fix(app): say the new script and notification messages in Korean too
+ fix(PluginCore): tie an event's error to the version it ran in, not the one that was current when it was sent
+ fix(plugins): refresh a plugin's libraries and assets when it is updated and take out a plugin that fails to enable
+ fix(app): say where script errors are and why a bot stays silent, and find logs by part of a tag or message
+ fix(agent): ask for a file's hash to overwrite it, let a rewind be undone, add a stop button and ask before compiling a running bot
+ fix(editor): keep unsaved code through a rotation or a fold, and notice files changed outside the editor
+ fix(app): keep unsaved settings, rules and the new project wizard through a rotation or a theme change
+ fix(app): start over from the splash when a screen comes back before the runtime, and keep a failing plugin from ending the app
+ fix(projects): stop a project cleanly when its compile fails and end what a recompile left running
