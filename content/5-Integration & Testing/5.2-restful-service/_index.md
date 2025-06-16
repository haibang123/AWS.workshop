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
     ![ConnectPrivate](../../images/5/5.7.png)

2. 

- Select **New API**
- Select **API name**
  ![ConnectPrivate](../../images/5/5.8.png)

3. Add **Description**

- Choose **IPv4** 

  - Enter **Create API**

  ![ConnectPrivate](../../images/5/5.9.png)


  - Click **Creta method**
  ![ConnectPrivate](../../images/5/5.10.png)

  - Select **Method Get**
  - Click **lambda function**
  - Select **funtion Postreader**
  - Click **Create method**

  ![ConnectPrivate](../../images/5/5.12.png)

- In the **API** step

  - Choose **Enable CORs**
  
  ![ConnectPrivate](../../images/5/5.13.png)

- In the **Gateway responsea** step

  - Click **Default 4XX**
  - Click **Default 5XX**

- In the **Access-control-allow-Methods** step

  - Click **GET**
  - Click **POST**
  -Select **Save**

  ![ConnectPrivate](../../images/5/5.14.png)

  - Click **Integration request**
  - Select **Edit**


  ![ConnectPrivate](../../images/5/5.15.png)

- In the **Mapping templates** step

  - Choose **application/json**
  ![ConnectPrivate](../../images/5/5.16.png)
- In the **Template body** step
  - Add **data soure**
  - select **Save**


  ![ConnectPrivate](../../images/5/5.17.png)
- In the **API Gateway** step


  - Click **Deloy API**

  ![ConnectPrivate](../../images/5/5.18.png)

  - Choose **New Stage**
  - Choose **Dev**
  - select **Deloy**

  ![ConnectPrivate](../../images/5/5.19.png)
  - Deloy Complete
  ![ConnectPrivate](../../images/5/5.20.png)

