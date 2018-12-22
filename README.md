# tenableio2securityhub
A python script for sending vulnerabilities from Tenable.io to AWS SecurityHub.

### Installation
```
pip install boto3 requests
```

### Python Version
3.7+

### Configuration

Now run the script as per the example below, passing in the following 4 environment variables:

* AWS_ACCOUNT_ID (available [here](https://docs.aws.amazon.com/IAM/latest/UserGuide/console_account-alias.html#FindingYourAWSId))
* AWS_REGION (available [here](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html))
* TENABLE_ACCESS_KEY (available [here](https://cloud.tenable.com/api#/authorization))
* TENABLE_SECRET_KEY (available [here](https://cloud.tenable.com/api#/authorization))

Example:

```
AWS_ACCOUNT_ID=123456789012 AWS_REGION=eu-west-1 TENABLE_ACCESS_KEY=123456 TENABLE_SECRET_KEY=abcdef python3 ./tenableio2securityhub.py
```

When the command completes, you will see vulnerabilities from Tenable.io appear in your SecurityHub findings.
