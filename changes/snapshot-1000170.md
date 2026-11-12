## 1.1.0-261112 (1000170)
+ fix(debugroom): alert a log once when the room is shown over the editor
+ docs(agent): point the system prompt at Format, Schedule.at and onUncaughtError
+ fix(listener): let the listener's thread see that the app has started, so rooms are restored
+ fix(api): refuse NaN and invalid dates as times, and pass over curly quotes in Format.josa
+ feat(neonjs): tell onUncaughtError which async event function rejected, with its arguments
+ feat(api): call a script's onUncaughtError with the errors nothing caught
+ feat(api): add Schedule.at, which keeps a task across compiles and restarts
+ feat(listener): restore the rooms of the notifications still shown when StarLight starts
+ feat(api): add Format, which writes numbers, dates, durations and Korean particles
