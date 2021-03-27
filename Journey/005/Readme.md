

# Enabling CloudTrail 

## Introduction
AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting. In addition, you can use CloudTrail to detect unusual activity in your AWS accounts. These capabilities help simplify operational analysis and troubleshooting.


## Cloud Research
* Event History is where cloudTrail by default logs event data for the past 90days
* Create trail if you need to track beyond 90days
* Turn on Log validation to make sure logs are not tampered with
* CloudTrail logs can be streamed to CloudWatch logs (paid service)
* Trail can be applied to all regions and Organizations
* To log data operations for S3 and Lambda, use Data Events. It is disabled by default (Paid service)
* Query/Analyse trail logs in S3 using Athena
* Ensure CloudTrail trail logging buckets are not publicly accessible.


## Try yourself

* Search for Cloud Trail in the search box
* Go to Trails > Create trail
* ![cT](https://user-images.githubusercontent.com/22412589/110852757-aa692200-82aa-11eb-9ef2-6777b6d20554.PNG)
* I didnt create KMS key because it is a charged service
* ![ct2](https://user-images.githubusercontent.com/22412589/110852758-ab01b880-82aa-11eb-9fd9-8d735864da46.PNG)
* ![ct2](https://user-images.githubusercontent.com/22412589/110856380-7b08e400-82af-11eb-9422-14bdbde42e09.PNG)
* ![cT](https://user-images.githubusercontent.com/22412589/110856385-7ba17a80-82af-11eb-8477-771d43c72015.PNG)
* ![ct3](https://user-images.githubusercontent.com/22412589/110856383-7ba17a80-82af-11eb-8366-9d8765a4e0ae.PNG)
* Delete Trail
* ![cT](https://user-images.githubusercontent.com/22412589/110857993-747b6c00-82b1-11eb-8743-59d6a32e0981.PNG)







