---
layout: post
title: "AWS Summit Switzerland"
date: 2019-10-02 10:00:00
categories: 
tags: aws summit
published: true
---


The event was opened by a new AWS country lead who had started working for AWS only 8 weeks ago. She did extremely well on her opening speach. 

The keynote from Ian Massingham included some news and insights of the current state of Amazon Web Services.

Great event from content perspective. A lot of focus was on Serverless as one might expect. I gathered the most interesting topics on this blog post and also shared it with my colleagues in realtime.


Amount of Windows workloads on AWS is rather surprising.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/windows.jpg" />

Lambda integrates with 47 other services. 

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/lambda.jpg" />

AWS has learned from their customers that majority of infrastructure cost for doing Machine Learning comes from inference, not training.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/inference.jpg" />

Therefore there has been some recent development to reduce costs.
Notice the pre-announcement of a new service AWS Inferentia.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/inference_solutions.jpg" />


AWS benefits from Amazon’s long heritage on Machine Learning and the technology coming from these lessons learned is now available also for AWS customers.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/amazon_heritage.jpg" />

AWS IoT services has quite a growth. New services and feature additions are comprehensive.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/iot.jpg" />

Pretty good keynote with customer stories in my opinion.

I attended the following sessions:
1. Security - Don’t leave it for later
2. Migrate your website to AWS - Do and Don’t. A customer perspective
3. Deep Dive on Serverless Architectures
4. Deep Dive on Containers
5. AWS for highly regulated industries
6. Simplify your Front End Apps with Serverless Backend in the cloud

<h3>Security - Don’t leave it for later</h3>
(by Swisscom)

Not often I come across such interesting presentation about security. 

At Swisscom you can request for an AWS account for your project via online form. After automated provisioning the sub-account will instantly become monitored by their Security team.
Some custom setup with AWS Organizations to allow project accounts, sandboxes and centralized services.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/swisscom.jpg" />

<h3>Migrate your website to AWS - Do and Don’t. A customer perspective</h3>
(by Anwalt.de)

The second session included some good advices:
- Use reserved instances to reduce cost
- Use CDN for caching on the Edge
- Use Shield to prevent DDoS attacks


<h3>Deep Dive on Serverless Architectures</h3>

Two Senior Solutions Architects from AWS showed how to create a project template with Serverless Architecture (including authentication, CI/CD pipeline and monitoring)
Services used were AWS Amplify, CodeStar, AWS CDK, X-Ray.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/serverless1.jpg" />

Sanity check against customer requirements. 

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/serverless2.jpg" />



<h3>Customer journey to Serverless architecture</h3>

Homegate AG shared their experiences on re-architecting a real estate platform. 
70% of their develop time was spent on bug fixing a monolith. Asking around at conferences everyone was pointing them towards Kubernetes. Security was the main reason for them for going Serverless.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/homegate.jpg" />



<h3>Simplify your Front End Apps with Serverless Backend in the cloud</h3>

I really enjoyed the last session that was a walkthrough of AWS Amplify.
The service is an amazing combination of easy to use components which can be utilized with just a few commands. The presentation included creating a ticket service app with authentication (AWS Cognito). 

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-03-aws-summit-switzerland/amplify.jpg" />

Finally I want to leave you with advice from one of the customers presenting in the event.

"Don´t get locked up into avoiding lock-in"

<a href="https://aws.amazon.com/events/summits/switzerland/" target="_blank">https://aws.amazon.com/events/summits/switzerland/</a>
