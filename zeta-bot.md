

# ZETA - automation helper


### Possible commands 

- **login**  oauth login with Google

- **plugin** list installed plugins or search
	- search 
	- install 
	- list 

- **web**  start a local server on http://localhost:7777 with UI options


### Plugins ideas

Inspired in Krew, plugin index is a central repo with a yaml/json file pointing to different plugins

- **etc-host** handle content of etc/host files with ease
	- list 
	- set/unset

- **alias** create ZETA shortcuts to specific plugins on an executable path
	- list
	- set/unset

- **onboarding** (IGZ specific) a helper to 


### Features
- Install Go binaries or node programs as plugins. 
- Has a config file to store global preferences `$HOME/.zeta/config`
- Export variables to underlying plugins
	- ZETA_VERSION
	- ZETA_CONFIG
	- ZETA_PLUGIN

### Mini SDK
- Expose helper functions to run interactive questionaries both CLI and web
- Expose helper functions to save plugin preferences
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNDE0OTU4OTRdfQ==
-->