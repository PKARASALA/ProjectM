## Step-1 : Setup Linux VM (Amazon Linux AMI)

1) Login into AWS Cloud account
2) Launch Linux VM using EC2 service
   
     - AMI : Amazon Linux
     - Instance Type : t2.medium
       
4) Connect to VM using MobaXterm

## Step-2 : Install Docker In Linux VM

```
$ sudo yum update -y 
$ sudo yum install docker -y
$ sudo service docker start
```
## Step-3 : Add ec2-user to docker group 

```
$ sudo usermod -aG docker ec2-user
```

## Step-4 : Restart the session
$ exit

## Step-5 : Rress 'R' to restart the session (This is in MobaXterm)

## Step-6 :  Verify docker installation
$ docker -v

## Step-7 : Run nexus using docker image
```
$ docker run -d -p 8081:8081 --name nexus sonatype/nexus3
```

## Step-8: Enable 9000 port number in Security Group Inbound Rules & Access Sonar Server
```
 - URL : http://public-ip:8081/
```

## Step-8 
...
$ docker stop --time=120 <CONTAINER_NAME>

## Step-9
...
$ curl http://localhost:8081/