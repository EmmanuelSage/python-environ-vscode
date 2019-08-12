# python-environ-vscode
This is a readme.md description of how to setup your python environment in visual studio code 

# **TODO : CLEAN UP THIS README**

# steps

install pip to check

`$ pip --version`

if its not there use eas_install on a mac to install it

`$ sudo easy_install pip`

`$ pip install virtualenv`

`$ which python`

============

`$ pip3 install virtualenv` : To install

`$ python3 -m virtualenv env` : install a virtualenv called env in path
or
`$ python3 -m venv env` : install a virtualenv called env in path **faster **ecomended
or
`$ virtualenv -p python3 env` : install a virtualenv called env in path

`$ source env/bin/activate` : activate env

`$ deactivate` : deactivate env

`$ which python` : show environment path

========================================


- Download vscode

- install Python extension

- cmd shift p : then >color or >file icon to select themes or download as you like: i changed file icon to ayu

- > default settings change these after getting the json of your changed settings
- workbench.settings.editor: ui to json
- workbench.settings.openDefaultSettings: false to true
- workbench.settings.useSplitJSON: false to true

hence:

```json
Switch settings to json format and add this

{
    "workbench.settings.editor": "json",
    "workbench.settings.openDefaultSettings": true,
    "workbench.settings.useSplitJSON": true
}

```

- This would give you the json view

- change python.pythonPath to the `$ which python3` path so it uses it by default

# create virtualenv

- ctr ~ to open terminal
- `$ python3 -m venv env`
- now set the virtual environment from the settings.json file
- virtual env would be set for all instances of our environment

# Formatting code

- shift option F : this formats the code, it would use autopep\* or useBlack
- ctr space brings settings as you type into the json in the user settings
- you could also use sort imports from the command pallette

# linting pylint
- command pallete : linting
- install pylint

# install Code Runner
- the green run runs the code in your terminal hence using the default env python
- to use the white (run code *inputs don't work with this as it is just results)you would have to change the path of the python as it uses python 3 which is the default
- ctr option N is also the shortcut to run

# debugging
- add configuration
- run debug

# unit testing
cmd shift p : > shell : add code to path:

- > python: Discover Tests
click to setup unitest framework allows you to run tests inline

- > zen : to toggle zen mode

- you could use this settings

- > keyboard shortcuts

```json
{
    "workbench.colorTheme": "Predawn",
    "workbench.iconTheme": "ayu",
    "editor.fontSize": 22,
    "editor.fontWeight": "500",
    "editor.fontFamily": "Source Code Pro",
    "debug.console.fontFamily": "Source Code Pro",
    "debug.console.fontSize": 22,
    "terminal.integrated.fontSize": 22,
    "terminal.integrated.fontWeight": "600",
    "window.zoomLevel": 2,
    "python.pythonPath": "/usr/local/bin/python3",
    "python.formatting.provider": "black",
    "editor.formatOnSave": true,
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": true,
    "code-runner.executorMap": {
        "python": "$pythonPath -u $fullFileName"
    },
    "code-runner.clearPreviousOutput": true,
    "code-runner.showExecutionMessage": false,
    "code-runner.ignoreSelection": true,
    "code-runner.saveFileBeforeRun": true,
    "[plaintext]": {
        "editor.quickSuggestions": false
    },
    "editor.quickSuggestionsDelay": 100,
    "zenMode.centerLayout": false,
    "zenMode.fullScreen": false,
    "zenMode.hideLineNumbers": false,
    "zenMode.hideTabs": false,
    "editor.minimap.enabled": false,
    "workbench.settings.openDefaultSettings": true,
    "workbench.settings.editor": "json",
    "workbench.statusBar.feedback.visible": false,
    "workbench.startupEditor": "newUntitledFile",
}
```
