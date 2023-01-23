---
layout: single
title:  "Comcast, Verizon and T-Mobile Internet Service Compared"
date:   2023-01-17 13:17:00 -0500
categories: [boston, ISP, comcast, tmobile, verizon]
---

I've recently moved to a new location within the city of Boston and as
a result have needed to choose a new ISP. Sadly, service from my
previous, and well liked, ISP [Starry](https://starry.com) was not
offered at the new location.

So in this review I'll be looking at the three options that are
available to me in the new location at the time of writing. Listed in
the order in which I've installed them, they are:

### Comcast/Xfinity Cable

There's not much to say about Comcast that most people don't already
know. They are one of the US's least popular companies, which is why I
suppose they're rebranding themselves as Xfinity now. *You're not
fooling anyone, Comcast!*

I've used this company on and off over the years and my main problems
with them have been:

1. Creeping increases in montly rates. Seemingly at least every year,
   and without notice.
   
2. In areas where they have no competition their bandwidth is lower
   than in areas where they do, and they have data caps in at least
   some of those areas as well. While at a previous address in a large
   building they had paid the building management not to allow
   competition in the building. Once building management bowed to
   pressure from residents for alternative services, Comcast increased
   their bandwidth. Currently there are no data caps in the Boston
   (and I believe, the entire North East.)
   
That said, Comcast has been the the most reliable service I've
used. In the past I might have complained about their support people,
but the last time, and probably the only time, I've had to contact
Comcast support in the last 10 years, the woman on the other end of
the line was easily the best support person I'd ever spoken to at any
company.

I guess had some things to get off my chest about Comcast.

### T-Mobile 5G

I don't have much experience with this company so I don't have much to
say about it. The sales person suggested I'd likely get an order of
magnitude better bandwidth than T-Mobile advertised. "Oh yeah, you're
right in our sweet spot location wise", he said. It wasn't true of
course and I didn't expect it. I've been aware of a single service
interruption from T-Mobile in the five or so months I've been using
it, and that lasted only about two minutes.

### Verizon 5G

Even less to say about Verizon. I've had the service for about a week.

# Price

There's not much difference in the price for all three services at the
moment. 

| ISP      | Price/Month | Notes                                            |
|----------|------------:|--------------------------------------------------|
| Comcast  |      $39.00 | For the first two years, then 💰💰💰 most likely |
| T-Mobile |      $50.00 | Total, no extra fees                             |
| Verizon  |      $59.00 |                                                  |

Obviously Comcast is marginally less expensive at the moment but that
price is good only for two years, after which it more than doubles. I
can't remember what the actual price will be, probably around
$100/mo. which is really expensive for this level of service. I could
dig around on their site to find the post-intro price but I can't be
arsed becuase where that information is located is not at all obvious
and I'm sure it'll be higher when the time comes anyway.

As far as Verizon, I haven't been charged yet as I'm in their free
first month trial period. Given that it's a phone company though, I
expect plenty of inscrutable extra fees tacked on to the bill.

# Setup

Aside from Verizon I don't have much to say about setup for these
systems. It's all pretty standard and easy. Verizon, though, wants you
to glue their receiver to your window, apparently so it's as close as
possible to their transceiver outside on the street. I really didn't
want to do that and it turns out I didn't have to as it reports an
excellent signal strength despite it just sitting on a small table
near the window.

<iframe width="560" height="315" src="https://www.youtube.com/embed/kF_L7onVIo8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Watching Verizon's "easy" installation video above, I couldn't help
wondering at times if it was an SNL skit of an overly complicated
"easy" setup.

### Reliability

Frogs
: Bird and cow
: Make birds great again

### Bandwidth

I tested upload and download speeds over a period of about one week
and at different, random, times during each day, though mostly during
business hours since that is the time I was mostly concerned about.

For the test I used the built-in macOS command `networkQuality` with
the default parmaters. That meant that the test measured upload and
download speeds concurrently, which I think is more representative of
normal use than measuring each sequentially.

As you'll be able to see from the charts below, Verizon was the
download speed king yet it suffered from a day in which the service
was either down or so slow that it was unuseable. I also saw some
pretty bad numbers from Comcast at various points though that service
never outright failed.

#### Download Speeds During the Week (Mb/sec)

![Download Speed Over Time](/assets/images/isp-review/download-speeds.png)

#### Average Download Speed (Mb/sec)

![Average Download Speed](/assets/images/isp-review/average-download-speeds.png)

#### Upload Speeds During the Week (Mb/sec)

![Upload Speed Over Time](/assets/images/isp-review/upload-speeds.png)

#### Average Upload Speed (Mb/sec)

![Average Upload Speed](/assets/images/isp-review/average-upload-speeds.png)

### Connectivity

| Feature            | Comcast | Verizon | T-Mobile |
|--------------------|:-------:|:-------:|:--------:|
| LAN Ethernet Ports | 4       | 3       | 2        |
| 2.4 Ghz            | ✅      | ✅      | ✅       |
| 5 Ghz              | ✅      | ✅      | ✅       |
| 6 Ghz              | ✅      |         |          |
| MOCA               |         |         |          |

Comcast offers the most Ethernet ports, which is nice when you can
place it next to multiple devices that you want to plug in and so
avoid having to use an external Ethernet switch. One oddity I noticed
with the fourth Ethernet configuration in Comcast's web UI:

![Comcast Port 4 Config](/assets/images/isp-review/comcast-ethernet-port-4-config.png)

I see, so associating this port to my home network will remove it from
my home network. Hmm.... I think I'll leave it alone.

### Nerd Knobs

What options does each service offer for users who prefer to fiddle
with their router configuration? My preference would be for something
along the lines of this:

![Control Room](/assets/images/russian-control-room.png)

Short of that, the following table lists the sort of features you'd
expect and appreciate to see in a router.

| Feature            | Comcast | Verizon | T-Mobile |
|--------------------|:-------:|:-------:|:--------:|
| Dynamic DNS        |         | ✅      |          |
| UPnP               | ✅      | ✅      |          |
| Port Forwarding    | 📝      | ✅      |          |
| Port Triggering    | ✅      | ✅      |          |
| DMZ Host           | 📝      | ✅      |          |
| SIP ALG            |         | ✅      |          |
| Static NAT         |         | ✅      |          |
| Device Static IP   | ✅      | ✅      |          |
| Routing            |         | ✅      |          |
| IPv6 Pinholes      |         | ✅      |          |
| Bridge Mode        | ✅      |         |          |
| Firewall           | ✅      | ✅      |          |
| Network Objects    |         | ✅      |          |
| WiFi 6             |         | ✅      |          |

That's right, nothing for T-Mobile. They let you set your SSID,
password, frequency band, encryption type and that's about it. I
didn't include any of that in the table above because that stuff's
just a given today. Worse, it's necessary to make these settings
through their iOS or Android mobile app.

This makes me sad. There *is* a web UI built in to the T-Moble device
but it doesn't offer any configuration options to speak of, just a
link to the Android and iOS T-Mobile Internet apps. It did tell me I
wasn't currently connected to the internet, which was incorrect since
I'd been using that device for the past few hours.

Just for the lols, the following is a screen shot of the entirety of
the router configuration screen in the T-Mobile app. Note the
"Advanced" section.

![T-Mobile Configuration](/assets/images/isp-review/t-mobile-app-advanced-settings.png)

That's all there is for T-Mobile network configuration, I promise you.

Verizon obviously shines in this category. They have a nice and
extensive Web UI for configuring just about everything except for
switching to bridge mode. At least I couldn't find it. They have an
option called "Network Objects" which I don't completely understand
yet but looks interesting.

Comcast's configuration is decent and honestly I'd be ok with it.

Comcast and Verizon both offer some firewall configuration
options. Both offer three levels of pre-defined firewallification:
low, medium and high. Comcast also allows custom firewall
3configuration on both IPv4 and IPv6.

### Summary

My primary considerations for an ISP, other than price, are summarized
in the table below, with rankings for each service.

| ISP      | Download Speed | Upload Speed | Configurability | Reliability |
|----------|:--------------:|:------------:|:---------------:|:-----------:|
| Comcast  | 2              | 3            | 2               | 1 🏆        |
| T-Mobile | 3              | 2            | 4 ☹️             | 2           |
| Verizon  | 1 🏆           | 1 🏆         | 1 🏆            | 3 ☹️         |

Note that T-Mobile is a very close second in the reliability
category. As I mentioned above, I've already had a day long outage
from Verizon and as I'm writing this I've received notice to expect
another outage tomorrow, Monday. A work day.

My main concern is to have reasonably reliable service while also
having enough upstream bandwidth for two people to successfully carry
on concurrent Zoom meetings. Despite not coming in first in any
category, T-Mobile might just be the one I stay with as it's pretty
reliable and does work well for Zoom. I've been using a Roku TV to
stream 4K content over T-Mobile's service since installing it and I
can't recall any issues.

### Notes

Comcast 
: WebUI says set up in Moble app, but can't find it
: Firewall is very basic. 
: Pick from Minimum, Typical, Maximum and Custom security
: Custom security is:
: IPv4
LAN-to-WAN : Allow all.
WAN-to-LAN : IDS Enabled and block as per selections below.
 Block http (TCP port 80, 443)
 Block ICMP
 Block Multicast
 Block Peer-to-peer applications
 Block IDENT (port 113)
 Disable entire firewall
: IPv6 only "Typical" and Custom
: WebUI Software is "eMTA & DOCSIS Software Version: 10.1.27B.SIP.PC20.CT"
: Confusing option with LAN Ethernet Port 4, "Associate Ethernet Port 4 to XFINITY HOME Network: Note: Associating Ethernet Port 4 to XFINITY HOME network will remove the port from your home network."

T-Mobile
: App is flakey, doesn't think I'm on the T-Mobile WiFi when I am
: Router's web UI thinks the route's not connected to the internet
: Can't do anything with the web UI
