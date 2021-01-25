# Verify your documentation and build the pages

### Step 1: Ensure you have a `mkdocs.yml` file in place

This is a example [configuration](https://www.mkdocs.org/user-guide/configuration/):

```yml
# Project information
site_name: Your Project
site_url: https://[YOUR_GITHUB_ID].github.io/[your-repository-name]
site_author: Thomas Südbröcker

# Repository
repo_name: [YOUR-REPOSITORY-NAME]
repo_url: https://github.com/[YOUR_GITHUB_ID]/[YOUR-REPOSITORY-NAME]
edit_uri: edit/master/[YOU-DOCUMENTATION_FOLDER]
docs_dir: [YOU-DOCUMENTATION_FOLDER]

# Navigation
nav:
  - Welcome:
    - Overview: README.md   
  
## DO NOT CHANGE BELOW THIS LINE

# Copyright
# TBD

# Theme
theme:
  name: material
  font:
    text: IBM Plex Sans
    code: IBM Plex Mono
  icon:
    logo: material/library
  features:
    # - navigation.tabs
    - navigation.instant
    - navigation.expand
  palette:
    scheme: default
    primary: blue
    accent: blue

# Plugins
plugins:
  - search

# Customization
# TBD

# Extensions
markdown_extensions:
  - abbr
  - admonition
  - attr_list
  - def_list
  - footnotes
  - meta
  - toc:
      permalink: true
  - pymdownx.arithmatex:
      generic: true
  - pymdownx.betterem:
      smart_enable: all
  - pymdownx.caret
  - pymdownx.critic
  - pymdownx.details
  - pymdownx.emoji:
      emoji_index: !!python/name:materialx.emoji.twemoji
      emoji_generator: !!python/name:materialx.emoji.to_svg
  - pymdownx.highlight
  - pymdownx.inlinehilite
  - pymdownx.keys
  - pymdownx.mark
  - pymdownx.smartsymbols
  - pymdownx.snippets:
      check_paths: true
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
  - pymdownx.tabbed
  - pymdownx.tasklist:
      custom_checkbox: true
  - pymdownx.tilde
```

### Step 2: Preview your documentation locally

```sh
python3 -m mkdocs serve  
```

* Example output:

```sh
INFO    -  Cleaning site directory 
INFO    -  Documentation built in 0.57 seconds 
[I 210125 09:15:48 server:335] Serving on http://127.0.0.1:8000
INFO    -  Serving on http://127.0.0.1:8000
[I 210125 09:15:48 handlers:62] Start watching changes
INFO    -  Start watching changes
[I 210125 09:15:48 handlers:64] Start detecting changes
INFO    -  Start detecting changes
```

### Step 3: Build the pages in the folder "/site", which will be added to your GitHub project

```sh
python3 -m mkdocs build
```