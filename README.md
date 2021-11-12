## Serverless Address Validation with Amazon Location Service

This repository contains a SAM tempalte and code for deploying a Serverless Address Validation pipeline using S3, Lambda, and Amazon Location Service.

## Highlevel Architecture
<img width="891" alt="Architecture" src="https://user-images.githubusercontent.com/73195085/141511303-9475720d-778d-4fd6-9305-3c2acdf00484.png">

  1.	The Scatter Lambda function takes a data set from the S3 bucket labeled input and breaks it into equal sized shards. 
  2.	The Process Lambda function takes each shard from the pre-processed bucket and performs Address Validation in parallel calling the Amazon Location Service     Places API 
  3.	The Gather Lambda function takes each shard from the post-processed bucket and appends them into a complete dataset with additional address information.
![image](https://user-images.githubusercontent.com/73195085/141511996-1d643a1f-d9f5-4ba7-b590-08090bfb85af.png)


## Deployment Steps


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

