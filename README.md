# Software Release

script created to automate release management process

## Installation

script compiled from `srelease.bish` to bash script

to install clone `bin/srelease` to `/usr/local/bin/srelease`

## Usage

```ruby
    prepare: initialize `releases/` folder with files

             srelease prepare


    current: create task file at `releases/current/<task>`

             srelease current task-11   => creates `releases/current/task-11`


    init:    - fork to branch `release/<today's date>-<postfix>`
             - summarize `releases/current/*` files to `releases/history/<branch name>`

             srelease init              => forks and creates `releases/history/2017-02-05`
             srelease init backend_team => forks and creates `releases/history/2017-02-05-backend_team`


    clean:   remove all files from `releases/current/` except `.keep`

             srelease clean
```
