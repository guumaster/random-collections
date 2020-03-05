

# ZETA - automation helper


### Features
- Allows to run Go binaries or node programs as plugins. 
- If Go is detected, can run programs from source (maybe with `mage` ?) 
- Has a config file to store global preferences `$HOME/.zeta/config`
- Export variables to underlying plugins
- Has a simple SDK for plugin development
	
	
### Mini SDK
- Available for Go/Node/Python/Bash 
- Expose helper functions to run interactive questions both CLI and web
- Expose helper functions to save plugin preferences
- templating helper
- Git/gitlab/gihtub setup helper to handle tokens without env vars
	- functions to ad
- integrates with fzf  ?


### Possible commands 

- **login**  oauth login with Google
- **plugin** list installed plugins or search
	- search 
	- install 
	- list 
- **web**  start a local server on http://localhost:7777 with UI options
- **config** command to setup all zeta variables
	- config <plugin> allows to save preferences for plugins

- **help** show all available commands and aliases
	- help <plugin> show specific plugin help (use templating or simple string)



### Plugins ideas

Inspired in Krew, plugin index is a central repo with a yaml/json file pointing to different plugins

- **etc-host** handle content of etc/host files with ease
	- list 
	- set/unset

- **alias** create ZETA shortcuts to specific plugins on an executable path
	- list
	- set/unset

- **git-changelog** reads commits and make a markdown changelog list (maybe with a template)

- **onboarding** (IGZ specific) help with introduction of new employee
	- web-draft: open a web editor to write your Markdown presentation
	- send PR
	- update PR

- **programs** (IGZ specific) help with program tasks
	- upload video
	- notify  send slack messages about coming talks and videos uploaded
		
### Env Vars
ZETA_CONFIG=path to config folder
ZETA_PLUGINS=path to plugin binaries
ZETA_ALIAS=path to aliases config


	
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcxNjYxOTQ4MiwxNDEwMzY0OTcsLTEwND
M1NTAyOTYsLTEwMzI4ODYzNjVdfQ==
-->