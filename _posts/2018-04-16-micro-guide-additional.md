---
layout: post
title: "Micro guide: Additional steps and recommendations when using Cloudflare for your DNS"
microblog: false
audio: 
date: 2018-04-16 21:19:43 +0100
guid: http://roelwillems.micro.blog/2018/04/16/micro-guide-additional.html
---
[Cloudflare](https://www.cloudflare.com/) users wanting to use a custom domain name for their hosted Micro.blog will be greeted by a ```“custom domain isn't pointing to the micro.blog"``` error message when trying to save the custom domain. 

Luckily there is a work around:

## How to get your custom domain working _with_ Cloudflare
1. First follow the steps as outlined above and add the proper “A” and/or “CNAME” records to the Cloudflare DNS panel;
2. Before adding the custom domain to your Micro.blog account make sure that the “DNS and HTTP proxy (CDN)”  (orange cloud-icon) is disabled and set to bypass (grey cloud icon with the hover text “DNS only”);
3. After updating your DNS records and Cloudflare set to bypass for the “A” record and/or “CNAME” go to “Account” on Micro.blog  and fill hostname (e.g. yourdomain.com) that you’d like to use for your Micro.blog;
4. Micro.blog should save and enable to custom domain without issues. _If you get a message “custom domain isn't pointing to the micro.blog"_ make sure that you have set Cloudflare on bypass and wait for a few more minutes (the DNS change can take some time to get in effect);
5. After successful saving the custom domain you can re-enable Cloudflare functionality on your domain/Micro.blog by remove the bypass, make sure that the cloud-icon is set to orange (hover text should state: “DNS and HTTP proxy (CDN)”).

_So there you have it, you are able to use  Cloudflare (DNS/CDN/security/caching/DDOS protection) with hosted Micro.blogs, with some  additional steps to get the initial setup working._


## Some additional recommendations: 

### Using Cloudflare to redirect www. to root domain
If you would like to enable www. and root version of your custom domain it’s advisable to redirect one to the other (to make sure that there isn’t any duplicated content). Cloudflare can redirect the www. version to the root domain:
1. Go to “Page rules” within your Cloudflare account;
2. Create a page rule;
3. Add \<www.yourdomain.com\>/\* within the first field (“If the URL matches”); 
4. Under “Then the settings are:” select “Forwarding URL”, “ 301 - Permanent redirect”;
5. Add: \<yourdomain.com\>/$1 to the destination URL field;
6. Save and deploy the page rule for the redirect to take effect.

### Cloudflare, SSL and your Micro.blog
You should not use the SSL functionality provided by Cloudflare (email help@micro.blog to enable SSL). 
