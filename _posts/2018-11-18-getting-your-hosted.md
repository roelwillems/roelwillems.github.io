---
layout: post
title: "Micro guide: Getting your hosted Microblog IPv6 ready"
microblog: false
audio: 
photo: 
date: 2018-11-18 09:20:11 +0100
guid: http://roelwillems.micro.blog/2018/11/18/getting-your-hosted.html
---
This is a small guide (hence the category ["micro guide"](https://roelwillems.com/micro-guides/)) to enable IPv6[^1] for your hosted microblog[^2].

*disclaimer: please make sure that you know what you are doing with your DNS settings. Although it isn't really difficult or complex you can really mess up access to your website if the settings are incorrect. Please make note of the original settings before changing anything.*

### Setting up IPv6
To start, you should go to your domain registrar or system to manage DNS (personally I use [Cloudflare](https://www.cloudflare.com) and have written another micro guide with recommendations on how-to [enable Cloudflare for your microblog](https://roelwillems.com/2018/04/16/micro-guide-additional.html)).

Now you can create an AAAA record (a record is an instruction for the browser to which server to connect and the AAAA version is used for IPv6 addresses). 

Make sure that the AAAA record is pointing to: 

    2600:3c00:1::68c8:16d6

This is the IPv6 address for hosted microblogs.
Leave the A record (address for IPv4) and other records like CNAME unaltered. Based on you DNS provider it should look somewhat like:

![example of DNS records](https://roelwillems.com/uploads/2018/99b7b82333.png)

Save the settings and after a few minutes you can [check if your website has support for IPv6](https://www.internet.nl).

[^1]:What IPv6 is and why it is beneficial will get technical very quickly, if your interested you could start reading [Wikipedia](https://en.wikipedia.org/wiki/IPv6) or look in to this [tutorial](https://www.tutorialspoint.com/ipv6/)
[^2]:hosted with [micro.blog](https://micro.blog)
