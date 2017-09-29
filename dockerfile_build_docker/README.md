##### Get the AWS account id from meta-data
`account_id=$(curl -s http://169.254.169.254/latest/dynamic/instance-identity/document | grep -oP '(?<="accountId" : ")[^"]*(?=")')`

##### Build the docker image
`docker build -t sandbox .`

##### Tag the docker image
`docker tag sandbox $account_id.dkr.ecr.us-east-1.amazonaws.com/sandbox:0.0.1`

##### Push the docker image to AWS ECR
`docker push $account_id.dkr.ecr.us-east-1.amazonaws.com/sandbox:0.0.1`
