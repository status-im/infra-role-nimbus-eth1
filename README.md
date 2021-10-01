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
TODO
```
