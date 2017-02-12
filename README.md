# Software Release

script created to automate release management process

## Installation

script compiled from `srelease.bish` to bash script

to install clone `bin/srelease` to `/usr/local/bin/srelease`

## Usage

```ruby
Software Release
    script created to automate release management process


    prepare: initialize `releases/` folder with files

             srelease prepare


    task:    - fork to branch `feature/<task>-<postfix>`
             - create task file at `releases/current/<task>`

             srelease task task-11
                 => forks `feature/task-11`, creates `releases/current/task-11`
             srelease task task-11 create_readme
                 => forks `feature/task-11-create_readme`, creates `releases/current/task-11`


    start:   - fork to branch `release/<today's date>-<postfix>`
             - summarize `releases/current/*` files to `releases/history/<branch name>`

             srelease start              => forks and creates `releases/history/2017-02-05`
             srelease start backend_team => forks and creates `releases/history/2017-02-05-backend_team`


    clean:   remove all files from `releases/current/` except `.keep`

             srelease clean
```
