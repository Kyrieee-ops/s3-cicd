# s3-cicd deploy command
aws cloudformation deploy \
--stack-name s3-cicd-stack \
--template-file s3-cicd.yml \
--capabilities CAPABILITY_NAMED_IAM \
--profile Administrator
