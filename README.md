# s3-pipeline-codestar deploy command
aws cloudformation deploy \
--stack-name s3-pipeline-codestar-stack \
--template-file s3-pipeline-codestar.yml \
--parameter-overrides file://parameters.json \
--capabilities CAPABILITY_NAMED_IAM \
--profile Administrator
