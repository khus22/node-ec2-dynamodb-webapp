# Deployment Steps

1. **Launch EC2 Instance**
   - Amazon Linux 2
   - Install Docker: `sudo yum install docker -y`
   - Start Docker: `sudo service docker start`

2. **IAM Role or Keys**
   - Create IAM user or instance role with DynamoDB access.
   - Export or use env variables.
     
3. **Pull the Docker image from Docker Hub**
     ```bash
     docker pull philippaul/node-dynamodb-demo
     ```
     
4. **Run Docker Container**
   ```bash
   docker run --rm -d -p 80:3000 --name node-dynamo-app \
     -e AWS_REGION=us-east-1 \
     -e AWS_ACCESS_KEY_ID=your-access-key \
     -e AWS_SECRET_ACCESS_KEY=your-secret-key \
     dockerhub-user/image-name
   ```
- docker run	Tells Docker to run a container
- --rm	Automatically removes the container when it stops
- -d	Runs the container in detached mode (in the background)
- -p 80:3000	Maps port 3000 inside the container to port 80 on the host (so you can access it via browser)
- --name node-dynamo-app	Names the container for easier reference
- -e AWS_REGION=...	Sets the AWS region for SDK (e.g., us-east-1)
- -e AWS_ACCESS_KEY_ID=...	AWS access key for programmatic access to DynamoDB
- -e AWS_SECRET_ACCESS_KEY=...	AWS secret key
