# MANDY GITHUB ACTION :sparkles: :fire:

***A GitHub action to build your Mandy-powered project! :sparkles: :fire:***

## ABOUT :books:

This repository contains the source code for a GitHub Action for compiling Mandy-powered websites! To learn how to use this GitHub Action for your own Mandy project, read the section below! You can find the repository for the Mandy project [here](https://github.com/alyxshang/mandy).

## USAGE :hammer_and_pick:

To use this GitHub Action for your own Mandy-powered project, execute these steps.

- 1.) Go to your Mandy project's root directory and create a directory called `.github`.
- 2.) Inside this directory, create another directory called `workflows`.
- 3.) Inside `workflows` create a file called `main.yml`.
- 4.) Put the following into `main.yml`

```YML
on: [push]
name: Mandy Site Build CI
env:
  MANDY_ENV: production
name: Mandy CI
jobs:
  build_and_test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: alyxshang/mandy-github-action@v.0.2.0
      - name: "Build the Mandy site."
        run: mandy -c .
```

- 5.) This will build your Mandy-powered site into the directory you specified inside the `dist_dir` configuration option.
- 6.) You can also add a badge to your `README`, just like with other actions.
- 7.) Enjoy! :heart:

## NOTE :scroll:

- *Mandy Github Action :sparkles: :fire:* by *Alyx Shang :black_heart:*.
- Licensed under the [FSL v1](https://github.com/alyxshang/fair-software-license).
