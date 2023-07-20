# SRE tote-bag

SRE tote is a tote bag of simple ansible playbooks for automation!

It uses lightweight ansible-playbook approach to execute pre-defined scenarios.

Shared functionality to run shell commands, update environment variables and generate reports.

## About

- Self documenting.
- Re-usable.
- Embraces UNIX philosophy i.e. simple, compact, clear, modular, and extensible.
- Plays nice with the current tools and SOPs.
- Generates markdown and rich-text reports.
- Supports parallel execution (when running inside container).

## Playbooks

### Hello world

```shell
ansible-playbook hello_world.yml
```

### Cluster Context

```shell
ansible-playbook cluster_context.yml -e CLUSTER=<CLUSTER_NAME|CLUSTER_ID|CLUSTER_UUID>
```

### Cluster Create

```shell
ansible-playbook cluster_create.yml -e CLUSTER_NAME=<CLUSTER_NAME>
```

Default parameters:

- CHANNEL_GROUP (stable, fast, *candidate*)
- PROVIDER (*aws*, gcp)
- VERSION (*4.12.0-rc.8-candidate*)
- REGION (*eu-north-1*)
- OCM_ENVIRONMENT (*staging*, production, integration)
