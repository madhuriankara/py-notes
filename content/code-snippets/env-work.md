---
title: Env-Work
date: 2024-11-28
author: Your Name
cell_count: 7
score: 5
---

```python
import os
```


```python
import json
```


```python
# Convert environment variables to a dictionary
env_vars = dict(os.environ)
```


```python
# Convert dictionary to JSON string
env_vars_json = json.dumps(env_vars, indent=4)
```


```python
# Print or save the JSON string
print(env_vars_json)
# Optionally, you can write it to a file
with open("env_vars.json", "w") as f:
    f.write(env_vars_json)

```

    {
        "TERM_SESSION_ID": "w0t11p0:730CFA34-89B1-4DCB-A032-5C447F2FFA8F",
        "SSH_AUTH_SOCK": "/private/tmp/com.apple.launchd.fkke2I3hcY/Listeners",
        "LC_TERMINAL_VERSION": "3.5.8",
        "COLORFGBG": "15;0",
        "ITERM_PROFILE": "Default",
        "SQLITE_EXEMPT_PATH_FROM_VNODE_GUARDS": "/Users/madhuriankaraboyina/Library/WebKit/Databases",
        "XPC_FLAGS": "0x0",
        "LANG": "en_CA.UTF-8",
        "PWD": "/Users/madhuriankaraboyina/tact/madhuri_space/pynotes",
        "SHELL": "/bin/zsh",
        "__CFBundleIdentifier": "com.googlecode.iterm2",
        "TERM_FEATURES": "T3LrMSc7UUw9Ts3BFGsSyHNoSxF",
        "TERM_PROGRAM_VERSION": "3.5.8",
        "TERM_PROGRAM": "iTerm.app",
        "PATH": "/Users/madhuriankaraboyina/.gem/ruby/3.3.5/bin:/Users/madhuriankaraboyina/.rubies/ruby-3.3.5/lib/ruby/gems/3.3.0/bin:/Users/madhuriankaraboyina/.rubies/ruby-3.3.5/bin:/opt/homebrew/Caskroom/miniconda/base/envs/py312/bin:/opt/homebrew/Caskroom/miniconda/base/condabin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/Applications/iTerm.app/Contents/Resources/utilities",
        "LC_TERMINAL": "iTerm2",
        "COLORTERM": "truecolor",
        "COMMAND_MODE": "unix2003",
        "TERM": "xterm-color",
        "TERMINFO_DIRS": "/Applications/iTerm.app/Contents/Resources/terminfo:/usr/share/terminfo",
        "HOME": "/Users/madhuriankaraboyina",
        "TMPDIR": "/var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/",
        "USER": "madhuriankaraboyina",
        "XPC_SERVICE_NAME": "0",
        "LOGNAME": "madhuriankaraboyina",
        "__CF_USER_TEXT_ENCODING": "0x0:0:0",
        "ITERM_SESSION_ID": "w0t11p0:730CFA34-89B1-4DCB-A032-5C447F2FFA8F",
        "SHLVL": "1",
        "OLDPWD": "/Users/madhuriankaraboyina/tact/madhuri_space",
        "HOMEBREW_PREFIX": "/opt/homebrew",
        "HOMEBREW_CELLAR": "/opt/homebrew/Cellar",
        "HOMEBREW_REPOSITORY": "/opt/homebrew",
        "INFOPATH": "/opt/homebrew/share/info:",
        "P9K_TTY": "old",
        "_P9K_TTY": "/dev/ttys015",
        "ZSH": "/Users/madhuriankaraboyina/.oh-my-zsh",
        "PAGER": "cat",
        "LESS": "-R",
        "LSCOLORS": "Gxfxcxdxbxegedabagacad",
        "LS_COLORS": "di=1;36:ln=35:so=32:pi=33:ex=31:bd=34;46:cd=34;43:su=30;41:sg=30;46:tw=30;42:ow=30;43",
        "P9K_SSH": "0",
        "_P9K_SSH_TTY": "/dev/ttys015",
        "CONDA_EXE": "/opt/homebrew/Caskroom/miniconda/base/bin/conda",
        "_CE_M": "",
        "_CE_CONDA": "",
        "CONDA_PYTHON_EXE": "/opt/homebrew/Caskroom/miniconda/base/bin/python",
        "CONDA_SHLVL": "2",
        "CONDA_PREFIX": "/opt/homebrew/Caskroom/miniconda/base/envs/py312",
        "CONDA_DEFAULT_ENV": "py312",
        "CONDA_PROMPT_MODIFIER": "(py312) ",
        "RUBY_ROOT": "/Users/madhuriankaraboyina/.rubies/ruby-3.3.5",
        "RUBYOPT": "",
        "RUBY_ENGINE": "ruby",
        "RUBY_VERSION": "3.3.5",
        "GEM_ROOT": "/Users/madhuriankaraboyina/.rubies/ruby-3.3.5/lib/ruby/gems/3.3.0",
        "GEM_HOME": "/Users/madhuriankaraboyina/.gem/ruby/3.3.5",
        "GEM_PATH": "/Users/madhuriankaraboyina/.gem/ruby/3.3.5:/Users/madhuriankaraboyina/.rubies/ruby-3.3.5/lib/ruby/gems/3.3.0",
        "CONDA_PREFIX_1": "/opt/homebrew/Caskroom/miniconda/base",
        "_": "/opt/homebrew/Caskroom/miniconda/base/envs/py312/bin/jupyter",
        "JPY_SESSION_NAME": "/Users/madhuriankaraboyina/tact/madhuri_space/pynotes/notebooks/code-snippets/Untitled.ipynb",
        "JPY_PARENT_PID": "68562",
        "PYDEVD_USE_FRAME_EVAL": "NO",
        "CLICOLOR": "1",
        "FORCE_COLOR": "1",
        "CLICOLOR_FORCE": "1",
        "GIT_PAGER": "cat",
        "MPLBACKEND": "module://matplotlib_inline.backend_inline"
    }



```python

```


```python

```


---
**Score: 5**
