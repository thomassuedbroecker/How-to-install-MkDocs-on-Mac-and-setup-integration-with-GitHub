# Integrate the documentation with [GitHub CI](https://docs.github.com/en/actions/guides/about-continuous-integration)

### Step 1: Add folder to `.gitignore`

```sh
echo "site/" >> .gitignore
```

### Step 2: Create a two folders in your project

```sh
mkdir .github
cd .github
mkdir workflows
```

### Step 3: Create a file called `ci.yml` and insert the CI configuration

```yml
name: ci
on:
  push:
    branches:
      - main
      - master
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-python@v2
        with:
          python-version: 3.x
      - run: pip install mkdocs-material
      - run: mkdocs gh-deploy --force
```

### Step 4: Create a [new branch in your GitHub](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-and-deleting-branches-within-your-repository) project called for example `gh-pages`

### Step 5: Enable the [GitHub pages](https://pages.github.com) on your project and select the branch `gh-pages` as source for your documentation
