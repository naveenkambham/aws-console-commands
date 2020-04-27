##### Connecting to ec2 instance:

```
sudo chmod 400 /path/to/key.pem
ssh -i /path/to/key.pem ubuntu@ec2-**-***-***-***.compute-1.amazonaws.com
```

##### To copy a directory from local machine to ec2 instance

```
sudo scp -i /path/to/key.pem -r /Users/directory path/ ubuntu@ec2-**-***-***-***.compute-1.amazonaws.com:/home/ubuntu/directory path/
```

##### To copy a single file from local machine to ec2 instance

```
sudo scp -i /path/to/key.pem /Users/file path/ ubuntu@ec2-**-***-***-***.compute-1.amazonaws.com:/home/ubuntu/file path/
```
