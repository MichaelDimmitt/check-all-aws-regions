## Just want to get a list of all my AWS resources
https://forums.aws.amazon.com/thread.jspa?threadID=235322

## tldr:
This looks more built out, but possibly more brittle:<br/>
https://github.com/devops-israel/aws-inventory

The script I wrote is very simple is in this repo and can be found here:
https://github.com/MichaelDimmitt/check-all-aws-regions/blob/main/regions.sh

## Check-all-aws-regions
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-available-regions

## Setup: 
You will need to generate a client secret from IAM admin:<br/>
https://console.aws.amazon.com/iam/home#/users/Administrator?section=security_credentials
```bash
{
brew install aws-cli;
aws configure # paste id and secret here.
}
```

```bash
# commands to build:
# cat ./regions.txt | command xargs -I {} echo "echo \"aws resourcegroupstaggingapi get-resources --region {}\$(aws resourcegroupstaggingapi get-resources --region {})\"" > regions.sh
# now cleanup files using vim files: `:%s/ctrl-v + ctrl m/ /; :%s/ctrl-v + ctrl m//;`
```

## Check all of your regions:
```bash
bash regions.sh
```
