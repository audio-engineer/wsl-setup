# WSL Setup

This shell script will install and set up the following libraries and software on your WSL system:

- `libssl-dev`
- `pkg-config`
- `Ninja`
- `Clang 17`
- `Clang-Format 17`
- `Clang-Tidy 17`
- `LLDB 17`
- `CMake 3.26.4`
- `keychain`
- `Z shell`
- `Oh My Zsh`
- `zsh-autosuggestions`
- `zsh-completions`
- `zsh-syntax-highlighting`
- `GNU Debugger`

Furthermore, it will:

- Upgrade `git` to the latest version
- Create an SSH key pair for usage with GitHub and display the public key to the user at the end of the script
    - Add the SSH key to `keychain` so that its password doesn't have to be entered every time it's used
- Configure `git` `user.name`, `user.email` and default branch
- Lock the `CMake` version, making it impossible to accidentally upgrade it
- Make `Z shell` the default shell

## Usage

### Prerequisites

- `wget`

### Installation

After logging into WSL, run the following command:

```shell
sh <(wget -qO - https://raw.githubusercontent.com/audio-engineer/wsl-setup/main/installer)
```

The script will generate an `error.log` file in the directory where it's run.
You can remove it after running the installer by running `rm error.log`.
