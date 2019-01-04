---
title: "Tor and its services"
layout: post
---

{:refdef: style="text-align: center;"}
[![A message from George Torwell](https://img.youtube.com/vi/c4EEa0HAqzQ/0.jpg)](https://www.youtube.com/watch?v=c4EEa0HAqzQ)
{:refdef}

"Wenn du meinst, Privatsphäre ist dir egal, nur weil du nichts zu verbergen hast, kannst du genauso behaupten, Redefreiheit ist dir egal, weil du nichts zu sagen hast" -- Ed Snowden

When anonymity fails, people die. The eavesdropper "Eve" should not be "cute", but a grim reaper, see Rogaway (2015).

Snowden revelations, Arabic Freedom Spring

Here's a list of [people](https://www.torproject.org/about/torusers.html.en) who use Tor (and their stories). Also movie directors sometimes [do](https://pbs.twimg.com/media/B1VZHZZCMAA721i.jpg).

- TOC
{:toc}

Tor is used by Journalists all around the world to enable privacy of themselves and their sources. The main task of Tor is to ensure anonymity in communications. It's based on a concept of Roger Dingledine which was published 2004.

# Tor

In short Tor is a network of servers that tries to improve privacy on the internet by redirecting encrypted traffic over virtual tunnels. By using Tor, internet surveillance techniques like simple traffic analysis can be made much harder or even impossible. A common data packet sent over the internet is split in the payload and the header. The payload contains the content of the data packet, while the header is used for enrollment. By looking into the payload, anyone observing the traffic can extract all the information of the communication. This risk can be reduced by encrypting the payload. This is for example done in HTTPS. Unfortunatly the header can't be obfuscated in the same way because it is needed for routing the packet to the right receiver. By analyzing the header, third parties are able to extract information about who communicated with whom, the time of communication, and the size of the sent data.

This [overview](https://www.torproject.org/about/overview.html.en) link gives an introdcution to the functionality of the Tor network by text and three pictograms released by the [Electronic Frontier Foundation](https://www.eff.org/de).

Tor creates private network pathways to make it harder to locate the sender of a data packet. This is achieved by starting the communication with a randomly chosen starting point. From here, the path is iteratively extended one hop at a time. Individual relays can't see further in the path than one step of communication. Each relay knows only the sender of the last hop and the receiver of the next.

Directory servers are hereby used to track the IPs of all voluntarily participating nodes in the Tor network. They are asked by the client to yield an entry point to the network. There are currently 9 directory servers feeding the Tor network. The client can switch between DNS servers and entry points and therefore distribute it's actions even more. Regular switching of routes makes it harder to pinpoint communications.

- routes get switched regularly
- DNS servers get switched regularly

## Ingredients for privacy

{% include image.html
            img="images/privacy.jpg"
            title="Privacy"
            caption="CC BY 2.0 (http://creativecommons.org/licenses/by/2.0), via flickr.com"
            url="https://www.flickr.com/photos/g4ll4is/8521624548/" %}

These are the ingredients for the Tor network:

- directory servers
- network of relays (~8 000), also called nodes or routers

To access the network one can use a client like the:

- Tor Browser Bundle (suitable for all platforms)

The directory of relays is public, so an adversary may block these connections. This can make it harder to access the Tor network in strictly regulated enviroments. Tor [bridge relays](https://www.torproject.org/docs/bridges.html.en) aren't listed in the main Tor directory, so they may evade detection. If this doesn't work, then there's [pluggable transports](https://www.torproject.org/docs/bridges.html.en#PluggableTransports), where the traffic to the first hop is manipulated to be not (easily) identifiable as Tor connection.

## Tor and https

Tor is used to obfuscate the header information and HTTPS is used to obfuscate the content.

Here's an animation to understand what is providing what (and what not): [Tor and HTTPS](https://www.eff.org/pages/tor-and-https)

## Three flavors of relays

Middle Relays ::

Exit Relays :: will show up as the origin of traffic from the Tor network. [Lawyer up!](https://www.eff.org/torchallenge/faq.html) (also: [Legal First Aid](https://www.privacyfoundation.de/wiki/Erste-Hilfe-fuer-Torbetreiber) (german))

Bridges :: not publicly listed, tools to circumvent censorship in countries that block IP addresses of publicly listed Tor relays

## Data and Metrics

- Raw Datasets for analysis/research at [CollecTor](https://collector.torproject.org/)
- Performance/Usage metrics derived from them at [TorMetrics](https://metrics.torproject.org/)

Excerpt: Users (~1.7 mil), Relays (~7 000), Bridges (~2 500), Bandwith (~100 Gbit/s)

There a few thousand relays
and a small number (9?) of central directory authorities, where relays need to register for announcement. The (dis)agreement of these directory authorities on the relays is visualized at http://letty.io/tor

# Applications

- [Tor Browser](https://www.torproject.org/projects/torbrowser.html.en) :: display "Tor circuit" in browser through onion menu
- Orfox :: The Tor Browser for Android
- Orbot :: Enabling Tor network for other applications in Android
- [Ricochet](https://ricochet.im/), Tor Messenger (beta) :: (de-centralized) chat client (for OTR)
- [Tails](https://tails.boum.org/) :: (amnesic, incognito) live operating system (built on Debian GNU/Linux)
- [SecureDrop](https://securedrop.org/) :: whistleblower submission system; used by [The New Yorker](http://projects.newyorker.com/strongbox/), [The Intercept](https://theintercept.com/securedrop/)

Library Freedom Project
ALA, Freedom to Read Statement "Freedom itself is a dangerous way of life -- but it is ours."

# Attacks/Pitfalls

- any firefox bug
- any 3rd party tracking/identifiers (cookies, blob-URLs)
- fingerprinting defenses

[Change your habits](https://www.torproject.org/download/download-easy.html.en#warning)

Software Engineering Institute (SEI) of Carnegie Mellon University (CMU) (origin of CERT and "responsible disclosure") [attacked](https://motherboard.vice.com/en_us/article/carnegie-mellon-university-attacked-tor-was-subpoenaed-by-feds) the Tor network on a Department of Defense "research" project.

[Why TOR failed to hide the bomb hoaxer at Harvard](http://theprivacyblog.com/anonymity/why-tor-failed-to-hide-the-bomb-hoaxer-at-harvard/) TLDR; Hoaxer used TOR and Guerrilla Mail, but was the only one on Harvard Campus connected to the TOR network while the emails were sent.

## Does Tor Work (when used properly)?

Ask the NSA (c/o Edward Snowden): [Tor stinks](https://edwardsnowden.com/docs/docs/tor-stinks-presentation.pdf)

# Tor Hidden Services/Tor Onion Services

[Overview](https://www.torproject.org/docs/hidden-services.html.en)

How much? Compare [total traffic](https://metrics.torproject.org/bandwidth.html) with [onion traffic](https://metrics.torproject.org/hidserv-rend-relayed-cells.html)

ICAN gives top-level addresses -- except for .onion

16-digits encoded in base32 (a-z and 2-7)

hidden services = .onion-adresses

Think: own/parallel DNS-system

hash of public-key (=> self-authenticating!); NEW not 16 char hash any more, but 52 char public-key.

[wikileaks](https://wikileaks.org/wiki/WikiLeaks:Tor) has a .onion address

    http://suw74isz7wqzpmgu.onion/

which only works with Tor running.

hidden services directory

- https://ahmia.fi/search/
- http://thehiddenwiki.org/

## "Darknet"

bad term; https: is a security measure, .onion is also one

search engines:
- [onion.city](http://onion.link/), [onion.to](https://tor2web.org/), [NotEvil](https://hss3uro2hsxfogfq.onion.to/)

is based on hidden services

# References and Links

- [Tor Project](https://www.torproject.org/)

## Videos

- **Roger, David Goulet, asn**, [Tor onion services: more useful than you think](https://events.ccc.de/congress/2015/Fahrplan/events/7322.html) (english), presentation at 32C3, 29 Dec 2015
- **Roger, Jacob, Mike Perry, Shari Steele, Alison Macrina**, [State of the Onion](https://events.ccc.de/congress/2015/Fahrplan/events/7307.html) (english), presentation at 32C3, 29 Dec 2015
- **Annette Dittert, Daniel Moßbrucker**, [Das Darknet -- Eine Reise in die digitale Unterwelt](http://www.daserste.de/information/reportage-dokumentation/dokus/sendung/das-darknet-reise-in-die-digitale-unterwelt100.html) (german), ARD-documentary, 09 Jan 2017
- **Daniel Mossbrucker (Reporter Ohne Grenzen), Andreas May
  (Generalstaatsanwaltschaft Frankfurt), Julia Eikmann (Journalistin,
  Autorin, Moderatorin) und Ahmad Alrifaee (Hamburg Media School)**,
  [Darknet -- Das Internet der
  Zukunft?](https://www.youtube.com/watch?v=ImW5lLfiT6I) (german),
  Podiumsdiskussion auf der re:publica 17

## Documents

- Sueddeutsche Zeitung, ["Das Darknet macht keine Waffen](http://www.sueddeutsche.de/digital/tor-netzwerk-das-darknet-macht-keine-waffen-1.3101766) (german), interview with Falk Garbsch, 31 Jul 2016
- Phillip Rogaway (2015), ["The Moral Character of Cryptographic Work"](http://web.cs.ucdavis.edu/~rogaway/papers/moral-fn.pdf)
- Mike Barlow and Gregory Fell (2016), ["Patrolling the dark
  net"](https://www.oreilly.com/ideas/patrolling-the-dark-net),
  O'Reilly Media
