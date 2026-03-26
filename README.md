# aws-project-1-text-to-audio-using-polly
First Project in DevOps Journey

Text to Audio Converter pipeline using Amazon Polly.

Architectural Diagram

<img width="963" height="510" alt="image" src="https://github.com/user-attachments/assets/9983e878-5ef5-440f-afa8-fa3e9da0b5bd" />

Amazon Polly --> Provided by AWS, helps to convert Text-to-Speech. 

Realistic Speech

Options to customize

SSML Support

******Steps to be performed*******

1. Exploring Amazon Polly
  
2. Creating an IAM role:
   
    Role Name: PollyTranslationRole
   
    Policies: AmanzonPollyFullAccess
   
              AmazonS3FullAccess
   
              AWSLambdaBasicExecutionRole.

3. Creating a source & Destination S3

  Buckets:
  
    Source S3 Bucket Name: twy-polly-text-files-storage-bucket-1
    
    Destination S3 Bucket Name: twy-polly-audio-files-storage-bucket-1

4. Writing Lambda function code:

    [lambda-function.py](https://github.com/user-attachments/files/26266047/lambda-function.py)

    except Exception as e:
        print("Error:", str(e))
        return {
            "statusCode": 500,
            "body": json.dumps({"error": str(e)})
        }
