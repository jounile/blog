---
layout: post
title:  "Augmented reality app"
date:   2019-05-06 21:34:25
categories: mediator feature
tags: featured
image: /assets/article_images/2014-11-30-mediator_features/night-track.JPG
published: true
---
#AR with AWS Sumerian

This weekend I decided to test Amazon Sumerian more and see if I could make something interesting with it. I came across this <a href="https://www.youtube.com/watch?v=QKeCDZWkExQ">recording</a> and just followed the guide.


Apparently an easy way to get started with AR in Sumerian is to clone the <a href="https://github.com/aws-samples/amazon-sumerian-arkit-starter-app">Amazon Sumerian ARKit starter app</a>.


<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+19-05-2019%2C+0.35.15.jpg" width="" height="">

Click Publish and copy the URL to your public hosted scene.

In XCode you need to change the sceneURL to the previously copied URL.
Also append in the end of the URL /?arMode=true

If the Xcode build fails with something saying "Trust" you should go to iPhone settings -> General -> Device Management -> Your developer account and click Trust (developer account).

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+18-05-2019%2C+23.45.08.png" width="30%" height="30%">

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+18-05-2019%2C+23.47.50.png" width="30%" height="30%">

When the AR app tries to launch on the iPhone you need to allow accessing device Camera. 

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+18-05-2019%2C+23.52.26.png" width="30%" height="30%">

You should see the progress bar and your AR app name or this error message if something goes wrong.


<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+18-05-2019%2C+23.52.36.png" width="30%" height="30%">

 

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+18-05-2019%2C+23.53.38.png" width="50%" height="50%">


<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+18-05-2019%2C+23.52.51.png" width="50%" height="50%">

When the app starts it might take a second or two to load this box onto the scene.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+19-05-2019%2C+0.16.47.jpg" width="" height="">

Look around and you should see other content you placed on the scene in Sumerian.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+19-05-2019%2C+0.05.56.jpg" width="50%" height="50%">

Your scene items get augmented into the scene you are currently. 
<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+19-05-2019%2C+0.17.49.jpg" width="" height="">

For example here the lamps are placed in the ceiling.

<img src="https://s3.eu-central-1.amazonaws.com/jounileino.com-images/arkit-sumerian/Photo+19-05-2019%2C+0.26.51.jpg" width="" height="">



Guide for adding trusted app on iphone:

<a href="
https://www.youtube.com/watch?v=7ejkoLgoPGk"></a>

Also, see the Amazon Sumerian [website][sumerian] for more info. 


<footer class="site-footer">
 <a class="subscribe" href="{{ "/feed.xml" | prepend: site.baseurl }}"> <span class="tooltip"> <i class="fa fa-rss"></i> Subscribe!</span></a>
  <div class="inner">a
   <section class="copyright">All content copyright <a href="mailto:{{ site.email}}">{{ site.name }}</a> &copy; {{ site.time | date: '%Y' }} &bull; All rights reserved.</section>
   <section class="poweredby">Made with <a href="http://jekyllrb.com"> Jekyll</a></section>
  </div>
</footer>



[sumerian]:      https://docs.sumerian.amazonaws.com/tutorials/create/intermediate/augmented-reality-using-sumerian-arkit/
