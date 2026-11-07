## 1.0.1-261107 (1000141)
+ revert(neonjs): drop the main thread's wait limit for a script's context and the fallbacks it needed
+ fix(agent): give create_project starting code for the message event of each API level
+ fix(PluginCore): keep the starting code of a language that overrides only the older formatDefaultCode
+ fix(PluginCore): give the compile permit back when cancelled just as it is taken
+ fix(neonjs): bound the main thread's wait for a context only where its timeout is caught
+ fix(docs): reject malformed member keys, construct only StarLight's constant holders and tell a plugin's own packages
+ fix(agent): close calls an older version left open before resuming, and mark a call running only once it can start
+ fix(api): deliver runOnUiThread's outcome past a timed-out wait, let UIThread's interrupts stop the script and declare getScopeOf as any
+ fix(PluginCore): enable the listeners a plugin adds during onEnable
+ fix(PluginCore): run one compile of a project at a time, whoever starts it
+ fix(agent): name API2 listeners by every event a project receives and give create_project the app's default events
+ fix(docs): render undocumented varargs by element type and read test guides by portable paths
+ fix(api): split runOnUiThread's main-thread waits, guard wake locks and keep Env's helper out of its members
+ fix(agent): tell a call cut short by a stop from those that never ran or came from earlier turns
+ fix(agent): give create_project only its events and wait for a compile already running
+ fix(PluginCore): mark a plugin enabled after onEnable and keep disabling listeners past one that throws
+ docs(agent): put a misplaced KDoc back and note how alternate starter names meet custom code
+ fix(docs): look for unresolved types outside the KDoc text
+ fix(PluginCore): disable every listener of a plugin when it is unloaded
+ fix(agent): rebuild the script docs when plugins or API levels are registered again
+ fix(agent): keep two compiles of one project from both starting
+ refactor(agent): find a turn's results by the one rule CallResults keeps
+ fix(agent): tell the model nothing is known of calls found open only at a new message
+ fix(agent): close the open calls of a run imported while it went on
+ feat(agent): answer script questions from docs built from the code, not a copy of the site
+ docs(api): document in KDoc every API, type and event scripts reach
+ build(docs): collect the KDoc of what scripts reach with a KSP processor
+ fix(agent): give every event a create_project wildcard matches its starting code
+ fix(projects): name API2 starter listeners apart when StarLight's own function takes the name
+ fix(PluginCore): report a loaded plugin as enabled
+ fix(api): give both engines the same clear error when a script assigns to Env
+ fix(api2): keep an error in runOnUiThread's onComplete from stopping the app
+ fix(legacy): fail clearly when Bridge.getScopeOf names a project that isn't compiled
+ fix(api): post notifications only through build, which says what is missing
+ fix(legacy): release the shared wake lock only while it is held
+ docs(api2): note the lock-order hang Broadcast.send can cause between NeonJS projects
+ fix(neonjs): bound how long the main thread waits for a script's context
+ fix(legacy): stop Api.UIThread from deadlocking NeonJS projects
+ build(deps): update NeonJS to 0.1.7
+ fix(agent): give compile_project a time limit, set in the project settings
+ fix(agent): close tool calls left without a result so the conversation keeps working
