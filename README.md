# uv-conda-like (for fish)

- [uv-conda-like (for fish)](#uv-conda-like-for-fish)
	- [1. Install](#1-install)
	- [2. Usage](#2-usage)
		- [2.1. Create a new virtual environment](#21-create-a-new-virtual-environment)
		- [2.2. List all virtual environments](#22-list-all-virtual-environments)
		- [2.3. Activate a virtual environment](#23-activate-a-virtual-environment)
		- [2.4. Delete a virtual environment](#24-delete-a-virtual-environment)

## 1. Install

First, install uv.

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Then, clone this repository.

```bash
git clone https://github.com/zeroDtree/uv-conda-like.git
cd uv-conda-like
```

(Optional) Moddify `auv.fish` to set the directory of the uv virtual environment. Default is `$HOME/.uv/venvs`.

```bash
set UV_ENV_PATH "$HOME/project/.uv/venvs"
```

Add `auv.fish` to your fish config

```bash
echo "source $(pwd)/auv.fish" >> ~/.config/fish/config.fish
```

Restart your shell or source the config file.

```bash
source ~/.config/fish/config.fish
```

## 2. Usage

### 2.1. Create a new virtual environment

The options of `uv create` are the same as the `uv venv` command.

```bash
uv create {venv_name} [options]
```

For example, create a new virtual environment with python 3.11.

```bash
uv create venv_name --python=3.11
```

### 2.2. List all virtual environments

```bash
uv list
```

### 2.3. Activate a virtual environment

```bash
uv activate venv_name
```

### 2.4. Delete a virtual environment

```bash
uv delete venv_name
```
