# cloud-resume-challenge

A serverless resume website with view counter and CI/CD (Github) using AWS, inspired from the [Forrest Brazeal's ](https://aws.amazon.com/developer/community/heroes/forrest-brazeal/) [cloud resume challenge](https://cloudresumechallenge.dev/instructions/)


## Architecture


![image of diagram](https://github.com/kenYW/cloud-resume-challenge/blob/main/cloud-resume-challenge/cloud_resume_challenge.png)


## Service

* Serverless Application model (SAM) - as Infrastructure as Code
* CloudFront - to secure visitor cannot access s3 directly
* Github - version control and make it CI/CD 
* Lambda - to build visitor count by fetching functions
* S3 - host static website
* Golang - for lambda code




## Try & Error

* Bucket name (S3) must be as same as domain name
* (CloudFront) Orgin domain name must use s3 endpoint without "https:// "
* (ACM) mannual create as ACM only support in "us-east-1" region, may use nested clofrmation for IaC
* (IaC) always make change only in template not directly in service.
* (Cost) aware the endpoint charge, to see bill information.



## Reference

Thanks to the awesome tutorial from [Open up the Cloud](https://www.youtube.com/channel/UCAklaE5D59xWtip-3Jwa7xA)


