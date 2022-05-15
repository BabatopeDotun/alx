Website name: http://my-alx-bucket.s3-website-us-west-2.amazonaws.com/

Cloudfront name: https://dkd4lv4uqfl5s.cloudfront.net/

Create S3 Bucket
 An AWS S3 bucket was created on the AWS portal by typing "S3" in the search box 
Clicked the bucket and then created one by naming it "my-alx-bucket"

3. Upload files to S3 Bucket: I uploaded the files using the "add files feature"

4. Secure Bucket via IAM: I made the access to the website public and added the below config
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AddPerm",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-alx-bucket/*"
        }
    ]
}

6. Configure S3 Bucket: I added the index.html

7. Distribute Website via CloudFront

