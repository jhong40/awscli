# awscli

```
aws iam list-policies | jq '.Policies[] | select(.PolicyName|test("^dev-")).Arn'
aws iam delete-policy --policy-arn arn:aws:iam::123456789012:policy/MySamplePolicy

aws s3 rb --force s3://my-s3-log

aws iam delete-role --role-name myrole
aws iam list-instance-profiles-for-role --role-name dev-ec2_role
aws iam remove-role-from-instance-profile --instance-profile-name dev_ec2_role_profile --role-name dev-ec2_role
aws iam delete-instance-profile --instance-profile-name dev_ec2_profile


aws ec2 describe-security-groups \
    --filters Name=group-name,Values=*myname*  \
    --query "SecurityGroups[*].{Name:GroupName,ID:GroupId}"

aws ec2 delete-security-group --group-id sg-90348843
aws ec2 revoke-security-group-ingress  --group-id sg-04639944 --protocol tcp --source-group sg-488884 --port 0-65535

aws iam delete-open-id-connect-provider --open-id-connect-provider-arn myarn

aws eks list-clusters
aws eks delete-cluster --name myeks
aws eks describe-cluster --name myeks


aws eks describe-cluster --name experian-ais | jq -r '.cluster.status'
 

```
