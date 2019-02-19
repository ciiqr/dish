# dish
Dish allows you to run arbitrary docker run commands on multiple (ephemeral) servers at once.

## Dependencies
* `bash`
* `docker`
* `docker-machine`

## Examples
* single command: `DISH_GOOGLE_PROJECT=gcp-project dish busybox wget -O- 'http://example.com/'`
* shell script: `DISH_GOOGLE_PROJECT=gcp-project DISH_STDIN=true dish -i busybox /bin/sh -c 'cat | sh -s --' < some-script.sh`
