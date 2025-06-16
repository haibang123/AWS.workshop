+++
title = "IAM Role"
weight = 1
chapter = false
pre = "<b>2.1. </b>"
+++

## Creating an IAM Role

In this step, we will navigate to the IAM Console and create a role for the lambda service. This role will allow AWS lambda to access data stored in S3 and create necessary objects in the lambda Catalog.

1. Access the [AWS Management Console](https://aws.amazon.com/console/)

   - Search for **IAM**
   - Select **IAM** to open the **IAM Dashboard**

![ConnectPrivate](../../images/1/1.1.png)

2. In the IAM Dashboard

   - Select **Roles**
   - Click **Create role**

   ![ConnectPrivate](../../images/1/1.2.png)

3. In the **Create role** interface, under **Select trusted entity**

   - Choose **AWS Service**
   - Under _Service or use case_, select **lambda**
   - Click **Next**

   ![ConnectPrivate](../../images/1/1.2.png)

4. In the **Create role** interface, under **Add Permission**

   - Search for and select **AmazonS3FullAccess**

   ![ConnectPrivate](../../images/1/1.3.png)

   - Search for and select **AWSlambdaServiceRole**
   - Click **Next**

   ![ConnectPrivate](../../images/1/1.4.png)

5. In the **Create role** interface, under **Name, review and create**

   - In **Role name**, enter `AWSlambdaServiceRoleDefault`
     ![ConnectPrivate](../../images/1/1.5.png)
   - Review the role details under **Select trusted entity** and **Add Permission**
     ![ConnectPrivate](../../images/1/1.5.png)
   - Click **Create role**
     ![ConnectPrivate](../../images/1/1.6.png)

6. Successful role creation interface:
  
