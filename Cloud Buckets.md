# Cloud Buckets

Adviser supports the following services for mounting cloud storage to your job's working directory:

- Amazon S3
- Azure Cloud Storage

Use multiple `--store` flags to specify your Adviser Stores, or the URLs of the cloud storage bucket. Clusters can also be created with stores.

## Usage

```
adviser run ls my-adviser-store --store my-adviser-store
```

```
adviser run ls test --store s3://test
```

```
adviser run ls test --store https://<account>.blob.core.windows.net/test
```

```
adviser cluster create --store my-adviser-store
adviser run ls my-adviser-store --cluster <id>
```

## Adviser Store

Adviser can keep track of your cloud storage, and optionally can securely store any associated credentials.
* If no name is provided, a store will be created with the same name as the bucket or container.
* Use `--global` to mark a store as available to all of your organization's clusters and jobs.

```
adviser store create my-adviser-store \
  --url s3://<bucket> \
  --aws-access-key-id <access-key-id> \
  --aws-secret-access-key <secret-access-key>
```

```
adviser store create my-adviser-store \
  --url https://<account>.blob.core.windows.net/<container> \
  --azure-client-id <client-id> \
  --azure-client-secret <client-secret> \
  --azure-tenant-id <tenant-id>
```

```
adviser store create --url s3://<bucket> --global
```
