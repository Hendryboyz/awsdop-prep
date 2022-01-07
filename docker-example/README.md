# docker-example for CodeBuild

> Follow the step in this [tutorials](https://docs.aws.amazon.com/codebuild/latest/userguide/sample-docker.html) to pratice CI/CD on AWS

## Troubleshooting
* Use go image from ECR public image gallery as base image to prevent you from encountering **the image pull limit error**
* Use `git clone` to avoid subtle error while pulling go module from github via go command
* **Change build command** because the origin command in the tutorial don't assign the right dirctory contains go source code 

