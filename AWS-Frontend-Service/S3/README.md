# AWS S3 Frontend

## Create S3 static hosting

![alt text](image.png)

Hosturl :https://hosting-buckets2.s3.ap-southeast-1.amazonaws.com/index.html

![alt text](image-1.png)

## Implement cross region replication

- Create new bucket in Tokyo region

![alt text](image-2.png)

- Create replication rule for source bucket to replicate

![alt text](image-4.png)

- Upload file in source bucket

![alt text](image-3.png)

- File got replicated in tokyo region bucket

![alt text](image-5.png)


## Generate presign url

- Block all access to the bucket

![alt text](image-6.png)

- Tried to access s3 url

![alt text](image-7.png)

- Generate presign url with `index.html` file
![alt text](image-8.png)

- Tried to access s3 url with presign url


https://hostbucketaws.s3.ap-southeast-1.amazonaws.com/index.html?response-content-disposition=inline&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEBMaDmFwLXNvdXRoZWFzdC0xIkcwRQIgduvPemhD7FgohrfZ11VB%2FKiR1KYMHZwKhCUjoA87HkUCIQDQohMvE50Fcusd1bKAZDbufYgLX2uBLxKUA2KsYsZ8ySrCAwic%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDAyNTk3MTM4ODM2MyIMBIj7teRBn%2FW0Snb%2FKpYDD2HNv91Ck9u9zmtOlQeP8sgw5JM9xvgVa5GWw2BIcPw1364ZZkRKReM%2FYHh5cT08FyyfLPhM6lytTF6uiRwnL2g1JXN%2BTkcQ2iZDANR6mQusqH6oRNMfx8WMquxQ5ylo%2FRlYTRxtreKyBoqJ1H3NzRFjft4Jhc5rTQAGLvey1YhTZip4AThYES4s0yd1Bfl63XpNdj4gHcKvE77%2Fq%2BACnFnSlCi23p3mGP2quIn%2FaatA2NqEa64p3AqlWzE68FQ7FBwUDXIDdrPQAAiCbQ6oLCsBgorGELCo%2FlKyZ2L3W6bCY08uPhEBYo7TfCyijjgsVii9C6r6nQleJ9gfUsL6FCkWVuKNv%2FPsHVEVCvQSzudz83kp6ZXW3dEN%2Bvdanj0KSUTkvn9R7mYKkiFc00A003u%2BF0xo8Hiu%2FaykJU4PjZR5BJCm7s3HdeqrK5FLZTJAKZB%2F0zBkSWlKMR9nhNr8swcn%2BRX4OzZmY9x%2BKEFhCH3u%2FBMJVi7JLwJWozl48d0SQg0H3g30E7Zs85DL6tK4BNc3rdAjTjCZmt3GBjreAkiefQzGnySBV%2FNJjlsiaKE3og1%2FtMeghvzZDwwOxcdB%2B6UogV0GHZBvINQLzOPtF3nJfQTpI7nITypinqJNlX99LNAyi3sYtjHMSYlE7itw34ZOzyoCqR63T4ii%2FUNIRj%2BQ9bB2SsbgvLhmMGV7ya9dvoHxJJQyqIOjQ5qcpog8A83h561hAQdNjnnDLwfJ24QmgKpufhkgXZtA9Ncz3Dmyg299aKjYrFjEu62d16D3LH4y3M5VDI1lIJ%2FPt1a%2B4RsMTqD6GbcB2RlNozd%2FGt6KKVPl2akliIwMqF5b%2BemK3ddxUts2FtCq4VjHe7%2FonXVt0YD5cGBnqvp34Lvx4vzjQGSl3xDwH%2FdQ0rJKxFalAj0prHQME5H1uizvwC1k%2Fb2F27v9pZ6SWVvK%2F6ufUiDJgrHWbKSMoiLKD3NVTB4WYUpQZv1swYu1q6M3HUQBAw1wo%2FSuB6OoPV9b3tpg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=ASIAQMDAD57FZPM7MWUL%2F20250927%2Fap-southeast-1%2Fs3%2Faws4_request&X-Amz-Date=20250927T023856Z&X-Amz-Expires=60&X-Amz-SignedHeaders=host&X-Amz-Signature=92112c2d1eb53b2f5aa8abcc9473ecd8f343a93bb4bc1246be492400c1f92e62


![alt text](image-9.png)