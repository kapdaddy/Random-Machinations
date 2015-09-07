---
layout: post
title: Working Pictures Hosted on S3 and Centered
---

I was going to call this post something along the lines of "Woohoo! We have pictures" but thought it would make more sense if I tried to express what was going on. In my last post ["Krispy Kreme Peanut Butter"](http://www.randommachinations.com/2015/09/03/krispy-kreme-peanut-butter/) I was trying out getting images on my site here.

The S3 part was pretty straightforward; I've been using Amazon S3 for a while now to store files and whilst I'm loving using GitHub pages I felt it would be taking advantage if I tried to put all my images there. 

I use the AWS S3 web interface to create and manage buckets. I've created a couple of new buckets for my sites and simply upload my images, set them as public (or change the permissions for "Everyone" to "Open/Download") and use the link as the image source.

The tricky part for me was getting the images to look right on the website. I've always used Wordpress, which had little buttons that came up when you inserted an image into a post to change the alignment, but now that I'm blogging like a hacker I need to do things myself and actually try to understand how and why things work. So I discovered that using "align=center" was deprecated to use the HTML for the content and CSS for the presentation.

I added a little code to the stylesheet like this:

	/* Centered Images */
	img.centered {
	display: block;
	margin-left: auto;
	margin-right: auto}
	
And then to insert the image I wrote:

	<img class="centered" src="https://s3-eu-west-1.amazonaws.com/kapdaddy/20150902.jpg" alt="Krispy Kremes" width="300px" >
	
And there you have it! Centered images and peanut butter krispy kremes!
