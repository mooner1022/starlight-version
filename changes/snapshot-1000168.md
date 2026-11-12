## 1.1.0-261112 (1000168)
+ docs(agent): point the system prompt at Store, Chat.waitFor and Schedule
+ feat(api): add Schedule, which runs code daily, by cron or once, with an alarm to wake the device
+ feat(api): add Chat.waitFor, which gives the next message to the waiting script instead of the event functions
+ feat(PluginCore): warn when a project's code holds a worker longer than its slow run setting
+ fix(api): tell from Api.isCompiling whether a project is compiling
+ feat(api): add Store, which keeps a project's values in JSON files across compiles and restarts
