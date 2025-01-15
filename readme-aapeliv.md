Building a CE image:

```sh
rm -rf enterprise
rm -rf spec/enterprise

# put `ENV CW_EDITION="ce"` at the end of `docker/Dockerfile`

docker build -f docker/Dockerfile -t aapeliv/chatwoot:tweaked-v3.16.0-ce .
```
