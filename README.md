# Hunter zsh theme

Many thanks to [Bogdan Mihaila](https://github.com/bmihaila) for his work on the theme [dustmod](https://github.com/bmihaila/dustmod).  
I made some optical changes.

Features are:
- [Solarized](https://github.com/altercation/solarized) color-scheme inspired theme with info and command prompt split on 2 lines to allow for enough space for both
- clock/time on the right
- the usual: username, host, current directory in prompt
- different color and prompt for `root` user
- show a little `✗` in front of the current path if it is not writable by the user
- show if on `ssh` connection
- `git` status if inside a repo: shows the branch-name and repository status in a verbose description or using only symbols (✓✶✗↝✩⇡⇣↱⤱)
- python virtual environment name in prompt
- show return code of last command if it was not `0`. additionally translates the return code to a human readable error message
- duration of last command for long running commands, i.e. > 20 seconds


## Screenshots
![Showing features](https://raw.githubusercontent.com/se-jaeger/hunter-zsh-scheme/master/screenshots/hunter_screenshot.png)

With [this](https://github.com/se-jaeger/my-zsh#2-setup-iterm2) configuration the screenshots were taken.


## Requirements
- Zsh - see [zsh.org](http://www.zsh.org/)
- a Zsh framework like [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
- git lib for zsh - provided by above frameworks
- needs [Python](https://www.python.org/) installed to translate the return error codes


## Installation
Download the theme file to the right directory for you framework and add the following line to your `.zshrc` file depending on your zsh plugin manager:

- [oh-my-zsh - adding themes howto](https://github.com/robbyrussell/oh-my-zsh/wiki/Customization#overriding-and-adding-themes)

    `ZSH_THEME="hunter"`


## Tweaks and settings

The appearance can be modified by setting environment variables in your `.zhrc`:

- `HUNTER_COMMAND_TRACK_MIN_TIME_SECS=20` - after how many seconds consider a "long running command" and display its runtime after it finished
- `HUNTER_GIT_STATUS_LONG_DESCRIPTION="true"` - show the git status verbose, e.g. `✶modified` or only using the symbols `✶`
- `HUNTER_USER_HOST_ALWAYS="true"` - show the `username@hostname` part always or hide it when on the local machine
- `HUNTER_PYTHON_ENV_PROMPT_ENABLED` - set to `false` to deactivate environment printing
- Use `conda config --set changeps1 False` to prevent conda from changing PS1.


For further changes, modify the code!
