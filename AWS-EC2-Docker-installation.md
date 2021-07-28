### Docker installaction on EC2
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html

### To install Docker on an Amazon EC2 instance

#### 1. Launch an instance with the Amazon Linux 2 or Amazon Linux AMI. For more information, see Launching an instance in the Amazon EC2 User Guide for Linux Instances

#### 2. Connect to your instance.

#### 3. Update the installed packages and package cache on your instance.
```console
sudo yum update -y
```
#### 4. Install the most recent Docker Engine package. 

Amazon Linux 2
```console
sudo amazon-linux-extras install docker
```

Amazon Linux
```
sudo yum install docker
```

#### 5. Start the Docker service.
```
sudo service docker start
```

#### 6. Add the ec2-user to the docker group so you can execute Docker commands without using sudo.
```
sudo usermod -a -G docker ec2-user
```

#### 7. Log out and log back in again to pick up the new docker group permissions. You can accomplish this by closing your current SSH terminal window and reconnecting to your instance in a new one. Your new SSH session will have the appropriate docker group permissions.

#### 8. Verify that the ec2-user can run Docker commands without sudo.
```
docker info
```
