# AWS DynamoDB


## Dynamo console

### Create table

![alt text](image.png)
![alt text](image-1.png)

### View table

![alt text](image-2.png)

### Insert record to table

![alt text](image-3.png)
![alt text](image-4.png)

### Update, delete record
![alt text](image-5.png)
![alt text](image-6.png)

*Delete*
![alt text](image-7.png)
![alt text](image-8.png)

### Query table with id = `testid-1`

![alt text](image-9.png)

### Scan table only by name attr

![alt text](image-10.png)

## Working with CLI

### Create table

![alt text](image-13.png)
![alt text](image-14.png)
![alt text](image-15.png)

### Load data

- Create a sample products.json file
![alt text](image-16.png)

- Load with CLI

![alt text](image-17.png)
![alt text](image-18.png)


### Read data

![alt text](image-19.png)


### Modify data

![alt text](image-20.png)

- Check data modified from 1200 quantity to 1300

![alt text](image-21.png)

## Lambda function to dynamodb

### Create lambda function to interact with dynamodb
```python
import json
import boto3
def lambda_handler(event, context):
    dynamodb = boto3.resource('dynamodb',region_name="ap-southeast-1")
    table = dynamodb.Table('dynamo-table')
    response = table.get_item(
        Key={
            "id": "testid-1"
        }
    )
    item = response.get("Item")
    return {
        'statusCode': 200,
        'headers': {
            'Content-Type': 'application/json',
            'Access-Control-Allow-Origin': '*'
        },
        'item': item,
        'body': json.dumps('Hello from Lambda!')
    }

```
![alt text](image-11.png)

### Test lambda function

![alt text](image-12.png)