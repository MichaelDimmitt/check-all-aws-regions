# check-all-aws-regions

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-available-regions
```bash
# commands to build:
# cat ./regions.txt | command xargs -I {} echo "echo \"aws resourcegroupstaggingapi get-resources --region {}\$(aws resourcegroupstaggingapi get-resources --region {})\"" > regions.sh
# now cleanup files using vim files: `:%s/ctrl-v + ctrl m/ /; :%s/ctrl-v + ctrl m//;`
```
