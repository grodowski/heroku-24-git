Try out getting `rugged` and `git` to work on `heroku-24` stack.

Steps

- set buildpack to apt

```
heroku buildpacks:add --index 1 heroku-community/apt
```

- workaround https://github.com/heroku/heroku-buildpack-apt/issues/137, so that all git commands are in `PATH`

```
 heroku config:set GIT_EXEC_PATH=/app/.apt/usr/lib/git-core
 ```

