---
created: 2022-10-19T12:24:33 (UTC -07:00)
tags: []
source: https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html
author: Author: Simon Jary, Contributing writer
---

# How to connect two or more external displays to an Apple Silicon M1 and M2 Mac | Macworld

> ## Excerpt
> Get around Apple's annoying M1 Mac single-display limitation via software and adapters

---
Apple’s range of MacBooks that use the company’s own Silicon M1 or M2 processors cannot natively connect more than one external monitor, which is a massive limitation on the previous Intel-based generation of Mac laptops that could run two displays when connected to a USB-C or Thunderbolt 3 docking station or hub.

The M1 Pro and M1 Max do support multiple external displays, so owners of these Mac laptops can relax.

We hoped the M2 would lose the M1 limitation, but it survives on the plain M2; when available, expect the M2 Pro and M2 Max to support more displays, just like their M1 siblings.

**M1 MacBook Air**: Maximum one external display

**M2 MacBook Air**: Maximum one external display

**M1 MacBook Pro**: Maximum one external display

**M1 Pro MacBook Pro**: Maximum two external displays

**M1 Max MacBook Pro**: Maximum three external displays

However, there are ways around this plain M1/M2 limitation, allowing you to run two external displays off an M1/M2 MacBook, which we will outline here. There’s a software driver plus dock workaround and a hub/adapter workaround. 

With the software workaround, there are some risks involved as you will be required to install third-party drivers, and these might later be unsupported by future updates of the macOS. And you will likely have to buy at least one adapter, where previously a dock plus a display cable per external screen would have sufficed.

The hardware solution involves a dual-HDMI adapter that requires a little tinkering in System Preferences at setup.

If you waited for Apple’s latest [14in or 16in M1 Pro M1 Max MacBook Pro](https://www.macworld.com/article/668162/14in-macbook-pro-vs-16in-macbook-pro-2021.html) models, you are in luck as these laptops do support multiple external displays. Laptops with the M1 Pro can connect to up to two external displays with up to 6K resolution at 60Hz, while MacBooks with the M1 Max can connect to three external displays with up to 6K resolution and one external display with up to 4K resolution at 60Hz.

M1/M2 owners, start saving for a new MacBook Pro or read on.

## External displays: big problem for M1 and M2 Macs

Apple’s Mac mini, MacBook Air, and MacBook Pro 13in were the first Macs to feature the Apple-designed M1 CPU. They received rave reviews for their speed improvements over Intel-based laptops, including here on Macworld.

See our comparison of the [13in MacBook Pro (M1) vs MacBook Pro (Intel)](https://www.macworld.com/article/668067/13in-macbook-pro-m1-vs-macbook-pro-intel.html) and [MacBook Air (M1 Silicon) vs MacBook Air (Intel)](https://www.macworld.com/article/668061/new-macbook-air-m1-silicon-vs-macbook-air-intel.html). We have also looked at the differences between the [Mac mini (M1) and Mac mini (Intel)](https://www.macworld.com/article/668063/mac-mini-m1-vs-mac-mini-intel.html), and look at what we can expect from the [new M2 Macs](https://www.macworld.com/article/678349/new-macbook-pro-2022-with-m2-could-be-coming-soon.html).

But if your MacBook setup includes running more than one external display, you have a major problem. Apple’s M1 or M2 chips simply won’t consider it—at least natively.

Apple states in the M1 and M2 MacBook Air and MacBook Pro tech specs that they support only “one external display with up to 6K resolution at 60Hz”.

![Apple M1 and M2 Display Support tech specs](https://b2c-contenthub.com/wp-content/uploads/2022/06/Apple-M1-M2-Display-Support-tech-specs.jpg?quality=50&strip=all)

Apple

While the M1 and M2 MacBooks natively support just one monitor, the M1 Mac Mini does natively support up to two external monitors—one via the HDMI port and a second via USB-C. But the M1 models of the MacBook Air and MacBook Pro support only one external display.

Apple has apparently [promised to fix the problem](https://www.macworld.com/article/675911/apple-promises-to-fix-external-monitor-problems-with-m1-macs.html) in a future macOS update, but the arrival of the later M1 Pro and M1 Max—and more recently the M2—suggest that M1 owners could be waiting a long time. We have this guide to [Monitors for M1 Macs and what you need to know before buying.](https://www.macworld.com/article/677287/monitors-for-m1-macs-what-you-need-to-know-before-buying.html "Problems with displays for M1 Macs ") We also cover the basics of [how to connect your Mac to an external monitor](https://www.macworld.com/article/671793/how-to-connect-an-external-monitor-to-your-mac.html).

## Workaround #1: install DisplayLink software drivers

You can use a combination of display technologies to get around the M1/M2 MacBooks’ single-monitor limitation. This should work with most third-party docks, although some manufacturers, such as Caldigit, don’t recommend it.

For example, Plugable’s multi-display docks use a combination of native USB-C Alternate Mode (native “Alt Mode” video output) and DisplayLink technology. This combination serves as a workaround to the M1/M2 platform supporting only a single external display via USB-C.

Note that DisplayLink requires a third-party driver to be installed on the Mac. There are different versions of the DisplayLink driver, and some bring their own compromises to the party.

The DisplayLink macOS app or DisplayLink Manager app are ways of enabling DisplayLink technology on macOS. The app is available as a [standalone installer](https://go.redirectingat.com/?id=111346X1569486&url=https://www.synaptics.com/products/displaylink-graphics/downloads/macos&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html) rather than through the mac App Store.

![Plugable UD-ULT4K dock M1 Mac](https://images.macworld.co.uk/cmsdata/features/3799794/plugable-ud-ultc4k-usb-c-dock.jpg)

Plugable docking station and three external displays via DisplayLink.

**1.** First, download the latest [Mac DisplayLink driver](https://go.redirectingat.com/?id=111346X1569486&url=https://www.displaylink.com/downloads/macos&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html).

DisplayLink Manager Graphics Connectivity App v. 1.7.0 is compatible with macOS Catalina 10.15, macOS 11 Big Sur and macOS 1dis
2 Monterey. It can be managed via the DisplayLink icon in the Apple Menu bar.

The macOS requires the user to permit “Screen Recording” in order for DisplayLink devices to work properly. This can be found in System Preferences under Privacy in Security & Privacy; navigate to Screen Recording in the list on the left, then tick the Screen Recording permission for DisplayLink Manager after unlocking the padlock using your admin password. You may need to quit and restart DisplayLink Manager afterwards.

More in-depth details on DisplayLink Manager under macOS Big Sur, Catalina and Monterey, in this [DisplayLink support page](https://go.redirectingat.com/?id=111346X1569486&url=https://support.displaylink.com/knowledgebase/articles/1932214-displaylink-manager-app-for-macos-introduction-in&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html).

Installation is straightforward. Older versions did not support laptops’ closed-display/Clamshell mode, but 1.7.0 does support Clamshell mode if the MacBook is Intel-based running macOS 12 or if the MacBook is M1-based running macOS 11 or 12.

Other limitations include incompatibility with display rotation. Rotation on Apple M1/M2 requires DisplayLink Manager 1.6+ with macOS 12+.

There’s an option in DisplayLink manager to “launch at startup”, or you can drag the DisplayLink Manager to your Login Items in Users & Groups.

**2.** Then connect the MacBook to a dock.

**3.** For the first screen you can connect via the dock’s DisplayPort or HDMI Port, and this will be handled natively by the M1/M2 MacBook.

You could also connect the first external display via the dock’s other display ports or via a Thunderbolt or USB-C to HDMI or DisplayPort adapter.

The HDMI or DisplayPort output uses Alternate Mode (Alt Mode), and as it is basically a pipeline directly to the system’s native GPU, it will behave just like if you hooked up a USB-C to HDMI dongle to your laptop. This requires no user driver installation.

The second and third displays will rely on the DisplayLink software. DisplayLink uses an installed driver and the system CPU and GPU to convert graphics data on the system into data packets. That data is then sent over the cable as data packets, and converted back to video information and output to the monitors via the DisplayLink chip in the docking station.

![Baseus 17-port dock and three screens with M1 Mac](https://b2c-contenthub.com/wp-content/uploads/2022/09/Baseus-Three-Screen-USB-C-Dock-Screens.jpg?quality=50&strip=all)

Baseus docking station with M1 MacBook Air and three external displays via DisplayLink.

IDG/Foundry

## Which docks support DisplayLink?

Originally, dock manufacturers did not officially supported such a DisplayLink setup for Macs. The solution works, but they warned that this could become unstuck in future versions of the macOS.Whenever there is a new OS update the drivers may need to be updated each time.

However, after some recent testing and improvements Plugable has updated its compatibility to officially support that configuration. For Mac compatibility it has validated both Apple and Intel platforms running at least macOS 11. For M2, the company does anticipate compatibility but is awaiting new M2 MacBooks for testing and validation.

Learn more about the [best Thunderbolt docking stations](https://www.macworld.com/article/668894/best-thunderbolt-3-4-and-usb-c-docking-stations-for-macbook-pro-and-air.html) for more details, or you can connect via a simpler [USB-C hub](https://www.techadvisor.com/test-centre/pc-peripheral/usb-c-hubs-3683402/). Look for a dock with two or more display ports, preferably ones that can connect to your preferred displays without the need for an adapter. Some, such as the Anker Apex, have two display ports but Anker warns against using it with Macs, even though DisplayLink should work around the problem.

[Thunderbolt 4 docks or hubs](https://www.techadvisor.com/article/725034/best-thunderbolt-4-and-usb4-hubs-and-docks.html) often have no dedicated display port but three available TB4 ports that can be used to connect directly to a USB-C display or via adapters to HDMI or DisplayPort monitors. While you may have to buy an adapter cable, 40GBps Thunderbolt 4’s port flexibility and backwards compatibility are recommended for users of modern Macs such as the M1 and M2 MacBooks.

Docking station and hub manufacturers are now actively marketing their products as solutions to the M1/M2 external display limitation. Each requires the DisplayLink download but no further hardware adapter except for the dock or hub itself. And of course these hubs offer the usual multi-port benefits as well as the external monitor solution.

Note that the three listed (and tested) below use USB-C rather than Thunderbolt, so don’t benefit from the MacBook’s potential 40Gbps data bandwidth.

Read our [**Ugreen USB-C Triple Display Dock review**](https://www.techadvisor.com/article/1094467/ugreen-usb-c-triple-display-dock-review.html) for full details on how to use this quality compact docking station to support up to three external displays on a plain (non-Pro or -Max) M1/M2 MacBook. Priced at $329/£369, it features two HDMI ports and a DisplayPort and can support three 4K displays at 60Hz on a Mac. There are 12 ports in total, including Gigabit Ethernet, card readers and 10Gbps USB-A and USB-C ports. It connects to the MacBook via 10Gbps USB-C.

The **EZQuest Ultimate Plus USB-C Multimedia Hub** has two HDMI ports and a VGA port, and supports one 4K at 60Hz and one 4K at 30Hz via HDMI and 1080p HD via VGA. It also features 5Gbps USB-A ports, Gigaboit Ethernet and card readers. Like the Ugreen dock, it requires a USB-C charger for power and can passthrough up to 85W to the connected MacBook, but connects via slower 5Gbps USB-C. Available at [EZQuest](https://go.redirectingat.com/?id=111346X1569486&url=https://ezq.com/dual-hdmi-usb-c-multimedia-hub-adapter-12-ports.htm&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html) for $169 and [Amazon UK](http://buy.geni.us/Proxy.ashx?TSID=14156&GR_URL=https://www.amazon.co.uk/Designed-Ultimate-Multimedia-Gigabit-Ethernet/dp/B09TX1R1QT&asc_refurl=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html) for £150.

The **[Baseus 17-in-1 Docking Station](https://www.amazon.com/dp/B082R5S1MP?th=1?tag=macworld05-20&asc_refurl=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html)** ($135) has three HDMI ports, each of which can connect to an external 4K display at 30Hz. Its claim to have 17 ports is exaggerated slightly as one is for the external power supply that powers just the dock. and another to add power the dock via a USB-C charger and then onto the laptop. But it has 15 other ports including the upstream 5Gbps USB-C connection to the MacBook, plus Gigabit Ethernet, card readers and 5Gbps USB-A and USB-C ports. In Europe, it is available via [AliExpress](https://go.redirectingat.com/?id=111346X1569486&url=https://www.aliexpress.com/item/4000807652888.html&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html).

![USB-A 3.0 to display adapters](https://images.macworld.co.uk/cmsdata/features/3799794/usb-a-to-display-adapters.jpg)

If your hub or dock has just one display port, you could also attach a second or third display via one or more of the spare USB-A ports, using an adapter such as [StarTech.com USB 3.0 to HDMI / DVI Adapter](http://buy.geni.us/Proxy.ashx?TSID=14156&GR_URL=https://www.amazon.co.uk/HDMI-Monitor-External-Video-Adapter-Black/dp/B008CXFMT6&asc_refurl=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html). This costs £80 or US$80, so needs to be factored in when pricing an M1/M2 MacBook purchase if you require multiple monitors and want to use the USB-A port rather than a display port such as HDMI or DisplayPort. Another option is [Plugable’s USB Dual 4K Display Adapter](https://www.amazon.com/Plugable-DisplayPort-Monitor-Adapter-Compatible/dp/B08F2SZQYX?tag=macworld05-20&asc_refurl=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html).

This adapter turns an available USB-A 3.0 port into one DVI-I or VGA port (DVI to VGA adapter included) and one HDMI output. Each display can simultaneously support the maximum resolution of 2048×1152 at 60Hz. Make sure to use an active HDMI DisplayLink adapter that can support 4K at 60Hz, as some are limited to 4K at 30Hz.

![Hyperdrive Dual 4K HDMI 3-in-1 USB-C Adapter and M1 Mac with two external displays](https://b2c-contenthub.com/wp-content/uploads/2022/09/Hyperdrive-Two-Displays-M1-MacBook-Air.jpg?quality=50&strip=all)

Hyperdrive Dual 4K HDMI 3-in-1 USB-C Adapter and M1 MacBook Air with two external displays

IDG/Foundry

## Workaround #2: Use a special Dual HDMI adapter

Accessory maker Hyper sells two hardware solutions that allow you to add more than one display to an M1 or M2 Mac.

The **Hyperdrive Dual 4K HDMI Adapter for M1 MacBook** and **Hyperdrive Dual 4K HDMI 10-in-1 USB-C Hub** can extend to two HDMI displays: one at 4K 60Hz through HDMI and DP Alt-mode, and one at 4K 30Hz through HDMI and Silicon Motion’s InstantView technology.

Hyper says that these work “without having to download cumbersome drivers” but there is some software installation involved, and you need to allow InstantView access to your Privacy settings in System Preferences. You connect the hub or adapter to your M1 MacBook and find the HyperDisplay app that appears in a Finder folder sidebar. Double-click the macOS InstantView icon and follow the System Preferences instructions. Once this has been completed your MacBook will automatically recognise the adapter from then on.

The Dual 4K HDMI 3-in-1 USB-C Adapter ([$129.99](https://go.redirectingat.com/?id=111346X1569486&url=https://www.hypershop.com/products/hyperdrive-dual-4k-hdmi-adaptor-for-m1-macbook&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html)) features two HDMI ports and connects to your M1 Mac via its integrated USB-C cable. A further USB-C PD port allows you to charge the connected laptop at up to 100W—handy as the adapter itself uses up one of your M1 or M2 laptop’s two Thunderbolt ports.

A more fully fledged solution is the Dual 4K HDMI 10-in-1 USB-C Hub ([$199.99](https://go.redirectingat.com/?id=111346X1569486&url=https://www.hypershop.com/products/hyperdrive-dual-4k-hdmi-10-in-1-usb-c-hub&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html)), which boasts 10 ports, including the two HDMI ports and 100W PC port seen on the cheaper adapter, plus Gigabit Ethernet, 3.5mm Audio Combo Jack, SD and MicroSD UHS-I card readers, and two USB-A (5Gbps) ports. It too connects to the laptop via an integrated USB-C cable. Of the two, this multi-port hub is better value as you can use it as a dock when it’s connected to a decent [USB-C PD wall charger](https://www.techadvisor.com/test-centre/laptop/usb-c-power-delivery-chargers-3676400/).

Buy direct from [Hyper](https://go.redirectingat.com/?id=111346X1569486&url=https://www.hypershop.com/pages/hyperdrive-dual-4k-hdmi-usb-hub-and-adapter-for-m1-macbooks&xcust=1-1-675869-1-0-0&sref=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html). Shipping to the UK is currently a steep $66, so factor that in if you are not based in the US. Or buy the 10-in-1 hub for [$199.99](https://www.amazon.com/HyperDrive-Dual-HDMI-MacBook-10in1/dp/B09NBS9DS6?tag=macworld05-20&asc_refurl=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html) or [£219.99](http://buy.geni.us/Proxy.ashx?TSID=14156&GR_URL=https://www.amazon.co.uk/HyperDrive-Dual-HDMI-MacBook-10in1/dp/B09NBS9DS6/&asc_refurl=https://www.macworld.com/article/675869/how-to-connect-two-or-more-external-displays-to-apple-silicon-m1-macs.html) from Amazon.

![Hyperdrive Dual 4K HDMI adapter and Hub](https://images.macworld.co.uk/cmsdata/features/3799794/hyperdrive-dual-hdmi-adapter-hub.jpg)

## Workaround caveats

Whenever there is a new OS update DisplayLink drivers may need to be updated each time.

Plugable doesn’t recommend the workaround for gaming, video editing, digital audio workstations (DAWs), and protected-content (HDCP) playback. For these workloads, users will want the full throughput of a “bare-metal” native GPU connection—such as provided by the DisplayPort or HDMI port on the dock using Alt Mode.

Caldigit actively recommends against using DisplayLink, as it finds it unreliable and there would be no synergy between the driver and the dock. Because it requires a third-party driver, users are at the mercy of Apple and the third-party developer to support later versions, the company told Macworld.

However, this combination of display technologies does allow M1 and M2 MacBooks to run more than one external monitor, and the M1 Mac mini to run more than two. And more manufactuers are coming out with docks and hubs that support it.

The only risk is that it could stop working at any time, although it wouldn’t harm your system if it did, and you could simply uninstall DisplayLink.

DIsplayLink a workaround with a potentially limited timespan but the likelihood is that compatibility would be restored at some stage if the worst happened and you would get back your multi-monitor setup.

The Hyperdrive dual 4K HDMI hardware solution is the more expensive but stable workaround of the two—but if you want up to three displays you’ll need a dock such as the [Plugable USB-C Triple 4K Display Docking Station](https://www.techadvisor.com/article/721352/plugable-usb-c-triple-display-4k-docking-station-review.html) and the DisplayLink solution.

Read our [M1 MacBook Air review](https://www.macworld.com/article/668078/macbook-air-m1-2020-review.html) and everything you need to know about the [M2 MacBook Pro](https://www.macworld.com/article/678349/new-macbook-pro-2022-with-m2-could-be-coming-soon.html) and [M2 MacBook Air](https://www.macworld.com/article/676165/new-macbook-air.html).

If you are wanting to use a second display with your Mac and not have your Mac’s screen on, read our feature [How to turn a Mac’s screen off.](https://www.macworld.com/article/676437/how-to-turn-a-macs-screen-off.html "How to turn a Mac's screen off.")
