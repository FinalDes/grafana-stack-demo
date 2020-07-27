## grafana-stack-demo

You need to install the plugin on each Docker host with container from which you want to collect logs.

You can install the plugin from our Docker hub repository by running on the Docker host the following command:

``` loki install
docker plugin install  grafana/loki-docker-driver:latest --alias loki --grant-all-permissions
```

To check the status of installed plugins, use the docker plugin ls command. Plugins that start successfully are listed as enabled in the output:

``` plugin output
docker plugin ls
ID                  NAME         DESCRIPTION           ENABLED
ac720b8fcfdb        loki         Loki Logging Driver   true
```

## docker compose config list
loki_swarm_only.yml tested on single node swarm

loki-demo.yml simple docker-compose setup to check how loki work