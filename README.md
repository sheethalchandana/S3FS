mount S3 bucket on Amazon EC2 Linux using S3FS
step 1: create a new IAM user
step 2: enter name and next
step 3:"attach policy directly"
               and
        "create policy"
step 4: while creating a policy select
         S3 as service
        and give list of actions required
        and next
step 5: give policy name and next
step 6: create a user and attach the policy which is created and click on next
step 7: after creating a user, go to security credentials
step 8: in "access key" create a "new key"
         select CLI
step 9: you will get "access key" and "secret key"(copy it for future reference)
step 10: create a EC2 t2 micro instance
step 11: SSH to server
step 12: install AWS CLI using
         (#sudo apt-get install awscli -y)
step 13: install S3FS using
         (#sudo apt-get install s3fs -y)
step 14: create a folder named "bucket" to location "/home/ubuntu/bucket"
         (#mkdir /home/ubuntu/bucket)
step 15: go inside bucket directory using
         (#cd $HOME/bucket)
step 16: add as many files required 
step 17: in AWS create a bucket
step 18: go to vm and configure aws cli
         (#aws configure)
         give the "access key" and "secret key"
step 19: run command 
         (#aws s3 sync /home/ubuntu/bucket s3://bucketname)
step 20: all the files present in EC2 will be uploaded to S3 bucket

         

         
