ECR is a repository for your docker images. It stores them, serves them with high availability, versions them, and makes them available to fargate.

Once you've created your target image, we need it to be accessible by aws so that we can host our application up in the cloud.

In order to upload your images to ecr we will want to either use the aws-cli or a CI/CD tool ie: CodeBuild/Jenkins