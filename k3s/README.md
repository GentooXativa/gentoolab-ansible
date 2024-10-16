# K3S Setup overview

- [K3S Setup overview](#k3s-setup-overview)
  - [Resume](#resume)
  - [Diagram](#diagram)

## Resume

This playbooks will setup a HA k3s cluster using etcd with at least 3 `master` nodes and 0 to N `agent` nodes. External access is done using an external node ( a cheap VPS ) that is connected using WireGuard to the `master` nodes.

All the `master` nodes are running a `ucarp` instance to provide a virtual IP that is used to access the k3s cluster and provide HA. The virtual IP can be configured at inventory file using the `k3s_ha_virtual_ip` variable using CIDR format `<address>/<netmask>`.

## Diagram

> To be added
