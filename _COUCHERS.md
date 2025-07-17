Set up [the upstream chatwoot repo as an upstream](https://github.com/chatwoot/chatwoot) (i.e. a git `remote` called `upstream`), then

```sh
git fetch upstream
git rebase v4.4.0
git push -f
```

Wait for the build to complete on Github, and find the latest container in <https://github.com/Couchers-org/chatwoot/pkgs/container/chatwoot>, update that on [the `tools` repo docker-compose](https://github.com/Couchers-org/tools/blob/f2dca3e3c95b48945dbabba6e6432e85376d42ce/docker-compose.yml#L81) (note there are two lines), and then update as in those docs with

```sh
docker exec -it tools-chatwoot-1 bundle exec rails db:chatwoot_prepare
```
