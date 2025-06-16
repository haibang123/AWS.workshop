+++
title = "Introduction"
date = 2020
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

#  Building a Serverless Text-to-Speech Application with Amazon Polly

#### Introduction to Amazon Polly

**Amazon Polly is a text-to-speech (TTS)** service by Amazon that uses advanced deep learning technologies to synthesize lifelike human speech. It supports dozens of realistic voices across more than 20 languages, enabling developers to build voice-enabled applications for a global audience.

Polly addresses common challenges in TTS systems, such as:

Handling words that are spelled the same but pronounced differently (e.g., "live" in different contexts),

Text normalization (e.g., abbreviations like “St.” as “Street” or “Saint”),

Converting text to phonemes in complex languages like English (e.g., "tough", "though", "through"),

Dealing with foreign words, proper names, and slang (e.g., "déjà vu", "ASAP").

Amazon Polly delivers fast and consistent response times suitable for real-time interactive applications. You can cache or save audio files for offline playback or distribution — with no extra fees for using the speech output.

It's easy to use: just send text to the Amazon Polly API, and it returns an audio stream (e.g., in MP3 format) that your application can play or store.

In this workshop, you’ll build a simple serverless application using Amazon Polly to convert multilingual text into speech, which can be played directly in a web browser. This can be used for reading recipes, news, books, or any content hands-free.

#### Benefits of Amazon EKS

- Create an Amazon DynamoDB table to store data

- Create an Amazon API Gateway RESTful API

- Create AWS Lambda functions triggered by API Gateway

- Connect AWS Lambda functions with Amazon Simple Notification Service (SNS)

- Use Amazon Polly to synthesize speech in a variety of languages and voices

#### Challenges of Amazon Polly

- **Text Normalization**: Abbreviations and numbers may need preprocessing.

- **Homographs and Context**: Same spelling, different pronunciation (e.g., live).

- **Foreign Words and Proper Names**: Can be mispronounced (e.g., François).

- **Language and Voice Limitations**: Not all features work across all voices/languages.

- **Latency with Long Texts**: Delays with long text or multiple requests.

- **Usage Cost**: High usage can lead to high costs.

- **API Security**: Avoid exposing keys in frontend apps.

- **Limited Expressiveness**: Lacks natural human expressiveness.



#### Workshop Architecture

##### Architecture Overview

The diagram below illustrates the Amazon Polly system architecture we will deploy in this workshop:
![Workshop](../images/Diagramworkshop.png)

##### Architecture Description

- **User Interaction**:

  - Users load a static website hosted on Amazon S3.
  - They interact with a form (e.g., submit or view posts), which sends requests via Amazon API Gateway.

- **API Gateway triggers a Lambda function**:

  - If the request is to create a new post → API Gateway calls "New Post" Lambda.
  - If the request is to retrieve posts → it calls "Get Post" Lambda.


- **Lambda accesses DynamoDB**:

  - Both Lambda functions interact with Amazon DynamoDB, where post data is stored.


- **New Post triggers SNS notification**:

  - After a new post is added, the "New Post" Lambda function sends a message to Amazon SNS (Simple Notification Service).

- **SNS triggers another Lambda**:

  - The "Convert to Audio" Lambda function is triggered by SNS to handle the text-to-speech conversion.

- **Lambda calls Amazon Polly**:

  - The function uses Amazon Polly to synthesize speech from the text content.


- **Store the audio file**:

  - Polly returns an MP3 file, which is then stored in Amazon S3 (used for audio file hosting).



##### Workshop Objectives

- Understand the components of a text-to-speech architecture using Amazon Polly.
- Deploy a simple system using Amazon Polly along with other AWS services (S3, Lambda, API Gateway, DynamoDB, etc.).
- Integrate web tools and storage to generate and play audio files from user-submitted text.

{{% notice info %}}
This lab is conducted in the Singapore region (ap-southeast-1).
{{% /notice %}}
