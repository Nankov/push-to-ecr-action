Repository for GitHub composite action that pushes Docker image to ECR

The following custom action is used for building, tagging and pushing images to ECR.
It takes 5 required inputs: 

  image-name: The name of the docker image
  tag: The tag name for the image
  aws-region: The AWS region name in ID format e.g eu-west-1
  account-id: The ID of the account owner of the ECR repository
  repository: The name of the ECR repository
 
Note that you do have to configure your AWS credentials in the same job in which you call the push-to-ecr-action action. You can do so via using the aws-actions/configure-aws-credentials@v1 action. You also have to login to ECR using aws-actions/amazon-ecr-login@v1
  
