---
layout: post
title:  "AWS Gameday"
date:   2019-10-17 00:30:00
categories: aws cloud
tags: aws gameday
image: 
published: false
---

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2019-10-17-aws-gameday/scoreboard.png" alt="Scoreboard" />

AWS Gameday is a fun game like event where participants compete agains each other in teams.
The goal is to create and run online services of a Fictional company named Unicorn Rentals.

Each team gets access to an AWS cloud environment via AWS Console and API.

The game starts with some predefined services. For example a frontend API (called the "Service Router"). The purpose of Service Router is to be able to use microservices from other teams.

Each team is running one of the many Service Routers. 
The Service Router finds microservice endpoints from a DynamoDB table that each team should edit by adding service endpoints of other teams. 
Teh ultimate goal is to use many services, preferably the fastest ones and thereby gain a high score. The Legacy Services provided at the start of the game are very slow so each team should also swap their endpoints to optimized ones.

Tasks each team goes through:
- Deploy, Maintain and Optimize microservices for other teams to use.
- Publish teams services in "Services Marketplace" using a Dashboard. 
- Making teams Service Router highly available.
- Use the fastest microservices and score high 
- Keep everything going (use X-Ray, CW Metrics, CW Logs). Watch your score events for changes.

Things to avoid:
- Don't consume your own services

To maximise your score, you need to run copies of the microservices.
When another teams Service Router receives a request, they may use your microservice to perform some of the required operations. If so, you get a share of their score.

Services that each team needed to create and keep running.
swapcaser: SAM(Lambda and API Gateway)
reverser: Fargate
leeter:	Elastic Beanstalk

Some unexpected events were also possible like for example loosing a team member or getting hit by a security issue mid-flight.

There was also a Chat link for teams to use and ask for help from AWS professional services team.

The whole game lasted 3 hours. Originally this was ment to be run in a 4h session so this was a bit tight schedule.

Summary of what I accomplished:
I started one hour late without instructions as those were given in the beginning of the live stream. 
- Deploy Beanstalk application
- Fix Launch configuration to bring the application running again.
- Create an S3 bucket for application deployment purposes
- Upload the application sources and modified the Cloudformation template 
- Deploy Cloudformation template to create Serverless infra 


[readme]:      https://s3.amazonaws.com/ee-assets-prod-us-east-1/modules/gd2018-loadgen/v2/readme.md
[twitch]:   https://www.twitch.tv/aws/
