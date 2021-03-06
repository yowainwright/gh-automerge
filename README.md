# GH-Automerge

[![CircleCI](https://circleci.com/gh/jonathanong/gh-automerge/tree/master.svg?style=svg&circle-token=d89466bafa3597afd2af10e1305ecac50a76958f)](https://circleci.com/gh/jonathanong/gh-automerge/tree/master)
[![NSP Status](https://nodesecurity.io/orgs/jonathanong/projects/90f33c5d-5d57-410c-9899-4e1e7b3a254a/badge)](https://nodesecurity.io/orgs/jonathanong/projects/90f33c5d-5d57-410c-9899-4e1e7b3a254a)
[![Greenkeeper badge](https://badges.greenkeeper.io/jonathanong/gh-automerge.svg)](https://greenkeeper.io/)

----

GH-Automerge is a cron bot. It is built node and can used by being installed with NPM. 

----

**GH-Automerge automatically:**

- Merges master into a pull request when it is out of date
- Merges a pull request when it is up-to-date and is not blocked by checks

## Usage

To enable automerge on a pull request, add a Github Label called `AUTOMERGE` to the pull request.

![gh-automerge](https://user-images.githubusercontent.com/1074042/36138017-9db600c4-104c-11e8-862a-4f43bed4a02a.jpg)

## Installation

GH-Automerge could run this where ever. However, it is typically run as a cron job within CircleCI.

**To install:**
1. Create a repository
1. Run `npm i --save-dev gh-automerge`

**Enabling GH-Automerge in CircleCI:**
1. Copy the [`.circleci/config.yml` template](.circleci/template.config.yml) into a repository
1. Enable CircleCI
1. Add `GITHUB_TOKEN` and `GITHUB_ORG` env vars to your CircleCI config
