# AWS VPC,IGW,Public subnet exercise

## Create VPC with name `demo-vpc` and CIDR `10.16.0.0/16`

![create-vpc](assets/image.png)

## Create Subnet

Creating 2 public subnet with CIDR block `10.16.0.0/20` and `10.16.16.0/20`

![create-subnet](assets/image2.png)

## Create Internet Gateway

Creating IGW and attach it to `demo-vpc`

![create-igw](assets/image3.png)

## Create Route Table

- Create route table for `demo-vpc` named `rt-web-demo-vpc`

![create-rt](assets/image4.png)

- Associate subnet to rt

![associate-rt](assets/image5.png)

- Add new route for IPv4 (0.0.0.0/0 to `igw-demo-vpc`)

![add-route](assets/image6.png)

## Create EC2

- Create EC2 instance for testing public subnet

![create-ec2](assets/image7.png)

- Try to connect to EC2 instance with SSH

![connect-ec2](assets/image8.png)

- Try to ping `google.com` from EC2 instance successfully

![ping-google](assets/image9.png)

## Test scenario: Remove public subnet and retry to connect to EC2

- Subnet detached 

![detach-subnet](assets/image11.png)

- Unable to connect to EC2 instance

![unable-connect-ec2](assets/image10.png)

## Test scenario: Delete outbound rule
**Expected: Unable to access internet from inside EC2 instance**

- Delete outbound rule
![delete-outbound-rule](assets/image13.png)

- Try to ping `google.com`
![unable-access-internet](assets/image12.png)


## Create Network Access Control List (NACL)

- Creating NACL for `demo-vpc`

![create-nacl](assets/image14.png)

- Associate NACL to subnet `public-subnet-1`

![associate-nacl](assets/image15.png)

- Now, we will unable to connect to EC2 instance

- Update inbound rule and outbound rule

![update-nacl](assets/image16.png)
![update-nacl](assets/image17.png)
