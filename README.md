# aws-emr-lambda
Playbook to run AWS EMR (e.g. PySpark) via AWS Lambda and boto3

This stackoverflow article is pretty good representative example:
https://stackoverflow.com/questions/36706512/how-do-you-automate-pyspark-jobs-on-emr-using-boto3-or-otherwise

* AWS Lambda function written in Python
* Uses boto3 library to manage AWS resources
* Uses boto3 "EMR" client
* Uses `.run_job_flow()` method
* The example is interesting because it appears that the Spark configuration is handled inside the bootstrap script
* Other possible places to set the Spark configuration
    - Lambda emr.run_job_flow()
    - PySpark application itself (i.e. Python file)
    - Spark submit at command line

See also example of how to supply Spark properties configuration at execution runtime:
https://spark.apache.org/docs/latest/configuration.html#spark-properties
