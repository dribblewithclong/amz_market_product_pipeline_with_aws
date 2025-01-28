# amz_market_product_pipeline_with_aws

## leverage utils functions (optional for local dev)

1. navigate to project folder

    $ ```cd amz_market_product_pipeline_with_aws```

2. clone utils from github repo

    $ ```git submodule add git@github.com:dribblewithclong/iykyk_python_utils.git iykyk_python_utils```

## techstack

- AWS Lambda: call api to fetch and store the raw data
- Amazon S3: backend for data storage (bronze/silver/gold)
- AWS Glue:
    - ETL for extract raw data from bronze/silver layer, transform then load to silver/gold layer
    - orchestrate/schedule the data pipeline
    - data catalog for lakehouse architecture (apache iceberg)
- Amazon Redshift: data replication from the gold layer for dashboard visualization
