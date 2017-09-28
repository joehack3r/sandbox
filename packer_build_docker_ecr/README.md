`account_id=$(curl -s http://169.254.169.254/latest/dynamic/instance-identity/document | grep -oP '(?<="accountId" : ")[^"]*(?=")')`
`/usr/local/bin/packer build -var "aws_account_id=${account_id}" -var 'version=0.0.1' build_docker.json`
