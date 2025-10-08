# Start a Development Cluster

Adviser clusters are always-on, pre-configured instances that are shared across an organization and can quickly run jobs without waiting for provisioning.

## Usage

With the following command, Adviser will help you choose an appropriate cloud (i.e. AWS), region (i.e. us-west-2), instance type (i.e. t2.medium), workdir (i.e. `$PWD`), and setup command (i.e. `pip install -r requirements.txt`).

```
adviser cluster create
```
