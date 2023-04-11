# Deploy a Website using Github Action on AWS S3 Bucket.

## Description: 

As part of a my-web project, I design and implemented a Github action workflow script to deploy my-web site on AWS S3 Bucket.

## Introduction:

Deploying a website to a production environment can be a complex and time-consuming process. However, with the right tools and techniques, it can be streamlined and automated. In this project, I will use Github Actions to deploy a website to an AWS S3 bucket automatically.

Amazon S3 is a highly scalable and cost-effective object storage service that allows us to store and retrieve any amount of data, including website files. Github Actions is a powerful workflow automation tool that allows us to automate our software development workflows.

The goal of this project is to automate the deployment of a website to an AWS S3 bucket using Github Actions. I will create a Github repository to host the website code and configure a Github Actions workflow that will build the website and deploy it to the S3 bucket.

## Steps:

### 1. Setting up the project repository: 

Create one project directory on terminal.Create a Repository for my-web project on git hub.Clone the newly crteated my-web repo to integrated project
terminal. copy my-web project code to project directory. run "git status" command it will display the current status of your local repository, showing
any changes that have been made to files, and whether or not they have been staged (added to the staging area) or committed(added to the loca lrepository). 
run "git commit -m "add code" " it will create a new commit with the changes you have staged, along with the commit message you provided. The commit will 
be saved to the local repository history. Run "git push origin main" It will push the changes in your local repository to the remote repository. Specifically, this command pushes the changes on the local "main" branch to the "main" branch on the remote repository (in this case, the remote repository 
is named "origin").
   
### 2. Create one S3 bucket on AWS:

Create S3 bucket on Aws with name my-web. while creating S3 bucket allow public access to S3 bucket then click on create bucket.

### 3. Set up a github action workflow.

Here, we write a github action workflow for my-web project. the name of work flow is my-web deployment. the workflow push on main branch means if we make 
any changes in my-web main branch of git repository the work flow will start work or jobs. we can also add multiple branches.
    
#### Jobs Performed by github Action
    
- It will deploy one ubuntu VM environment to run jobs.
- By using "actions/checkout@v1" it will check over code.
- To access Aws account by configuring Aws credentials in github action work flow using "aws-actions/configure-aws-credentials@v1".
- In Aws IAM got Users create a access key for CLI.
- In github go to Settings, Secrate and Variable select Actions Create New repository secretes Enter Name "AWS_ACCESS_KEY_ID" and copy access key ID      from aws portal and paste it to Secrate. same steps for access key give name as "AWS_SECRET_ACCESS_KEY".
- By using command "aws s3 sync . s3://my-web-project" it will take a code from github and sync to Aws bucket and deploy web on S3 bucket.
 
 ### 4. Enable Static Website Hosting.
 
 Go to S3 Bucket click on properties go to static website hosting click on edit and enabled it and enter file name "index.html". It will allow bucket to 
 host website. Copy a web site link from static web site hosting.
        
 ### 5. Write a bucket policy.
 
Go to S3 bucket click on permissions go to bucket policy and click on edit write a policy for public read object for my-web-project bucket.
      
### 6. Deploying website on AWS S3.

Go to termianal. open index.html make some changes save it. Run command "git add index.html" then run "git commit -m "make some changes" ". and push it 
using command "git push origin main". Now goto github repo click on action It will start performing the deployment. one Deployment done. go to aws 
s3 bucket click on properties goto static web site hosting and a link from static web site hosting and paste it browser it will run my-web wesite.
    
## Key technologies used: 

- Github
- Github Action
- AWS S3
- AWS IAM
- CI/CD 
- Automation
- My-web Code
    
    
## Daigram:



   <img width="1396" alt="image" src="https://raw.githubusercontent.com/ahmad24mliwala/images/main/my-web-app-project-architecture.jpg?raw=true">




