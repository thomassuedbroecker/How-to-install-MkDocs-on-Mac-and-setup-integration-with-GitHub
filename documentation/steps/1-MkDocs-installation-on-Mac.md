# MkDocs installation on Mac

### Step 1: Verify the [brew](https://brew.sh) installation

```sh
brew --version
```

### Step 2: Change the folder permission to install python, if needed

```sh
sudo chown -R $(whoami) /usr/local/lib/pkgconfig
chmod u+w /usr/local/lib/pkgconfig
```

### Step 3: Install [python3](https://www.python.org)

```sh
brew install python3
```

### Step 4: Upgrade pip

```sh
pip3 install --upgrade pip
```

### Step 5: Install [mkdocs](https://www.mkdocs.org)

```sh
pip3 install mkdocs
```

### Step 6: Install the [mkdocs-material-extensions](https://pypi.org/project/mkdocs-material-extensions/)

```sh
python3 -m pip install mkdocs-material-extensions
```
