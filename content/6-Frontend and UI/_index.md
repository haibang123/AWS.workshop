+++
title = "Frontend and UI"
date = 2020
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

## Frontend / UI

**Serverless Interface** In this task, you will build a static web-based user interface that allows users to:

Submit a text post with a selected Amazon Polly voice

View the list of posts

Listen to the generated audio for each post

The frontend is hosted on Amazon S3 and interacts with your backend Lambda functions via API Gateway.



## Create a Serverless UI

This step involves uploading a simple HTML + JavaScript application to an S3 bucket and configuring it to connect with your deployed APIs.

🧰 What the UI will do:
-Send a POST request to create a new post

-Poll the API to get post details

-Display the original text and a playable audio file (MP3)

-Allow language and voice selection from Amazon Polly

🧪 Requirements:
-The S3 bucket must be configured for static website hosting

-Your API Gateway must have CORS enabled

-Update the JavaScript file with your actual API endpoints


  - Sreach and select **S3**
  - Select **Create Bucket**

  ![Glue](/images/6/6.0.png?width=90pc)

  - Choose **General purpose**
  - Select **Bucket name**
  - Select **Create Bucket**

  ![Glue](/images/5/5.21.png?width=90pc)


  - Choose **Add files**
    ![Glue](/images/6/6.1/6.1.png?width=90pc)

- In the **Buckets** step

  - Choose **Bucket policy**
  - Click **Next**
    ![Glue](/images/6/6.1/6.2.png?width=90pc)


- In the **Bucket policy** step
  - Add **data source**
  - select **Save change**

  ![Glue](/images/6/6.1/6.3.png?width=90pc)

- In the **Block public access** step
  - Choose **Delete all**
  - click **confirm**

  ![Glue](/images/6/6.1/6.4.png?width=90pc)

  - Click **Link**
    ![Glue](/images/6/6.1/6.5.png?width=90pc)

- In the **Link** 
  - Add **Content**
  - Copy **ID**
  - Add **Information**
  - **Complete**

    ![Glue](/images/6/6.1/6.6.png?width=90pc)
