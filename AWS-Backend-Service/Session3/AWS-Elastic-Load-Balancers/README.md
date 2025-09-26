# AWS ELB

- Continue from Session2/AWS-Elastic-Load-Balancers/README.md

## Create additional instance number 3 at `ap-southeast-1c`

![alt text](./assets/image.png)

## Create a target group that include all 3 instances

![alt text](./assets/image-1.png)

## Create Load balancer to this target group

![alt text](./assets/image-2.png)

## Have nginx serve html over 3 instances

![alt text](./assets/image-3.png)

![alt text](./assets/image-4.png)

![alt text](./assets/image-5.png)

## Test elb online

First time pointed to instance-2
![alt text](./assets/image-6.png)

Second time pointed to instance-1
![alt text](./assets/image-7.png)

Third and forth point to instance-3

![alt text](./assets/image-8.png)