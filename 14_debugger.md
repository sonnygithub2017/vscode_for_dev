* vscode debugger:
  - open file in editor to debug (like `main.py`)
  - set breakpoints: click in glyph edge next to the line number
  - debug side bar: click active bar: `run and debug` to open it
    - variables:
      - locals and
      - globals
    - watch: watch variables and expressions
    - call stack: show all functions and modules in the call stack
    - breakpoints: show breakpoints
  - integrated terminal: show output in terminal
  - debug console: enter python commands and evaluate expressions, like `print(x)` or use gdb commands, like `bt` or `info locals`


* run debugger and debug actions:
  - trigger debugger: like "python debugger: debug python file" in top right corner
  - debug action:
    - continue: run until next breakpoint
    - step over: run next line
    - step into: run into function
    - step out: run until function returns
    - restart: restart the debugger
    - stop: stop the debugger

* breakpoints:
  - glyph edge next to the line number in editor
    - set breakpoints: click on the glyph edge next to the line number
    - remove breakpoints: click on the breakpoint in the editor
  - breakpoints section of the debug side bar -- helpful for long file
    - check breakpoints: check if breakpoints are enabled
    - disable/enable breakpoint: just for this session
    - toggle all active breakpoints: disable/enable all breakpoints
    - remove all breakpoints: remove all breakpoints
  - uncaught exceptions breakpoint: breakpoint for uncaught exceptions, like `ZeroDivisionError`
    - enabled by default, in breakpoints section of debug side bar

* inspect variables at breakpoint:
  - hover over variable in editor
    - show value of variable
    - show type of variable
    - show value of expression
    - show value of function call
  - variables section of debug side bar
    - locals: local variables in the current function
    - globals: global variables in the current module
    - show value of function call
  - debug console: enter python commands and evaluate expressions
    - use `print()` to print values

* watch variables and expression:
  - watch section of debug side bar
    - click on `+` icon to add watch expression
    - enter variable or expression to evaluate
      - example: `x`
      - example: `x < 5`
    - every time the debugger stops, the value of the expression will be updated
  - use `print()` to print values in the debug console

* other breakpoints:
  - function breakpoints: set breakpoints for specific functions
    - breakpoints section in debug side bar, click on `+` icon
    - enter function name
    - every time the function is called, the debugger will stop
  - conditional breakpoints:
    - set breakpoint in glyph edge of editor
    - right click on the breakpoint and select `Edit Breakpoint` > Expression
    - enter expression to evaluate
      - example: `x == 2`
    - if condition is true, debugger will stop, you can then inspect variables, do more debugging
  - hit-count breakpoints:
    - good for loops or functions that are called multiple times. it will stop at the breakpoint only when the hit count is reached
    - set breakpoint in a loop or function in glyph edge of editor
    - right click on the breakpoint and select `Edit Breakpoint` > Hit Count
    - enter hit count to stop at
      - example: `3`
    - every time the breakpoint is hit, the hit count will be incremented
    - when the hit count is reached, the debugger will stop

* log point: log messages to the console, but do not stop
  - set breakpoint in glyph edge of editor
  - right click on the breakpoint and select `Edit Breakpoint` > log message
  - enter message to log
    - use `{}` to insert variable values
    - example: `x = {x}`
  - every time the breakpoint is hit, the message will be logged to the "debug console" (not the terminal)

* call stack:
  - call stack section of debug side bar
    - show current function and module
    - show all functions and modules in the call stack
    - click on a function or module to jump to it in the editor
