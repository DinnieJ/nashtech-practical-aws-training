# Invoke Lambda in VPC

## Create VPC
- Create vpc for lambda with private subnet by availability zone
![create-vpc](./assets/image.png)

## Create the lambda function to invoke another lambda function

![create-lambda](./assets/image2.png)

Selecting VPC

![select-vpc](./assets/image3.png)

Created caller lambda function

![caller-lambda](./assets/image4.png)
![caller-lambda](./assets/image5.png)

## Create lambda destination function

![create-destination-lambda](./assets/image6.png)

![create-destination-lambda](./assets/image7.png)

## Create a vpc endpoint for lambda function

![create-vpc-endpoint](./assets/image8.png)
![create-vpc-endpoint](./assets/image9.png)

# Retest invoke function
- Adding permission to invoke lambda function from vpc endpoint

![add-permission](./assets/image10.png)
- Invoke lambda function from vpc

![invoke-lambda](./assets/image11.png)

- Found request with ID `f01a188e-1806-493d-9775-82c1fc2a2cb2` from Cloudwatch Log of destination function

![cloudwatch-log](./assets/image12.png)
