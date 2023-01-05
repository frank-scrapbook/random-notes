# Python Installation

## macOS
1. Install pyenv (via homebrew)
    ```
    brew install pyenv
    ```

2. Check latest known python release for specific version, aka 3.11
    ```
    ~ pyenv latest -k 3.11
    ```

    Command Line Usage + Output:
    ```
    ➜  ~ pyenv latest -k 3.11
    3.11.1
    ```

3. (Might be required - to be on the safe side) Setting up shell environment
    
    **bash**
    - `~/.bashrc`
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
        echo 'eval "$(pyenv init -)"' >> ~/.bashrc
        ```
    - `~/.profile`
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.profile
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.profile
        echo 'eval "$(pyenv init -)"' >> ~/.profile
        ```
    - `~/.bash_profile`
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
        echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
        ```
    - `~/.bash_login` (if it exists)
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_login
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_login
        echo 'eval "$(pyenv init -)"' >> ~/.bash_login
        ```
    
    **zsh**
    - `~/.zshrc`
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
        echo 'eval "$(pyenv init -)"' >> ~/.zshrc
        ```
    - `~/.zprofile`
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zprofile
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zprofile
        echo 'eval "$(pyenv init -)"' >> ~/.zprofile
        ```
    - `~/.zlogin` (if it exists)
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zlogin
        echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zlogin
        echo 'eval "$(pyenv init -)"' >> ~/.zlogin
        ```

4. (Might be required - to be on the safe side) Installing python build dependencies

    **Install Xcode Command Line Tools**
    ```
    xcode-select --install
    ```

    **Install Homebrew (if not already installed)**
    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

    **Install other python build environment dependencies**
    ```
    brew install openssl readline sqlite3 xz zlib tcl-tk
    ```

    **Restart Shell**
    ```
    exec "$SHELL"
    ```


6. Install python version (via pyenv)
    ```
    pyenv install 3.11:latest
    ```

    Command Line Usage + Output:
    ```
    ➜  ~ pyenv install 3.11:latest
    python-build: use openssl@1.1 from homebrew
    python-build: use readline from homebrew
    Downloading Python-3.11.1.tar.xz...
    -> https://www.python.org/ftp/python/3.11.1/Python-3.11.1.tar.xz
    Installing Python-3.11.1...
    python-build: use readline from homebrew
    python-build: use zlib from xcode sdk
    Installed Python-3.11.1 to /Users/frank.peng/.pyenv/versions/3.11.1
    ```

7. Check which python versions are installed and available
    ```
    pyenv versions
    ```

    Command Line Usage + Output:
    ```
    ➜  ~ pyenv versions
    * system (set by /Users/frank.peng/.pyenv/version)
    3.11.1
    ```

8. Set default python version
    ```
    pyenv global 3.11.1
    ```

    - `pyenv shell <version>`  - Set session-only for Current Shell Session
    - `pyenv local <version>`  - Set locally for Current Directory/Sub-Directories
    - `pyenv global <version>` - Set globally for Current User


## Points of Interest
- pyenv = python version management (similar to rbenv/rvm for ruby or nvm for node...etc.)
- pip = python package manager
- venv = virtual environment (isolated package installation environment)

## References
- [Python Docs on installation](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)
- OPTIONAL: [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)