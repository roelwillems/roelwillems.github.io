---
layout: post
title: "Changing the default colors of the Micro.blog Marfa theme"
microblog: false
audio: 
date: 2018-04-15 22:01:51 +0200
guid: http://roelwillems.micro.blog/2018/04/15/i-switched-my.html
---
I switched my theme for this microblog to Marfa.

Marfa is a new theme for [Micro.blog](https://micro.blog) hosted websites. I really like the theme but wanted to give it a small personal touch by changing the default color for links. 

The default is light red/pink(ish) but changing quite easy. 

Using the edit CSS functionality of Micro.blog you can overwrite the default colors by pasting the code above and change the colors to your liking.

```CSS
nav.main-nav a.cta {
	background: #fff;
	color: #ee4792;
	border: 2px solid #fcdae9;
}

nav.main-nav a.cta:hover {
	background: #fcdae9;
	color: #ee4792;
}

nav.main-nav a, #footer a, #post-nav a, p a{
   box-shadow: inset 0 -2px 0 #fcdae9;
}

nav.main-nav a:hover, #footer a:hover, #post-nav a:hover, p a:hover {
	box-shadow: inset 0 -25px 0 #fcdae9;
}
```
_`#fcdae9` is for underline and shading of the links. The `#ee4792` color is for the “Also on Micro.blog” text in the upper right button._
