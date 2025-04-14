* keyboard shortcuts:
  - undo: `cmd + z`,
  - save: `cmd + s`
  - copy: `cmd + c`, paste: `cmd + v`
  - cut: `cmd + x`,
  - select all: `cmd + a`
  - find: `cmd + f`

  - rename all identifier in file:
    select that word, then `cmd + shift + L`, then type new word
  - rename part of identifier in file:
    select that part, then `cmd + d`, then type new word

  - toggle comment: `cmd + /`

  - jump to file: `cmd + p`
  - jump to line: `ctrl + g`
  - move line up/down: `opt + up/down`
  - select line: `cmd + L`

  - show/customize keyboard shortcuts: manage > keyboard shortcuts

* editor group and different vscode windows:
  - once multiple files are opened, they will be opened in the same editor group
  - move file to new editor group: drag and drop the file tab to the right or left of the current editor group
  - move file to new window: drag and drop the file tab outside of the current window

* workspace:
  - central hub for all files and folders
  - 2 types of workspace:
    - single folder workspace: open a single folder
    - multi-root workspace: open multiple folders (can be in different locations)
  - multi-root workspace:
    - create: `File` > `Add Folder to Workspace...`
    - save workspace: `File` > `Save Workspace As...`
    - open saved workspace: `File` > `Open Workspace from file...`
    - the content of the workspace is saved in a `.code-workspace` file:
      ```
      $ cat computer_study.code-workspace
        {
                "folders": [
                        {
                                "path": "./git_github"
                        },
                        {
                                "path": "./vscode_for_dev"
                        }
                ],
                "settings": {}
        }
      ```
    - workspace settings:
      - `File` > `Preferences` > `Settings` > `Workspace`
      - the workspace settings are saved in the `.code-workspace` file
    - folder settings:
      - `File` > `Preferences` > `Settings` > `Folder`
      - the folder settings are saved in the `.vscode` folder in the folder (like ./git_github/.vscode/settings.json)

* sticky scroll
  - show the first line of scope while scrolling the nested scope
  - settings > search for `sticky scroll`
  - enable: `Editor > Sticky Scroll: Enabled`
  - max sticky line count: default is 5