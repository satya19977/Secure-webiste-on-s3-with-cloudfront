# Overview

Users can securely access my website www.myprojectssatya.click to see a simple react application in action. They do so by going through any browser, which goes to Route53 which directs them to an edge location where a SSL/TLS certificate  is attached and the origin is the s3 bucket.

#### Architecture Diagram

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/4b598b89-617c-4fa3-842f-a14d417b916b)

# Setup

Create two  S3 buckets(www.myprojectssatya.click, myprojectssatya.click). The reason we create another bucket is to direct all users pointing to the main bucket that starts with www.

# S3

1) Click create bucket and  store all the relevant files in the bucket

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/14aa3ba0-479d-4538-a37a-031b86957853)

2) Turn off block public access settings and add custom policy.

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/343e6ae5-4b39-4db2-82eb-537aceb10af1)

3) Turn on static website hosting and click save.

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/455dfd18-3653-4b3f-8cc6-7990f0c703a5)

4) Create second bucket myprojectssatya.click and enable static website hosting and click the option that says redirect requests for an  object, policy is http.

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/cecf0ca4-3834-469c-b2e3-9a5f6fdeba69)

## Create an SSL/TLS certificate in Certificate Manager(ACM)

1) Click request a certificate

