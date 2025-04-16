* vscode profile:
  - a collection of settings, extensions, workspace preferences.
  - different profiles can be created for different projects or workspaces.
  - Check the current profile: `Manage` > `Profiles`
    - Default profile: the profile that is used when no other profile is selected
    - `Use for new windows`: the profile that is used when a new window is opened
    - `Contents`: can be opened in the editor, having:
      - `Settings`: settings for the profile
      - `Keyboard Shortcuts`: keybindings for the profile
      - `Tasks`: tasks for the profile
      - `Snippets`: snippets for the profile
      - `Extensions`: extensions for the profile
    - Folders & Workspaces: folders and workspaces for the profile

* create profile: `Manage` > `Profiles` > `New Profile`
    - Name: type the profile name
    - Icon: select the profile icon
    - Copy from: select the profile to copy from, like
      - `None`: create empty profile
      - `Default`: copy the default profile
      - `python`, `javascript`, `html`,
    - Content: select the content to copy from the profile, including `Settings`, `Keyboard Shortcuts`, `Tasks`, `Snippets`, `Extensions`:
      - Default: copy the default profile
      - None: do not copy any content
    - "Preview" or "Create"
* associate folders and workspaces with profile:
  - `Manage` > `Profiles` > `your profile`
  - `Folders & Workspaces` > `Add Folder or Workspace`
    - select the folder or workspace to associate with the profile

* switch, rename and delete profile:
  - switch profile: `Manage` > `Profiles`
    - select the profile to switch to
  - rename profile: `Manage` > `Profiles`
    - select the profile to rename
    - type the new name
  - delete profile: `Manage` > `Profiles`
    - select the profile to delete (can't be the default profile)

* customize contents of profile
  - switch to the profile, and make it active
  - add or remove settings, extensions, tasks, snippets, keyboard shortcuts
  - add or remove folders and workspaces

* export and import profile:
  - export profile as local file or github gist:
    - `Manage` > `Profiles` > `your profile`
    - select the profile to export,
    - select as local file or github gist
    - if local file:
      - select the location to save the file, like myprofile.code-profile
    - if github gist:
      - need to login to github account
      - it will create a gist with the profile contents: like https://gist.github.com/sonnygithub2017/8839a00c2ff15755b701f9f43909806a
  - import profile: `Manage` > `Profiles` > `New Profile` >  `Import Profile`
    - if github gist:
      - paste the gist URL: like https://gist.github.com/sonnygithub2017/8839a00c2ff15755b701f9f43909806a
      - create
    - if local file:
      - click `select file ...` button
      - select your profile file
      - click create button

* open vscode with profile from command line:
  - cd to your folder, `code . --profile <profile_name>`
    - example: `code . --profile python`
  - open vscode with profile and folder: `code <folder_path> --profile <profile_name> `
    - example: `code ~/myproject --profile python `
  - open vscode with profile and workspace: `code  <workspace_path> --profile <profile_name>`
    - example: `code ~/myproject/myproject.code-workspace --profile python`

* create profile from template
  - `Manage` > `Profiles` > `New Profile`
  - select the template to create from:
    - `Doc write`: create a profile for writing documents
    - `python`: create a profile for python development
  - "Preview" or "Create"