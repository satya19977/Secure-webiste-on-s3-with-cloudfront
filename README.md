# Overview

Users can securely access my website www.myprojectssatya.click to see a simple react application in action. They do so by going through any browser, which goes to Route53 which directs them to an edge location where a SSL/TLS certificate  is attached and the origin is the s3 bucket.

#### Architecture Diagram

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/4b598b89-617c-4fa3-842f-a14d417b916b)

# Setup

Create two  S3 buckets(www.myprojectssatya.click, myprojectssatya.click). The reason we create another bucket is to direct all users pointing to the main bucket that starts with www.

# S3

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/38b99a71-2331-46ce-8536-6b96b47ec55f)


![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/906f2252-1a2b-43c1-8968-3b5bb3fe96dd)




![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/1d2582c4-b598-48ba-bd81-d9a7fa0dbe5c)
# Creation of ACM

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/bacbc27b-c9f9-4ee4-b330-2638ed6a125e)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/2e8676ca-ed18-422c-ba1c-c3a0d2f2937b)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/735f6708-e101-4cd9-bf22-9bbd4fef6b2f)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/7c149c18-e9cc-454d-bcb2-de9d7e5eaaaa)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/6ced871e-0ff4-4b44-b008-8b62560b4270)

# CloudFront Distribution
Use Cloudfront to cache your bucket in edge locations for low latency access.
CloudFront
Do this for both the domain names.
1)Click Create a Cloudfront distribution
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/85e54e97-4561-42f4-9ecb-ed0655e8e098)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/5728e3e3-404a-4523-a5a6-954c00a27951)
3) Select redirect http to https
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/82b03988-ac2b-4e8e-8464-e63772bb113a)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/fadb2fb8-5ca5-4be2-9f75-0d69477de934)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/5c7181eb-12fa-4ead-869c-866d7da5c23d)

# Route 53
Go to route 53 and create two alias to point to cloudfront distribution location.
1)Select create record to point to cloudfront distribution of respective domain names.

![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/2736888a-fad7-48a3-b2de-79b1ef2b0ddc)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/8d65d800-f4d6-40ca-ab0b-114edfbcb264)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/7955c58e-8c38-460e-8596-f7b17dd79fbc)
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/5a4f401b-3d69-4b26-9d8d-ef061ebbc881)

4) Click www.myprojectssatya.click and myprojectssatya.click to check if you have secure connection.
This is the final result.
![image](https://github.com/satya19977/Secure-webiste-on-s3-with-cloudfront/assets/108000447/04bbdd83-70f3-4118-aa0b-9bf38961a2bf)






