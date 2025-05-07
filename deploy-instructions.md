# Deployment Steps

1. **Launch EC2 Instance**
   - Amazon Linux 2
   - Install Docker: `sudo yum install docker -y`
   - Start Docker: `sudo service docker start`

2. **IAM Role or Keys**
   - Create IAM user or instance role with DynamoDB access.
   - Export or use env variables.

3. **Run Docker Container**
   ```bash
   docker run --rm -d -p 80:3000 --name node-dynamo-app \
     -e AWS_REGION=us-east-1 \
     -e AWS_ACCESS_KEY_ID=your-access-key \
     -e AWS_SECRET_ACCESS_KEY=your-secret-key \
     dockerhub-user/image-name
