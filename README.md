# Description

This role provisions a [nimbus-eth1](https://github.com/status-im/nimbus-eth1) installation that is ETH1 client.

# Ports

The service exposes five ports by default:

* `30303` - DevP2P peering port. Must __ALWAYS__ be public.
* `8545` - JSON RPC port. Must __NEVER__ be public.
* `8546` - WebSocket port. Must __NEVER__ be public.
* `8547` - GraphQL port. Must __NEVER__ be public.
* `9093` - Prometheus metrics port. Should not be public.

# Installation

Add to your `requirements.yml` file:
```yaml
- name: infra-role-nimbus-eth1
  src: git+git@github.com:status-im/infra-role-nimbus-eth1.git
  scm: git
```

# Configuration

The crucial settings are:
```yaml
# branch which should be built
nimbus_eth1_repo_branch: 'stable'
# ethereum network to connect to
nimbus_eth1_network: 'mainnet'
# increase maximum number of peers
nimbus_eth1_max_peers: 160
# optional setting for debug mode
nimbus_eth1_log_level: 'DEBUG'
# optional improvement for connectivity
nimbus_eth1_public_address: '12.34.56.78'
```
