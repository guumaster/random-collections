

# ZETA - automation helper


### Features
- Allows to run Go binaries or node programs as plugins. 
- If Go is detected, can run programs from source (maybe with `mage` ?) 
- Has a config file to store global preferences `$HOME/.zeta/config`
- Export variables to underlying plugins
- Has a simple SDK for plugin developments
	
	
### Env Vars
ZETA_CONFIG=path to config folder
ZETA_PLUGINS=path to plugin binaries
ZETA_ALIAS=path to aliases config

### Possible commands 

- **login**  oauth login with Google

- **plugin** list installed plugins or search
	- search 
	- install 
	- list 

- **web**  start a local server on http://localhost:7777 with UI options
- **config** command to setup all zeta variables
- **help** show all available commands and aliases


### Plugins ideas

Inspired in Krew, plugin index is a central repo with a yaml/json file pointing to different plugins

- **etc-host** handle content of etc/host files with ease
	- list 
	- set/unset

- **alias** create ZETA shortcuts to specific plugins on an executable path
	- list
	- set/unset

- **onboarding** (IGZ specific) help with introduction of new employee
	- web-draft: open a web editor to write your Markdown presentation
	- send PR
	- update PR

- **programs** (IGZ specific) help with program tasks
	- upload video
	- notify  send slack messages about coming talks and videos uploaded
	
	
### Mini SDK
- Expose helper functions to run interactive questionaries both CLI and web
- Expose helper functions to save plugin preferences
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3Mzc3MTA0MzgsLTEwNDM1NTAyOTYsLT
EwMzI4ODYzNjVdfQ==
-->