# Project Summary

In this project, a Jenkins pipeline was developed to deploy a static website in the cloud using Amazon AWS. The github repo that hosts the website is hooked into the Jenkins pipeline to automate the build process. The Jenkins server was hosted in an Amazon EC2 instance and the website in S3 bucket. To gaurantee the quality of the web content, the first stage in the Jenkins pipeline makes use of linting services for html files.
