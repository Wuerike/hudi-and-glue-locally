# Apache Hudi and AWS Glue locally

This repo provides a demo of the [Apache Hudi](https://hudi.apache.org/) you can execute locally within the [AWS Glue](https://aws.amazon.com/pt/glue/) docker image.

## Running

```
docker compose up
```

## Docker Compose Details

### AWS Glue

It's the AWS Glue + Spark environment, you can use it by opening the jupyter lab at http://localhost:8888/lab/, the `hudi_evaluation` sample notebook contains basic CRUD operations on Apache Hudi table.

Refer to this [AWS blog post](https://aws.amazon.com/pt/blogs/big-data/develop-and-test-aws-glue-version-3-0-jobs-locally-using-a-docker-container/)
 to check more details about it.

### Minio

Object storage compatible with Amazon S3, you can acces the Minio UI at http://localhost:9000, it will require an user and a password, both are set to `minioadmin`

### AWS CLI

CLI to apply s3 commands, it's used to create a bucket called `warehouse` and move the sample data from `data/transactions.json` to `warehouse/raw`.
