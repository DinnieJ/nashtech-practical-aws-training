# AWS Route 53 Healthcheck Failover Routing

## Create ec2 instance with hosted html number 1

![alt text](image-2.png)

## Create ec2 instance with hosted html number 2
![alt text](image-4.png)

## create healthcheck for ec2 instance host
![alt text](image-1.png)

## Create Route53 record for both ec2 and s3, with failover to healthcheck
![alt text](image-5.png)


## Test with curl from instance-2

- See the html return is from instance number 1

![alt text](image-3.png)

- Kill instance 1

![alt text](image-6.png)

- Service become unhealthy

![alt text](image-7.png)

- Retest with curl

![alt text](image-8.png)