# nyu-lab-agile-zenhub
This is the repository for the ZenHub training lab on Agile Development and Planning

[![ZenHub logo](https://dxssrr2j0sq4w.cloudfront.net/3.2.0/img/external/zenhub-badge.png)](https://app.zenhub.com/workspaces/lab-agile-zenhub-602c7d2ecd8ba2001cb5ed89/board)

Import/Export Tool
https://github.com/gavinr/github-csv-tools


## Export/Import Issues
Import and export GitHub issues via CSV (https://github.com/gavinr/github-csv-tools)

Prerequisite:  [Install Node.js](https://nodejs.org/en/).

On a Mac you can use [homebrew](http://brew.sh) to do install Node cleanly if you don't already have it:

```bash
brew install node
```

Then run this to install GitHub CSV Tools:

```sh
npm install -g github-csv-tools
```

After install, githubCsvTools --help for info on how to use, or see below.

Instructions for exporting or importing:

### To Export Issues

This will export all stories to a file called timestamp-issues.csv

```sh
githubCsvTools -t <token> -o <org> -r <repo>
```

```sh
githubCsvTools -t $GIT_TOKEN -o $GIT_ORG -r $GIT_REPO
```

### To Import Issues

Currently imports title, body, labels, status (closed or open) and milestones.

```sh
githubCsvTools new-issues.csv -t $GIT_TOKEN -o rofrano -r lab-agile-zenhub
```
