# Single-line Version Control System

> **Warning**
> 
> This project is in early development and not available now.

A simple versioning tool that only have one branch.

Maybe useful in file syncing and auto CI/CD :)

> **Warning**
> 
> **If you want to find some version control tool, please never use SVC, it lacks the core ability
of managing a project.**

## Usage

### `svc checkout`

Checkout to specified version.

### `svc commit`

Save current workspace status.

### `svc log`

Show complete logs for changes.

### `svc clone`

Clone a repository from remote.

### `svc push`

Push changes to remote.

### `svc pull [<version>]`

Update changes from remote.

### `svc set-remote <url>`

set up the remote url for local repository.

SVC only support ONE remote repository, and does not plan to support multiple remote repository
in the future.

## Solving conflicts

SVC doesn't support merging or other tree or flow based operations, all versions are snapshots. 
So if somebody pushed a version that you don't have, this version will be just hold in remote,
when you're pushing a new version, this missing version will be record as an old version.
only if you want to see this version that made by another people and try to `checkout` it in shell,
SVC will notify you that you should `svc pull <version>` first, and then the version will be
downloaded from remote to your local.
