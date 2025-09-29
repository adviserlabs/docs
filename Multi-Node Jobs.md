# Distributed Multi-Node Jobs

Adviser supports multi-node clusters and jobs. The `--num-nodes` flag specifies the number of nodes to scale the cluster or job to.

## Usage

```
adviser run python test.py --num-nodes 2
```

or

```
adviser cluster create --num-nodes 2
adviser run python test.py --cluster <id>
```

## Environment Variables

The following environment variables are available to any job:

| `ADVISER_NUM_NODES` | The number of nodes reserved for the job, which is the same as `--num-nodes`. |
| `ADVISER_NODE_RANK` | The number (0 to `$ADVISER_NUM_NODES - 1`) used to uniquely identify the current node in the job. |
| `ADVISER_NODE_IPS` | A newline-delimited list of N=`$ADVISER_NUM_NODES` IP addresses reserved for the job, ordered corresponding to the rank of each node. |
| `ADVISER_NUM_GPUS_PER_NODE` | The number of GPUs available to each node in the job. |
