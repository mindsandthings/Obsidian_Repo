---
created: 2022-10-19T14:10:05 (UTC -07:00)
tags: []
source: https://danielcompton.net/apple-m1-displaylink-multiple-display
author: 
---

# Understanding DisplayLink, multiple displays, and M1 Macs – Daniel Compton

> ## Excerpt
> Introduction I needed to buy a new Mac recently. I couldn’t bring myself to buy a legacy Intel Mac, but the new M1 Macs only support up to two displays. For the MacBook Air, MacBook Pro, and iMac that means you can connect one additional display along with the built-in display. For the Mac Mini, you can add two displays. I wanted a MacBook Air and already had two external displays which I wanted to keep using.

---
## Introduction

I needed to buy a new Mac recently. I couldn’t bring myself to buy a legacy Intel Mac, but the new M1 Macs only support up to two displays. For the MacBook Air, MacBook Pro, and iMac that means you can connect one additional display along with the built-in display. For the Mac Mini, you can add two displays. I wanted a MacBook Air and already had two external displays which I wanted to keep using.

**Update:** I ended up purchasing the ALogic DX3 and wrote a [follow-up post](https://danielcompton.net/2021/10/19/displaylink-alogic-dx3-review) about my experiences with it.

## DisplayLink

What are your options if you want to run more than two displays? Enter [DisplayLink](https://www.displaylink.com/). DisplayLink (not to be confused with DisplayPort) is the name of a technology created by a company also named DisplayLink. It lets you send a video signal to a display over USB or Wi-Fi instead of via DisplayPort or HDMI. DisplayLink technology was first used in laptop docking stations but can now be found in [other video-related products](https://www.displaylink.com/products) including adapter cables and monitors.

DisplayLink has two components - a software driver installed on your computer and a hardware chip in the dock or adapter. The software driver presents itself as one or more displays to the computer. The computer sends pixel data to the software driver, which then compresses the data and sends it over USB. The DisplayLink chip decompresses the data and sends the display signal to the (real) display.

I was pleasantly surprised to see that [DisplayLink’s drivers](https://www.displaylink.com/downloads/macos) have been updated for Apple Silicon and don’t require a kernel extension. From what I can tell, DisplayLink seems to be publishing regular updates to their drivers and is actively working on new features.

## DisplayLink Limitations

Sending compressed video over USB is a pretty neat trick! However, DisplayLink has quite a few downsides to be aware of.

An uncompressed 4K60 video signal requires 12 Gbps of bandwidth. The latest [DisplayLink chips](https://www.displaylink.com/integrated-chipsets/dl-6000) run over USB 3.0 which has a bandwidth of 5 Gbps. Even a single 4K signal is too big, let alone multiple displays. This is why DisplayLink needs to compress the captured screen.

For desktop browsing, email, software development, and other general computer tasks where the display doesn’t change much from frame to frame, DisplayLink compression can be very efficient and is unlikely to be noticeable. DisplayLink [claims](https://www.displaylink.com/integrated-chipsets/dl-6000) “Pixel-perfect graphics”, and “Compression tuned for video content and high-quality graphics” on their newer chipsets. If you’re a video/photo/graphics professional, you’d probably want to check and see if this works for you.

It doesn’t sound like it will be as good for [gaming though](https://www.displaylink.com/small-office/faq#headingTwelve):

> While DisplayLink technology is targeted primarily to productivity and video applications, it is suitable for the casual gamer. If you’re a “power gamer”, looking for every edge possible over your opponents, you might want to go another route.

Another downside to DisplayLink is that you need to install an optional [program](https://support.displaylink.com/knowledgebase/articles/1932214-displaylink-manager-app-for-macos-introduction-in) to show the Lock Screen on a DisplayLink monitor. Otherwise, the Lock Screen will only show up on the built-in display.

Unlock with Apple Watch [doesn’t work](https://support.displaylink.com/forums/287786-displaylink-feature-suggestions/suggestions/35524279-support-for-unlock-with-apple-watch) when using DisplayLink. Apple disables Unlock with Apple Watch with the message “Unlocking with Apple Watch is not available while your screen is being shared”.

DisplayLink has a few other limitations on Macs: HDCP is not supported so you may not be able to watch Netflix, Hulu, iTunes Movies, etc.; only 4 external displays are supported; screen rotation is not supported; Clamshell mode is [partially supported](https://support.displaylink.com/knowledgebase/articles/1963276). Manufacturers publish [blog posts](https://us.targus.com/blogs/discover-targus/targus-validates-displaylink-manager-release-1-3-for-big-sur-catalina-and-m1-macbooks) announcing that new DisplayLink drivers are validated with their hardware, it’s probably good to check with your manufacturer before updating.

There are quite a few limitations to using DisplayLink to extend your displays. However, it’s also currently the only way to run more than two displays on a Mac, so if you need that then you’ll need to look at a DisplayLink powered Dock.

## Choosing a Dock

If you already have a dock without DisplayLink, your cheapest option may be to purchase a DisplayLink USB adapter. You could connect your monitor to the adapter, and then the adapter to a free USB port. DisplayLink keeps a list of [USB adapters](https://www.displaylink.com/products/usb-adapters) you can purchase. Check compatibility as not all adapters list support for macOS, although sometimes the reviews will mention that they do still work.

DisplayLink sells chipsets to dock manufacturers. The chipset has their DisplayLink hardware, along with other ports like USB, Ethernet, Audio. This means that products from different manufacturers like Targus, Dell, Alogic, Plugable, Kensington can end up with very similar capabilities because they are all using the same electronics.

Unfortunately, all of the M1 compatible docks I saw had a maximum of one USB-C port. If you have a lot of USB-C devices you’ll either need to purchase USB-A->USB-C adapters or buy a non-DisplayLink dock and a DisplayLink adapter.

If you’re investigating docks, you may see reference to [USB-C Alternate Mode](https://blog.startech.com/post/tech-talk-using-usb-c-and-displayport-over-alt-mode/). This is a way for a USB-C port to run non-USB signals over it like DisplayPort and Thunderbolt(!). Alternate Mode doesn’t let you run any more displays than you could otherwise do natively.

## Dock Options

If you’re looking for a list of DisplayLink docks, DisplayLink has a [list](https://www.displaylink.com/products/universal-docking-stations) of DisplayLink docks. Here’s a list of docks that the manufacturers have said are supported on M1 Macs as a starting point:

**[Plugable](https://plugable.com/blogs/news/we-ve-tested-the-new-m1-powered-macbooks-here-s-the-compatibility-info-users-need-to-know)** has a few options:

-   [UD-3900PDZ](https://plugable.com/products/ud-3900pdz/), $160 - 3 HDMI ports, 1 supports 4K30, the other 2 only support 1080p/60Hz. 60W Power Delivery, 6 USB-A 3.0 ports, 3.5mm audio jack.
-   [UD-ULTC4k](https://plugable.com/products/ud-ultc4k/), $220 on [Amazon](https://www.amazon.com/dp/B0779K9DG2?ref_=maas_adg_48E4E5794A8CD3A8AE8DAFFE8060A81C_afap_abs) - 2 DisplayPort ports that support 4K60 over DisplayLink, 1 HDMI port that supports 4K30. 60W Power Delivery, 4 USB-A 3.0 ports, 1 downstream USB Type-C port, 3.5mm audio jack.

Note that Plugable mentioned that their Ethernet ports are limited to 300Mbps on macOS due to driver issues. I’m unsure if that extends to all DisplayLink docks.

**[Alogic](https://www.alogic.co/business/blog/post/understanding-dual-triple-external-displays-with-apple-s-m1-macs)** also has a few options:

-   [DX3](https://www.alogic.co/alogic-triple-4k-display-universal-docking-station-dx3-with-100w-power-delivery.html), $250 on [Amazon](https://www.amazon.com/ALOGIC-Universal-Charging-DisplayPort-Ethernet/dp/B0924789ZC) - 3 DisplayPort ports with DisplayLink, 100W Power Delivery, 3 USB-A ports, 1 USB-C port, Micro SD and SD card reader, Gigabit Ethernet port, 3.5mm audio jack.
-   [DX2](https://www.alogic.co/dual-4k-display-universal-docking-station-dx2-with-65w-power-delivery.html) - 2X DisplayPort ports, 65W Power Delivery, 3 USB-A ports, 1 USB-C port, Micro SD and SD card reader, Gigabit Ethernet port, 3.5mm audio jack.
-   [Universal Twin HD](https://www.alogic.co/product-solutions/browse-by-category/usb-c-products/usb-c-docking-stations-2/alogic-universal-twin-hd-docking-station-with-usb-c-usb-a-compatibility-dual-display-1080pat60hz.html)

**[Targus](https://us.targus.com/blogs/discover-targus/displays-for-m1-macbook)** has several docks with DisplayLink:

-   [DOCK190](https://us.targus.com/products/usb-c-universal-dv4k-docking-station-with-100w-power-dock190usz), $310 - 2 DisplayPort/HDMI ports (only 2 video ports can be used at the same time), 100W Power Delivery, 4 USB-A, 1 USB-C, Gigabit Ethernet, 3.5mm audio jack. Thunderbolt alt mode is supported.
-   [DOCK570](https://us.targus.com/products/usb-c-universal-quad-4k-docking-station-100-watt-power-delivery-dock570usz), $415 - 4 DisplayPort/HDMI Ports, 4 USB-A, 1 USB-C, Gigabit Ethernet, 3.5mm audio jack. Thunderbolt alt mode is supported.

**[Kensington](https://www.kensington.com/en-nz/news-index-blogs-press-center/docking-connectivity-blog/how-to-connect-more-than-one-display-to-an-apple-m1-macbook/)** has four docks with DisplayLink:

-   [SD4700P](https://www.kensington.com/p/products/device-docking-connectivity-products/laptop-docks-usb-accessories/sd4700p-usb-c-usb-a-5gbps-dual-2k-hybrid-dock-60w-pd-dp-hdmi-winmac-taa/), $250 - 1 DisplayPort, 1 HDMI port (both limited to 2K resolution), 60W Power Delivery, 5 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack. Supports up to 5Gbps.
-   [SD4750P](https://www.kensington.com/p/products/device-docking-connectivity-products/laptop-docks-usb-accessories/sd4750p-usb-c-usb-a-dual-4k-hybrid-docking-station-w-85w-pd-dp-hdmi-winmac/), $290 - 2 DisplayPort/HDMI ports up to 4K60, 85W Power Delivery, 5 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack. Supports up to 5Gbps.
-   [SD4780P](https://www.kensington.com/en-nz/p/products/connectivity/universal-laptop-docking-stations/sd4780p-usb-c-usb-a-10gbps-dual-4k-hybrid-docking-station-w-100w-pd-dphdmi-winmacchrome/) - 2 DisplayPort/HDMI ports up to 4K60, 100W Power Delivery, 5 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack. Supports up to 10Gbps.
-   [SD4900P](https://www.kensington.com/p/products/device-docking-connectivity-products/laptop-docks-usb-accessories/sd4900p-usb-c-and-usb-a-10gbps-triple-4k-hybrid-dock-60w-pd-dp-hdmi-winmacchrome/) $320 - 3 DisplayPort/HDMI ports up to 4K60, 60W Power Delivery, 5 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack. Supports up to 10Gbps.

[StarTech](https://blog.startech.com/post/apple-m1-silicon-fully-compatible-with-startech-com-products/) has 4 docks with DisplayLink:

-   [DK30CH2DEP](https://www.startech.com/en-us/cards-adapters/dk30ch2dep) - 2 DisplayPort (4K60), 1 HDMI port (4K30), 100W Power Delivery, 4 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack.
-   [DK30C2DPEP](https://www.startech.com/en-us/cards-adapters/dk30c2dpep) - 2 DisplayPort/HDMI (4K60), 100W Power Delivery, 3 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack.
-   [DK30C2DPPD](https://www.startech.com/en-us/cards-adapters/dk30c2dppd) - 2 DisplayPort/HDMI (4K60), 60W Power Delivery, 3 USB-A, 1 USB-C, 1 Gigabit Ethernet, 3.5mm audio jack.
-   [DK30CHDDPPD](https://www.startech.com/en-us/cards-adapters/dk30chddppd) - 1 DisplayPort (4K30), 1 HDMI (4K30), 60W Power Delivery, 4 USB-A, 1 USB-C, SD Card slot, 1 Gigabit Ethernet, 3.5mm audio jack.

Dell has some docks with DisplayLink technology, but they don’t list compatibility with Macs, so probably safest to avoid them unless you’re able to try them first.

[Caldigit docks](https://www.caldigit.com/docks/) are highly regarded but don’t contain DisplayLink chips. This means [you can’t run multiple displays](https://www.caldigit.com/apple-silicon-mac-and-caldigit-dock-compatibility/) on them. However, they seem to work if you only need a single external display on an M1 Mac, or purchase a USB display adapter. There is a [video](https://www.youtube.com/watch?v=Kq_FyjcAULA) of someone using a Caldigit TS3 Thunderbolt dock with 4 DisplayLink USB adapters.

## Disclaimer

I’m not an expert on any of this, I’ve just read a lot and compiled it into one place. Please let me know if I’ve missed something or if you have any suggestions.

## Summary

There are lots of moving parts involved with picking a USB-C dock, let alone one also running DisplayLink. You need one which:

-   Supports DisplayLink.
-   Supports the number of displays you have, at the resolution and refresh rate you want.
-   Has enough USB ports to support other peripherals, or is reliable enough to add a USB hub.
-   Supports USB Power Delivery with your laptop, with enough wattage.
-   Has enough bandwidth for all your devices.
-   Doesn’t have audible fan noise.
-   Works reliably and doesn’t cause other issues.

As you can tell from the number of limitations mentioned throughout this post, picking a dock that works with your setup is far from a simple task. I recommend checking the specs closely, checking out reviews, and ideally trying it out at home before committing.
