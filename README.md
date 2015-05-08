# ansible-zookeeper

An Ansible role for installing [Apache Zookeeper](http://zookeeper.apache.org).

## Role Variables

- `zookeeper_version` - Zookeeper version.
- `zookeeper_cloudera_distribution` - Cloudera distribution version (default: `cdh5.4`)
- `zookeeper_conf_dir` - Configuration directory for Zookeeper (default: `/etc/zookeeper/conf`)
- `zookeeper_data_dir` - Data directory for Zookeeper (default: `/var/lib/zookeeper`)
- `zookeeper_max_client_connections` - Maximum number of client connections (default: `50`)
- `zookeeper_tick_time` - Tick time (default: `2000`)
- `zookeeper_initial_limit` - Initial synchronization tick limit (default: `100`)
- `zookeeper_sync_limit` - Synchronization limit for acknowledgement (default: `5`)
- `zookeeper_client_port` - Port Zookeeper binds to. (default: `2181`)
- `zookeeper_myid` - Zookeeper `myid` (default: `0`)
- `zookeeper_servers` - Members of the Zookeeper cluster. Defaults to:

```yaml
- { index: "0", ip: "127.0.0.1", ports: "2888:3888" }
```

## Example Playbook

See the [examples](./examples/) directory.
