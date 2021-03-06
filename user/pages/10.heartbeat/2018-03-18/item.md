---
title: "yunity heartbeat 2018-03-18"
date: "2018-03-18"
continue_link: true
taxonomy:
    category: blog
    tag: [heartbeat]
published: true
---

**The yunity heartbeat** - news from the world of sharing, fresh every two weeks.

## [CivicTechGbg](http://civictechgbg.se/)
Organized by Bruno and others in [Digidem Lab](http://digidemlab.org/en/) in Gothenburg, Sweden, Civictech is going to be a series of hackdays and networking events to bring active people from civil society closer together and to thus form a coherent movement to tackle the problems of our current times in an open, collaborative and non-commercial way. The first event took place on March 10 at Viktoriahuset in Gothenburg.

![The very first CivicTechGbg event in Viktoriahuset](techcivic.jpg)
_The very first CivicTechGbg event in Viktoriahuset_

Karrot (and foodsaving in general) was one of four projects participating, the others were:
- [Hyresrättskollen](http://hyresrattskollen.se/) - collecting data to counter gentrification
- [DinRiksdag](https://www.dinriksdag.se/) - adapting [consul](http://consulproject.org/en/) to make the Swedish democracy more interactive
- [Getaborg](https://getaborg.se/) - a multisharing plattform for Gothenburg

_by Janina_

## [Foodsaving Worldwide](https://foodsaving.world)
Thanks to CivicTechGbg Janina and Tilmann finally managed to meet the foodsavers of [Solikyl](http://solikyl.se) in Gothenburg! Bruno and Madde hosted us for over a week and we got many opportunities to build stronger bonds to various members of Solikyl. It was amazing to see all the food they save (professionally documented on steemit, [check it out](https://steemit.com/@solikyl)!) and what a tightly-knit, productive group they built! We hope to see them again in the not so distant future and wish them all the best until that time comes. :)

Being already in the area, visiting Lotta in Borås was the logical thing to do. She is still planning on starting a foodsaving group in the smaller Swedish city as well and got a boost of new motivation after doing an epic dumpster dive together with Tilmann and Janina. On top of that she already arranged a networking meetup with Taras - our contact in Stockholm - and will drop by Solikyl's friday hang-outs once in a while.

![Some food that was saved in Borås](dd_after-full.jpg)
_Some food that was saved in Borås_

But there's even more foodsaving going on in Sweden!

The [foodsavers of Lund](https://www.facebook.com/groups/829765127111133/) also welcomed Janina and Tilmann and will be visited for some days, and Teddy already announced the second meeting to build up [Foodsharing i Östersund](https://www.facebook.com/groups/194858781249133/).

_by Janina_

## [Karrot](https://karrot.world)

After the hackweek end of February, lots of started work had to be finished and merged. The playground group is ready (@tiltec), as well as reactions to messages (@mrkvon). The group member list separates active from inactive users and the store list optionally shows archived stores too (@tiltec). The karrot mobile app is not released yet, but it's already quite usable with the new feature to pull fresh data when it switches from background to foreground (@nicksellen).

There's another type of notification email: if there's a pickup with free slots on the next day, you will get an email in the evening before. We added pickup feedback to the weekly summary email (@nicksellen).

We started collect internal statistics about group activity to find out more about how Karrot is used (@nicksellen). In future, we plan to display some of those statistics on karrot itself.

The foodsavers from Poland updated their language, which fits together with their plans to use karrot in the coming months.

![](karrot-reactions.png)
_Message reactions_

![](karrot-playground.png)
_Playground group_

![](karrot-stats.png)
_Statistics_

_by Tilmann_

## [Kanthaus](https://kanthaus.online)

Matthias installed a canbus system in the house some time back to collect various data about the house - the idea is to collect gas/water/electricity usage, room temperatures, humidity, etc.

There seem to be two main goals:
1. making people more aware of the resources they consume
2. having fun playing with some cool things :)

For a while the sensors have been up and running, but we have not been collecting the data anywhere.

Matthias gave Nick and Silvan a crash course in [canbus](https://en.wikipedia.org/wiki/CAN_bus) / [uavcan](http://uavcan.org/) and we got started with a python tool to collect the data and write it to influxdb. We built a tool called [uavcan-influxdb-writer](https://github.com/yunity/uavcan-influxdb-writer) to do this.

![](kanthaus-custom-board.jpg)
_Custom circuit board designed by Matthias and manufactured in China (I didn't even know that was a thing you could just do!). Here it is being a canbus to usb adapter, but can also have sensors connected to it._

![](kanthaus-pi.jpg)
_Raspberry pi to collect the data from the USB interface, and send it to influxdb_

The next part is to visualize the data from influxdb, we already have a [grafana](https://grafana.com/) installation and it was easy to add our new data into it and make a pretty dashboard.

![](kanthaus-grafana.png)
_Pretty dashboard!_

Not all the numbers are quite right yet though.

The gas is read by detecting a magnetic pulse as the counter rotates, and the water by using an infrared beam to detect the fast rotation of the dial. The difficulty is getting from the messy world of physical/analogue/electrical things into the nice clean digital environment.

The temperature sensors and greywater tank full detection are working nicely though!

We put our pi setup into an [ansible configuration](https://gitlab.com/kanthaus/kanthaus-ansible) so we can configure it from fresh whenever we need to. We used some cool systemd techniques to start the software automatically when you plug the USB device in, hopefully this will increase reliability of the data sending.

You can read more about the infrastructure in our new [kanthaus handbook](https://handbook.kanthaus.online/).

Aside from that we enjoyed the brief respite from the winter and hosted a foodsharing brunch outside:

![](DSC05466.JPG)
_Felt like spring had arrived!_

Work also started on the garden, and we had some stuff to burn!

![](ADSC05464.JPG)
_The "kebab" in Matthias' hand is actually bread baked in the fire :)_

For now though, back to winter...

![](DSC05498.JPG)

_by Nick_

## Haus X Harzgerode
Winter came back to Harzgerode with full force and made us delay the practical part of the project a bit. But there's a lot of planning and thinking to do anyways. Haus X is not just a house project. It will be one of many groups building the future ecovillage in Harzgerode.
- Which tasks will be our part?
- How can Haus X be open and free for everyone without sabotaging the accommodation- and event business of the main community (which is used to fund the project and enable Haus X to exist in the first place)?
- Haus X is going to have the privilege to allow moneyfree living. How can this be managed without freeloading the rest of the community?

Lots of questions, but none of them unsolvable. A small group (Lise, Bodhi, Josi, Steffen) will meet this upcoming week to chat about circumstances to participate in the project an maybe about some of those questions

![Haus X fancily illuminated](HausXnightbright.jpg)

_by Steffen_

## About the heartbeat.
The heartbeat is a fortnightly summary of what happens in yunity. It is meant to give an overview over our currents actions and topics.

### How to contribute?
Talk to us in [#heartbeat](https://yunity.slack.com/messages/heartbeat/) on [Slack](https://slackin.yunity.org) if you want to add content, change the layout or any other heartbeat related issues and ideas! We are also happy about any kind of feedback! ^_^
