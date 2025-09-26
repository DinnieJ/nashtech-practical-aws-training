# AWS EC2 EBS

## Create EC2 instance at ap-southest-1a

![alt text](./assets/image.png)

## Create EC2 instance at ap-southest-1b

![alt text](./assets/image-1.png)

## Create an EBS volume

![alt text](./assets/image-2.png)

## Attach volume to instance running at ap-southeast-1a

![alt text](./assets/image-3.png)

## Checking volume existed on instance

![alt text](./assets/image-4.png)

- Creating file system xfs on volume

![alt text](./assets/image-5.png)

![alt text](./assets/image-6.png)

- Mounting folder from instance to volume

![alt text](./assets/image-7.png)

- Updating Fstab to auto mount on boot

![alt text](./assets/image-8.png)

![alt text](./assets/image-9.png)

- Creating test file to folder `/ebstest`

![alt text](./assets/image-10.png)

## Create ebs snapshot for instance 1 at '/dev/sdf'

![alt text](./assets/image-11.png)
- Create volume from snapshot with availability zone `ap-southeast-1b`

![alt text](./assets/image-12.png)
![alt text](./assets/image-13.png)

- Attach volume to instance running at ap-southeast-1b

![alt text](./assets/image-14.png)

- Access instance at ap-southeast-1b and check the file exist

![alt text](./assets/image-15.png)