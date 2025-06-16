+++
title = "RESTful Web Service"
date = 2020
weight = 2
chapter = false
pre = "<b>5.2. </b>"
+++

## RESTful Web Service

1. Search and select **AWS API**

   ![Lambda](/images/5/5.7.png?width=90pc)

2. 

- Select **New API**
- Select **API name**
  ![Lambda](/images/5/5.8.png?width=90pc)

3. Add **Description**

- Choose **IPv4** 

  - Enter **Create API**

  ![Lambda](/images/5/5.9.png?width=90pc)


  - Click **Creta method**

  - Select **Method Get**
  - Click **lambda function**
  - Select **funtion Postreader**
  - Click **Create method**

  ![Lambda](/images/5/5.12.png?width=90pc)

- In the **API** step

  - Choose **Enable CORs**
  
    ![Lambda](/images/5/5.13.png?width=90pc)

- In the **Gateway responsea** step

  - Click **Default 4XX**
  - Click **Default 5XX**

- In the **Access-control-allow-Methods** step

  - Click **GET**
  - Click **POST**
  -Select **Save**

  ![Lambda](/images/5/5.14.png?width=90pc)

  - Click **Integration request**
  - Select **Edit**


  ![Lambda](/images/5/5.155.png?width=90pc)

- In the **Mapping templates** step

  - Choose **application/json**
    ![Lambda](/images/5/5.16.png?width=90pc)

- In the **Template body** step
  - Add **data soure**
  - select **Save**


    ![Lambda](/images/5/5.17.png?width=90pc)
- In the **API Gateway** step


  - Click **Deloy API**

  ![Lambda](/images/5/5.18.png?width=90pc)

  - Choose **New Stage**
  - Choose **Dev**
  - select **Deloy**

  ![Lambda](/images/5/5.19.png?width=90pc)

  - Deloy Complete
    ![Lambda](/images/5/5.20.png?width=90pc)

