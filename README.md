# Cloud-Resume-Challenge
The Cloud Resume Challenge by Forrest Brazeal.
I first heard of this project from community members in our discord server and found it quite interesting. 
Some areas are completely new to me like HTML, Javascript & CSS, so I've had to put in some hours doing crash courses on all. (Codecademy & W3schools are excellent resources)
I will write a post upon completion of this whole journey.


This project has 16 steps in total all listed below.
1. Your resume needs to have the AWS Cloud Practitioner certification on it.
2. Your resume needs to be written in HTML. Not a Word doc, not a PDF.
3. Your resume needs to be styled with CSS. It doesn’t have to be fancy. But we need to see something other than raw HTML when we open the webpage.
4. Your HTML resume should be deployed online as an Amazon S3 static website. 
5. The S3 website URL should use HTTPS for security. You will need to use Amazon CloudFront to help with this.
6. Point a custom DNS domain name to the CloudFront distribution, so your resume can be accessed at something like my-c00l-resume-website.com.  
7. Your resume webpage should include a visitor counter that displays how many people have accessed the site.
8. The visitor counter will need to retrieve and update its count in a database somewhere. I suggest you use Amazon’s DynamoDB for this. 
9. Do not communicate directly with DynamoDB from your Javascript code. Instead, you will need to create an API that accepts requests from your web app and communicates with the database.
10. You will need to write a bit of code in the Lambda function; you could use more Javascript, but it would be better for our purposes to explore Python – a common language used in back-end programs and scripts – and its boto3 library for AWS. 
11. You should also include some tests for your Python code.
12. You should not be configuring your API resources – the DynamoDB table, the API Gateway, the Lambda function – manually, by clicking around in the AWS console. Instead, define them in an AWS Serverless Application Model (SAM) template and deploy them using the AWS SAM CLI.
13. You do not want to be updating either your back-end API or your front-end website by making calls from your laptop, though. You want them to update automatically whenever you make a change to the code. (This is called continuous integration and deployment, or CI/CD.) Create a GitHub repository for your backend code.
14. Set up GitHub Actions such that when you push an update to your Serverless Application Model template or Python code, your Python tests get run. If the tests pass, the SAM application should get packaged and deployed to AWS.
15. Create a second GitHub repository for your website code. Create GitHub Actions such that when you push new website code, the S3 bucket automatically gets updated. (You may need to invalidate your CloudFront cache in the code as well.) Important note: DO NOT commit AWS credentials to source control! Bad hats will find them and use them against you!
16. Finally, in the text of your resume, you should link a short blog post describing some things you learned while working on this project. Dev.to is a great place to publish if you don’t have your own blog.
