* VScode setting: central control for all settings
  - VScode setting: user settings, workspace settings, folder settings
  - open: manage > settings
* setting fields:
  - search box: search for settings
  - filter: filter settings by category
    - modified: show modified settings. to reset a setting, click the gear icon next to the setting and select "Reset Setting"
    - extension ID: show settings for different extensions, like  @ext:github.copilot-chat
    - feature: show settings for different features, like @feature:debug
    - language: show settings for different languages, like @lang:python, @lang:markdown
* setting categories:
  - User settings: global settings for all workspaces
  - Workspace settings: settings for the current workspace
  - Folder settings: settings for the current folder
* User settings:
  - commonly used: commonly used settings
  - Text editor: editor settings
    - Files: auto save: onFocusChange (save on focus change)
    - Tab Size: tab size settings: 2 spaces
    - Font: font size: 14
    - Cursor: cursor style: block
    - Word Wrap: word wrap settings: on (wrap lines)
  - workbench: workbench settings
    - like enable preview: enable preview for markdown files
  - Features:
    - terminal
      - "terminal.integrated.suggest.enabled": true,
  - extensions: extension settings
    - Code Spell Checker: spell checker settings
    - Github Copilot: copilot settings
* open settings json:
  - open: manage > settings > "open settings (json)" icon
  - add or modify settings in the json file
  - example:
    ```json
    {
      "editor.fontSize": 14,
      "editor.tabSize": 2,
      "editor.wordWrap": "on",
      "workbench.editor.enablePreview": true,
      "terminal.integrated.suggest.enabled": true
    }
    ```