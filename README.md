# lambda-to-access-the-secrets-manager
To access the secrets manager credentials such as API from Lambda Function

**Step-1: To create a API credentials in Secret Manger**

Navigate to AWS Secrets Manager console and select - create a new key with "Other type of secret"

![sm1](https://github.com/kohlidevops/lambda-to-access-the-secrets-manager/assets/100069489/e9ffe242-e1dc-4c1b-830c-655e8a5b8735)
Provide the meaning ful secrets manager name

![sm2](https://github.com/kohlidevops/lambda-to-access-the-secrets-manager/assets/100069489/b4f35e0a-28fc-4f4b-80fd-3fb0381c1c69)

**Step-2: To create a IAM role for Lambda to access the secrets manager**

Create IAM policy for secrets manager Read only access with secret ARN
Create IAM Role for Lambda function and associate the secret manager Read Only policy and Lambda basic execution policy

<img width="724" alt="sm3" src="https://github.com/kohlidevops/lambda-to-access-the-secrets-manager/assets/100069489/0daf394c-8dd1-4c3e-8687-0b27ad58088c">

**Step-3: To create a Lambda Function**

Create Lambda Function (Python-3.10) and associate the newly created IAM role
Deploy code using below link and save & test it

https://github.com/kohlidevops/lambda-to-access-the-secrets-manager/blob/main/lambda-python-code

![sm5](https://github.com/kohlidevops/lambda-to-access-the-secrets-manager/assets/100069489/e088255c-ebb4-4165-845a-f78577329bc3)

![sm6](https://github.com/kohlidevops/lambda-to-access-the-secrets-manager/assets/100069489/0d2ce2b4-5fb9-44de-8ce4-2615f38c47c6)
