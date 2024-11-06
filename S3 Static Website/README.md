# Hosting a Static Website on AWS S3
Welcome to this quick guide on hosting a static website using AWS S3 (Simple Storage Service). This README summarizes the key steps from the [full article](https://medon.hashnode.dev/how-to-host-your-website-on-amazon-s3-a-step-by-step-guide), authored by Ahmed Salau.
## Introduction
If you're looking to host a static website on a budget, AWS S3 provides a simple, fast, and cost-efficient solution. With S3, you only pay for the storage you actually use, and you can take advantage of the AWS Free Tier, which offers up to 5GB of storage free for the first year.
## Step-by-Step Guide
Follow these steps to host your static website on AWS S3:

1. Create an S3 Bucket
  - Go to the Amazon S3 Console.
  - Click on Create bucket.
  - Provide a unique name for the bucket (the name must be globally unique across all AWS accounts).
  - Choose a region (select the one closest to your users for better performance).
  - Click Create (you can leave the rest of the options as default for now).
2. Upload Your Website Files
After creating the bucket, click on it to open.
Click on the Upload button.
Drag and drop your static website files (HTML, CSS, JavaScript, images, etc.) into the S3 console, or click to select files manually.
Click Upload to upload the files to S3.
3. Enable Static Website Hosting
Inside your bucket, go to the Properties tab.
Scroll down to the Static website hosting section and click Edit.
Select Enable.
Enter the name of your index document (usually index.html).
Optionally, specify an error document (usually error.html).
Click Save changes.
4. Set Bucket Permissions (Make the Website Public)
Go to the Permissions tab of your S3 bucket.

Click on Bucket Policy and add the following policy to allow public access to your website:
