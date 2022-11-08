---
created: 2022-10-29T10:20:34 (UTC -07:00)
tags: [tumblelog,blog,tumblog,tumbler,tumblr,tlog,microblog]
source: https://www.tumblr.com/gardenofroseandthorn/638786638132248576?source=share
author: 
---

# Garden of Rose and Thorn on Tumblr

> ## Excerpt
> I said it in the notes on the last post but I’m gonna say it again.

I’m married to someone with severe memory problems. Automation of household appliances & systems helps him a lot and helps me a lo…

---
Can confirm, Home Assistant is amazing; I transitioned everything I could for it to control and right now that’s literally everything. It can also be integrated with other voice-activated smart speakers than Alexa as well as Alexa. It also comes WITH an Add-on called Ada for voice.  So far, there is very goddamn little on the market that isn’t either officially supported or community supported and stuff is being added at the rate of literally weekly. If you do scripting and have a taste for diy, you can be Dr. Doom and your home is your supervillain lair.

Because of the market, most smart appliances and devices are Alexa enabled, but unless they’re made by Amazon, that doesn’t mean they’re Alexa exclusive and even then, someone is hacking their way into the API and pulling the endpoints. Right now, the only thing I can’t work in here (yet) is my Nest Thermostat and HA is working on adding that back in right now.

Home Assistant is fully compatible with the zwave and zigbee standards as well as wifi and bluetooth; you can directly control zwave and zigbee items or link up your existing hubs for it to control like SmartThings.

It can be run in several ways; I’ve done it on a Pi 4 both 4G and 8G and a VM on my Ubuntu server and while the Pi is recommended--I recommend it too for convenience--it’s one of several possibilites.  Currently I’m using a Raspberry Pi 4b 8G with a solid state hard drive instead of SD card.  You can purchase z-wave and zigbee modules to add to it for direct control of z-wave and zigbee devices or use your existing hubs (or both). Beneath the HA umbrella is also links to the blueprints of building your own zigbee and zwave devices with Arduino just to start that HA can also control. I’m not saying you’re going to be building your own smart thermostat on the weekend, but apparently, some people are doing just that.

This does not require a high tech start value; most integrations are automatic, you just say yes and login and let it happen, it even creates your Dr. Doom dashboard with TABS.

Again, you DO NOT NEED TO KNOW ANYTHING BUT COMPUTERS EXIST AND HOW TO CLICK YES AND NO TO USE THIS. For me, it was actually easier than a lot of setups with shit I had to pay money for that said they were easy.  This is open source, but that is not synonymous with user unfriendly; a lot of work was done to make this accessible to the casual automation user. The UI is card based; when you first start, HA does it all for you and creates discrete cards that control different things on your dashboard; no effort on your part, you can turn on and off any light in here or turn them red while someone is in the bathroom because that’s fucking funny.  But as you get more comfortable, you can start to create your own configurtions, take direct control of the UI, and mix it up; it’s up to you.

But.

If you are a DIYer or just want to be or never knew you wanted to be but feel the vibes and need a place to start, this is the perfect sandbox for learning and escalating.  There are a metric ton of tutorials, community add-ins, and message boards to consult. If you can imagine it, it can be done and its likely someone is working on version eight right now. The primary languages are python and javascript with yaml for configuration files for DIY.  You can create your own layouts, your own sensors, and your own cards if you don’t like what they have. If you’re like me, you may also go in to community addins and add new stuff to their code so it runs like you want it to; it’s all up to you.

I am not a dev pro, I’m a QC analyst with a scripting hobby; I do this quite literally for fun on weekends or when I’m bored or anxious and need to soothe myself with coding.

Here is the home page of my MULTI-TAB dashboard. Yes, that is a floorplan of my apartment and those glowy orange and dark grey bits are things that I can turn on and off from the comfort of my bed.  It’s fun.

I seriously would kill to get more people into this and have someone to play with and enjoy the feeling of controlling all within my (apartment) kingdom with but a single command.  Dear God tell me if you’re into it; we’ll be best friends and hopefully you’ll be okay with that.

Here’s an intro to Home Assistant I wrote back in September in DW when I first started, with screenshots.  You’ll also be able to see my Dash when I first started compared to the dash above. Feel free to ask me anything from the perspective of someone not a dev professional, an engineer, or even has a degree in anything, much less anything like this, and yet is a QC lead who codes their own testing tools and for whom this is just something cool and fun.
