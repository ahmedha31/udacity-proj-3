# Pipeline process

our pipeline can be summarized in few steps :

1. developer update codebase in local env
2. when updated code is pushed to github circleci triggers some actions
   1. install node/ aws-cli / eb-cli
   2. install dependencies for front-end
   3. build front-end
   4. install dependencies for back-end
   5. build back-end
   6. update back-end code in elastic-beanstalk
   7. update front-end code in its S3 bucket

## pipeline Infrastructure diagram

1. developer push code to github
2. circleci triggers some actions
3. circleci update code in elastic-beanstalk
4. circleci update code in S3 bucket


![pipeline diagram](./pipline_1.png)