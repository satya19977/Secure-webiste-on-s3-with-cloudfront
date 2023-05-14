# Overview

Users can securely access my website www.myprojectssatya.click to see a simple react application in action. They do so by going through any browser, which goes to Route53 which directs them to an edge location where a SSL/TLS certificate  is attached and the origin is the s3 bucket.

#### Architecture Diagram

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/4b598b89-617c-4fa3-842f-a14d417b916b)

# Setup

Create two  S3 buckets(www.myprojectssatya.click, myprojectssatya.click). The reason we create another bucket is to direct all users pointing to the main bucket that starts with www.

# S3
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/d905e5ec-5c54-4902-b18d-bb18ed743141)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/3797aed1-d324-476d-842c-0c85f6407bb3)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/95465cdc-9dc4-4d49-b236-d226570b506c)


# Creation of ACM
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/968162ac-7ccb-4373-855a-b8c0e6c4f446)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/720a89ba-0de4-4ec5-a9e8-dc67c0f260ce)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/2d8b80c4-6836-4e90-9de3-4e8029e6f601)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/ce2dc227-58e2-4ead-a87f-4522863b8f60)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/ab2f89bb-4692-4523-bc5c-e6f40f87bf29)



# CloudFront Distribution
Use Cloudfront to cache your bucket in edge locations for low latency access.
CloudFront
Do this for both the domain names.
1)Click Create a Cloudfront distribution
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/e7684f1b-8b44-410a-917c-88f59f656d33)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/7945b426-8c66-4af2-b154-2e4a4cb654ad)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/e16a0823-c024-43fb-9d0d-162864d86863)

3) Select redirect http to https
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/8c4f88bc-d073-4e98-b88c-eb7cc494cd15)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/23230943-96f3-48ac-aa4c-db21d2216839)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/5265d2e1-6b8e-4ace-b6b0-e56dc03b3a17)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/f836e15a-0541-4795-bb45-cb1ec1861138)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/937f408b-c407-4225-ab86-b803492da7cf)


# Route 53
Go to route 53 and create two alias to point to cloudfront distribution location.
1)Select create record to point to cloudfront distribution of respective domain names.
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/f8d3c790-dc35-481f-832e-37af6d62a1ef)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/7c20c069-69d7-4c63-89ae-e032d4d0deb4)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/ab9a6892-8b49-4498-a1ec-ae22548152ef)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/4fe0e336-2a58-4fb3-881a-a626b5c71801)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/2810638d-6a7e-4134-a467-02089c51d6c6)





4) Click www.myprojectssatya.click and myprojectssatya.click to check if you have secure connection.


This is the final result.

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/58158788-fdd1-4735-b593-34027bed9c58)







