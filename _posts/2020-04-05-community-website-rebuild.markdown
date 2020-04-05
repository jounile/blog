---
layout: post
title:  "Rebuilding a community website"
date:   2020-04-04 17:30:00
categories:
tags: flask python jinja azure
image: 
published: false
---


[Nolla.net][nollanet] is a community website for board riders.
The original website was created in 2000 and was loved by the Finnish skateboarding community until it became non-functional due to technical issues around 2015. The website included a popular discussion forum and features for video and photo sharing. There was also possibility to write diaries, event calendar and to share industry news.

The implementation of the website was rather old school and chaotic as multiple independent developers had written features directly in production environment for multiple years. It was built without any framework using PHP and the MySQL database was polluted with random obsolete data. 

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2020-04-05-nollanet/original_website.png" alt="Nolla.net" />

I was given access to the application server and database by a friend who was hosting it and decided to have a look what could be done to improve the situation. I had a couple of ideas in mind.
1. Check what features could be re-written with a reasonable effort.
2. Analyse what parts of the data would need to be cleaned. 
3. Think about how to improve the website architecture.
4. Consider how to improve security

After doing the initial analysis I decided to rewrite the website to make it functional again. 
My motivation was to see individuals continue documenting the Finnish skateboarding scene and to enable unofficial communication between members of the community. I decided to re-write the main features and discontinue some other features. This was also a great opportunity to learn some new technologies which is why I chose Python as the programming language and Flask as the web-framework. The site was to be hosted in Azure as my friend happened to have free credits that could be used for this purpose.

The most important improvements:

Security:
- Encrypted user passwords
- Using SSL
- Preventing SQL injections
- Requiring Captcha when registering new user
- Moving all secrets to environment variables

Scalability:
- Hosting MySQL database in Azure 
- Hosting web application in Azure App Service
- Hosting media files in Azure Blob Storage

Operations:
- Continuous Deployment: Github -> Azure

Content management:
- New content can be created and published later.
- Content creation is available for registered users
- Content administration is available for admin users

Kept features included Photos & Videos sections. News, interviews, reviews and spots were also kept. Facebook page feed continues updating on the frontpage and Facebook Comments social plugin was enabled so that users can share their comments. The database got partly re-structured and for example passwords were encrypted. Also data was cleaned where necessary. Usability improved by adding paging to speed up the page loading times.

Also, some new features were introduced. For example Links section was added with required administration tools and Youtube playlists page was added. Also user registration process was re-designed and a password reset feature was added.


<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/2020-04-05-nollanet/rebuilt_website.png" alt="Nolla.net" />

The source code can be found in my [Github][github]
Pull Requests are welcome if you fell like contributing.

[nollanet]:   https://www.nolla.net
[github]:   https://github.com/jounile/nollanet
