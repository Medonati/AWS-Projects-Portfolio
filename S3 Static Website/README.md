# Hosting a Static Website on AWS S3
Welcome to this quick guide on hosting a static website using AWS S3 (Simple Storage Service). This README summarizes the key steps from the [full article](https://medon.hashnode.dev/how-to-host-your-website-on-amazon-s3-a-step-by-step-guide), authored by Ahmed Salau.
## Introduction
If you're looking to host a static website on a budget, AWS S3 provides a simple, fast, and cost-efficient solution. With S3, you only pay for the storage you actually use, and you can take advantage of the AWS Free Tier, which offers up to 5GB of storage free for the first year.
## Step-by-Step Guide
Follow these steps to host your static website on AWS S3:

1. **Create an S3 Bucket**
    - In the [AWS Management Console](https://console.aws.amazon.com/), type S3 in the search bar and select Amazon S3 from the list of services
    - Click on Create bucket.
    - Provide a unique name for the bucket (the name must be globally unique across all AWS accounts).
    - Choose a region (select the one closest to your users for better performance).
    - Click Create (you can leave the rest of the options as default for now).
      
2. **Upload Your Website Files**
    - After creating the bucket, click on it to open.
    - Click on the Upload button.
    - Drag and drop your static website files (HTML, CSS, JavaScript, images, etc.) into the S3 console, or click to select files manually.
    - Click Upload to upload the files to S3.
      
3. **Enable Static Website Hosting**
    - Inside your bucket, go to the Properties tab.
    - Scroll down to the Static website hosting section and click Edit.
    - Select Enable.
    - Enter the name of your index document (usually index.html).
    - Optionally, specify an error document (usually error.html).
    - Click Save changes.
      
4. **Set Bucket Permissions (Make the Website Public)**
    - Go to the Permissions tab of your S3 bucket.
    - Click on Bucket Policy and add the following policy to allow public access to your website:

              {
                "Version": "2012-10-17",
                "Statement": [
                  {
                    "Sid": "PublicReadGetObject",
                    "Effect": "Allow",
                    "Principal": "*",
                    "Action": "s3:GetObject",
                    "Resource": "arn:aws:s3:::your-bucket-name/*"
                  }
                ]
              }
    - Replace your-bucket-name with the name of your S3 bucket.
    - Click Save.

    - Additionally, ensure that public access settings are configured correctly:

        - Go to the Block public access section.
        - Make sure the settings allow for public access to the objects in your bucket.

5. **Access the Website**
Once static website hosting is enabled, AWS will provide you with an endpoint URL for your website. It will look something like: http://your-bucket-name.s3-website-us-east-1.amazonaws.com

    - You can now visit this URL to access your static website.

## 🎉 Conclusion
By following these steps, you can effortlessly host your static website on AWS S3, taking advantage of its ease of use, fast performance, and cost-efficiency. Enjoy the process of launching your website!

For a comprehensive guide and detailed instructions, please refer to the original article: [**How to Host Your Website on Amazon S3: A Step-by-Step Guide**](https://medon.hashnode.dev/how-to-host-your-website-on-amazon-s3-a-step-by-step-guide).


