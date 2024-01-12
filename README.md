# Apache Hudi and AWS Glue locally

This repo provides a demo of the [Apache Hudi](https://hudi.apache.org/) you can execute locally within the [AWS Glue](https://aws.amazon.com/pt/glue/) docker image.

## Running

```
docker compose up
```

## Docker Compose Details

- glue: AWS Glue + Spark environment
- minio: Object storage compatible with Amazon S3
- aws: AWS CLI to create a Minio bucket

### AWS Glue

You can open the jupyter lab at http://localhost:8888/lab/ and use the sample notebook to CRUD a Hudi table.

Refer to this [AWS blog post](https://aws.amazon.com/pt/blogs/big-data/develop-and-test-aws-glue-version-3-0-jobs-locally-using-a-docker-container/)
 to check more details about it.

### Minio

You can acces the Minio UI at http://localhost:9000, it will require an user and a password, both are set to `minioadmin`

### AWS CLI

The AWS CLI will create a bucket called `warehouse` and move the sample data at `data/transactions.json` to `warehouse/raw`.
