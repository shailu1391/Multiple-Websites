# Multiple-Websites

## In this section we create 4 kinds of websites

1. Static website hosted on AWS s3 bucket
2. Serverless wesite using AWS Lambda
3. Static website on AS EC2 virtual machine
4. Static website using Paas AWS elastic beanstalk

## S3 Bucket Static Website

Steps:

1. Create a new project in AWS Cloud9
2. Use cloud shell to create a index.html page (touch index.html)
3. Open AWS S3 and create a bucket with open public access
4. Edit properties to enable Static Website hosting
5. Edit Permissions of S3 bukcet to modify bucket policy as below:

            {
                "Version": "2012-10-17",
                "Statement": [
                    {
                        "Sid": "PublicReadGetObject",
                        "Effect": "Allow",
                        "Principal": "*",
                        "Action": "s3:GetObject",
                        "Resource": "arn:aws:s3:::bucket4poopy/*"
                    }
                ]
            }
 
 6. Download the index.html file from Cloud9 project and upload it to the S3 bucket
 7. Check the Static website hosting section of the properties tab to find the website end point. Hosted as shown below:

![image](https://user-images.githubusercontent.com/76478051/153732476-59918c37-c7ff-4f0f-91a2-4fc3ab90412b.png)
