# Docs

For runnable code examples, see: https://github.com/adviserlabs/demos

## Getting Started

Download the Adviser CLI, sign up, and start running jobs in the cloud - your first $100 of compute is on us!

* [MacOS AMD](https://adviser-public-bucket.s3.us-east-2.amazonaws.com/adviser-darwin-amd64), [MacOS ARM](https://adviser-public-bucket.s3.us-east-2.amazonaws.com/adviser-darwin-arm64)
* [Linux AMD](https://adviser-public-bucket.s3.us-east-2.amazonaws.com/adviser-linux-amd64), [Linux ARM](https://adviser-public-bucket.s3.us-east-2.amazonaws.com/adviser-linux-arm64)
* [Windows AMD](https://adviser-public-bucket.s3.us-east-2.amazonaws.com/adviser-windows-amd64.exe), [Windows ARM](https://adviser-public-bucket.s3.us-east-2.amazonaws.com/adviser-windows-arm64.exe)

```
$ mv YOUR_DOWNLOADED_BINARY adviser
$ chmod +x adviser
$ adviser signup
$ adviser run your_simulation.py
```

## Basic Usage

### Writing Output

Your cloud environment comes with a directory called `adviser_output`. Any files you put there can be fetched with `adviser job download`.
```
$ adviser run "your_simulation.py > adviser_output/results.txt"
$ adviser job download <job-id>
$ cat adviser_output/<job-id>/results.txt
```

## Next Steps

* [Start a Development Cluster](Start%20a%20Development%20Cluster.md)
* [Cloud Buckets](Cloud%20Buckets.md)
* [Multi-Node Jobs](Multi-Node%20Jobs.md)
