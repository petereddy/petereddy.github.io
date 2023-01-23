---
layout: single
title:  "Comcast, Verizon and T-Mobile Internet Service Compared"
date:   2023-01-17 13:17:00 -0500
categories: [boston, ISP, comcast, tmobile, verizon]
---

A recent move has forced me to find a new ISP. Sadly, service from my
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
right in our sweet spot, location wise, so you should be able to get
gigabit speeds", he said. It wasn't true of course and I didn't expect
it.

I'm aware of only one T-Mobile service interruption in the five or so
months I've been using it, and that lasted only about two minutes.

### Verizon 5G

Even less to say about Verizon the company as I've had the service for
only about a week.

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
first month trial period. Given that it's a phone company at heart I
expect a number of inscrutable extra fees to be tacked on to that
bill.

# Setup

There's not much to report regarding T-Mobile and Comcast setup, it's
all pretty standard and easy, so much so that I don't remember the
details. T-Mobile, Verizon, and if I remember correctly Comcast also,
use phone app based setups, which is standard practice today. I
understand the reason for this though it's not my preference.

Verizon's hardware includes three different pieces, a large-ish power
brick, the router itself, and an antenna box. Oh, and they would very
much appreciate if you wouldn't mind gluing the antenna to your
window pane.

{:refdef: style="float: left; padding: 0 20px 20px 0;"}
![Verizon Antenna](/assets/images/isp-review/verizon-antenna.png)
{:refdef}

I assume the purpose of this is to ensure that it won't easily be
moved resulting in a connection disruption. I dislike the idea of
gluing things to windows, especially to living room windows, which
happen to be the only windows I have. Happily, gluing doesn't seem to
have been necessary. The router reports an excellent signal strength
with the antenna just sitting on a small table near the window,
dutifully facing it's big brother on the Verizon lamp post plinth
across the street.

<iframe width="560" height="315" src="https://www.youtube.com/embed/kF_L7onVIo8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Watching Verizon's "easy" installation video above, I couldn't help
wondering at times if it was an SNL parody skit.

I should note that the device I received from Verizon is not the same
type of device as the one in the video. My antenna is separate and
much smaller, definitely an improvement for window mounters. Unlike
the box in the video, Verizon states that my antenna can be mounted
outdoors as well, even going as far as to include an outdoor mounting
kit for it.

### Bandwidth Testing

I tested upload and download speeds over a period of about one week,
sampling at random times (i.e. when I remembered to do it) each day,
mostly during business hours as that's the time having good service
was most important to me.

I tested with an Apple M1 laptop over wifi, since that's what I use on
a daily basis. To measure bandwidth I used macOS's built-in
`networkQuality` tool with the default parmaters. That meant that the
tests measured upload and download speeds concurrently, which I think
is more representative of normal use than measuring each
independently.

Just for good measure, I also tested bandwidth with wifi turned off
and my laptop plugged into the ethernet connection on each router but
I didn't include the results because they weren't terribly different
to the wifi numbers.

I did not measure latency because I'm not a gamer, nor do I use my
connection for any other purpose that seems to be sensitive to this
metric.

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

#### Responsiveness

I also recorded responsiveness, which Apple
[defines](https://support.apple.com/en-us/HT212313) as follows:

> The Apple Network Responsiveness test reports its results using a measure called Round-trips Per Minute (RPM). The RPM is the number of sequential round-trips, or transactions, a network can do in one minute under normal working conditions.
>
> Low: If any device on the same network is, for example, downloading a movie or backing up photos to iCloud, the connection in some apps or services might be unreliable, like during FaceTime video calls or gaming.
>
> Medium: When multiple devices or apps are sharing the network, you might see momentary pauses or freezes, like during FaceTime audio or video calls.
>
> High: Regardless of the number of devices and apps sharing the network, apps and services should maintain good connection.

Only Comcast occasionally scored responsiveness values in the *Medium*
range however the average responsiveness scores for all three services
were in the *Low* category:

![Average Responsive](/assets/images/isp-review/average-responsiveness.png)

For the curious, there's an [IETF draft document
here](https://datatracker.ietf.org/doc/draft-cpaasch-ippm-responsiveness/)
with more information about responsivness.


### Connectivity

| Feature            | Comcast | Verizon | T-Mobile |
|--------------------|:-------:|:-------:|:--------:|
| LAN Ethernet Ports | 4       | 3       | 2        |
| 2.4 Ghz            | ✅      | ✅      | ✅       |
| 5 Ghz              | ✅      | ✅      | ✅       |
| 6 Ghz              |         | ✅      |          |
| MoCA               |         | ✅      |          |

Comcast offers the most Ethernet ports, which is nice when you can
place it next to multiple devices that you want to plug in and so
avoid having to use an external Ethernet switch. One oddity I noticed
with the fourth Ethernet configuration in Comcast's web UI:

Verizon offers an 10GE port and two additional 100 Mbps ports. I'm not
sure what MoCA is intended to be used for but I believe/hope it's the
normal MoCA method of extending the reach of the router via existing
coax wiring. If true, then that's a great feature and one I'd probably
make use of if I stick with this router. The network configuration for
this does warn, "Important: Only advanced technical users should use
this feature."

One strange message on the Verizon Ethernet port four configuration:

![Comcast Port 4 Config](/assets/images/isp-review/comcast-ethernet-port-4-config.png)

I see, so associating this port to my home network will remove it from
my home network? It's an intriguing option which I will have to
investigate some time.

### Nerd Knobs

Now, what options does each service offer for users who prefer to
fiddle with their router configuration? My preference for a router
configuration UI looks something like this:

![Control Room](/assets/images/russian-control-room.png)

The following table lists the sort of features you'd expect and
appreciate to see in a router.

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

First of all, yes that's right, T-Mobile offers no
configurability. They generously allow setting your own SSID,
password, frequency band, encryption type and that's it. I didn't
include any of that in the table above because that all a given
today. Worse, it's necessary to make these settings through their iOS
or Android mobile app

This makes me sad. There *is* a web UI built in to the T-Moble device
but it doesn't offer any configuration options to speak of, just a
link to the Android and iOS T-Mobile Internet apps. It did tell me I
wasn't currently connected to the internet, which was incorrect since
I'd been using that device for the past few hours.

The iOS app is also very flakey. It worked when I first set up
T-Mobile, but I had a very hard time connecting the app to the router
while writing this review. According to discussions I've seen in the
T-Mobile home internet forum, I'm far from the only one having this issue. 

Just for the lols, the following is a screen shot of the entirety of
the router configuration screen in the T-Mobile app. Note the
advanced section.

![T-Mobile Configuration](/assets/images/isp-review/t-mobile-app-advanced-settings.png)

That's all there is for T-Mobile configuration.

As you can see from the table above, Verizon shines in the
configuration category. They have a nice and extensive Web UI for
configuring just about everything except for switching to bridge
mode. It's possible bridge mode is there but I couldn't find it. They
have an option called "Network Objects" which I don't completely
understand yet but which looks interesting.

Comcast's configuration is decent and honestly I'd be ok with it.

Comcast and Verizon both offer some firewall configuration
options. Both offer three levels of pre-defined firewallification:
low, medium and high. Comcast also allows custom firewall
configuration on both IPv4 and IPv6, that lists the following options:

WAN-to-LAN : IDS Enabled and block as per selections below.
- Block http (TCP port 80, 443)
- Block ICMP
- Block Multicast
- Block Peer-to-peer applications
- Block IDENT (port 113)
- Disable entire firewall

### Summary

Price aside, my primary considerations for an ISP are summarized in
the table below, with rankings for each service.

| ISP      | Download Speed | Upload Speed | Configurability | Reliability |
|----------|:--------------:|:------------:|:---------------:|:-----------:|
| Comcast  | 2              | 3            | 2               | 🏆          |
| T-Mobile | 3              | 2            | ☹️               | 2           |
| Verizon  | 🏆             | 🏆           | 🏆              | ☹️           |

Note that T-Mobile is a very close second in the reliability
category. As I mentioned above, I've already had a day long outage
from Verizon and as I'm writing this I've received notice to expect
another outage tomorrow, Monday. A work day.

My main desire is to have reasonably reliable service while also
having enough upstream bandwidth for two people to successfully carry
on concurrent Zoom meetings. 

With the above in mind, and despite not it not coming in first in any
category, T-Mobile might just be the service I stick with as it's
relatively reliable and has proven to work well with multiple Zoom
sessions. I've been using a Roku TV to stream 4K content over the
T-Mobile service the entire time I've had that service and I can't
recall a single issue.

The bottom line is that I'm disappointed in all three services. I was
spoiled by [Starry's](https://starry.com) 200 Mbps symmetric
upload/download service. I'm also eager to try
[netBlazr](https://www.netblazr.com) who advertise up to 1000 Mbps
symmetric service at $50/mo, but alas that service is also unavailable
in my building despite their antenna just down the street.
