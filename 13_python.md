* python installation
  - python3.x installation to OS
  - extension installation in vscode (which include intellisense, python linting, debugging, etc)
* add python to path in macOS
  - get path of python: `which python3`
  - add `export PATH="/path/to/python:$PATH"` in `~/.bash_profile` (for old Mac ) or `~/.zshrc` (for new Mac)
  - run `source ~/.bash_profile` or `source ~/.zshrc`
* select python interpreter in vscode
  - open python file in vscode editor, the python interpreter version will be shown in the status bar
  - if not, `shift + command + p` to open command palette, and type `python: select interpreter`
* change indention to 2 spaces
  - this is NOT standard for python indentation (which is 4 spaces), so set it by using `ruff`
  - add pyproject.toml file in the root directory of the project
      ```
      [tool.ruff]
      line-length = 80  # Limit lines to 80 characters
      indent-width = 2   # (Ruff does not support this directly, VS Code handles it)
      lint.select = ["E", "W", "F"]  # Enforce style and formatting rules
      lint.fixable = ["ALL"]  # Allow Ruff to automatically fix issues
      ```
* python lint:
  - used to check the code style and formatting
  - extensions:  `ruff` (for linting and formatting) or `pylint` (for linting)
  - warning shown:
    - in the editor (yellow squiggly line)
    - status bar > `Problems` tab in bottom panel
* run python in integrated terminal
  - The python will be run with the selected python interpreter selected in the status bar
  - open integrated terminal and run `python filename.py`
  - or click `Run Python File in Terminal` button in the top right corner

* virtual environment
  - isolate projects and prevent package conflict
  - create
    - from terminal: `python3 -m venv venv`
      - venv folder will be created in the current directory, it will contain:
        - `bin` folder will contain the python interpreter and the packages installed in it
        - `include` folder will contain the header files for the python interpreter
        - `lib` folder will contain the python packages installed in it
        - `pyvenv.cfg` file will contain the configuration of the virtual env
    - from vscode UI:
      - open command palette `shift + command + p` and type `Python: Create Environment`
        - select: Venv Creates a `.venv` ventual environment in current workspace
        - select folder in workspace (for multi-root workspace) to create the venv folder
        - select the interpreter version
      - .venv folder will be created in the selected folder
  - activate virtual env: `source venv/bin/activate`
    - the terminal prompt will change to show that the virtual env is activated
  - install packages in virtual env: `pip install package_name`
  - check installed packages in virtual env: `pip freeze`
  - deactivate virtual env: `deactivate`
  - remove virtual env: `rm -rf venv`