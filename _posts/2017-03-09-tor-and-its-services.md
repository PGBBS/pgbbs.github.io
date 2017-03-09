---
title: "Tor and its services"
layout: post
---

[A message from George Torwell](https://www.youtube.com/watch?v=c4EEa0HAqzQ)

"Wenn du meinst, Privatsphäre ist dir egal, nur weil du nichts zu verbergen hast, kannst du genauso behaupten, Redefreiheit ist dir egal, weil du nichts zu sagen hast" -- Ed Snowden

When anonymity fails, people die.

Snowden revelations and presentation :smile:

Arabic Freedom Spring

on the other hand: shutting down silk road was an investigative police effort (costing money and man-power)

Here's a list of [people](https://www.torproject.org/about/torusers.html.en) who use Tor (and their stories). Also movie director's sometimes [do](https://pbs.twimg.com/media/B1VZHZZCMAA721i.jpg).

# Tor

[overview](https://www.torproject.org/about/overview.html.en) with *the* three pictures from EFF.

and onion-layer animation on blackboard

- routes get switched regularly
- DNS servers get switched regularly

## and https

Here's an animation to understand what is providing what (and what not): [Tor and HTTPS](https://www.eff.org/pages/tor-and-https)

## Ingredients

- client software: Tor Browser Bundle (all platforms)
- network of relays (~8 000), also called nodes or routers

The directory of relays is public, so an adversary may block these connections. Tor [bridge relays](https://www.torproject.org/docs/bridges.html.en) aren't listed in the main Tor directory, so they may evade detection. If this doesn't work, then there's [pluggable transports](https://www.torproject.org/docs/bridges.html.en#PluggableTransports), where the traffic to the first hop is manipulated to be not (easily) identifiable as Tor connection.



### Three flavors of relays

Middle Relays ::

Exit Relays :: will show up as the origin of traffic from the Tor network. [Lawyer up!](https://www.eff.org/torchallenge/faq.html) (also: [Legal First Aid](https://www.privacyfoundation.de/wiki/Erste-Hilfe-fuer-Torbetreiber) (german))

Bridges :: not publicly listed, tools to circumvent censorship in countries that block IP addresses of publicly listed Tor relays

## Data and Metrics

- Raw Datasets for analysis/research at [CollecTor](https://collector.torproject.org/)
- Performance/Usage metrics derived from them at [TorMetrics](https://metrics.torproject.org/)

Excerpt: Users (~1.7 mil), Relays (~7 000), Bridges (~2 500), Bandwith (~100 Gbit/s)

There a few thousand relays
and a small number (9?) of central directory authorities, where relays need to register for announcement. The (dis)agreement of these directory authorities on the relays is visualized at http://letty.io/tor

# Attacks/Pitfalls

- any firefox bug
- any 3rd party tracking/identifiers (cookies, blob-URLs)
- fingerprinting defenses

[Change your habits](https://www.torproject.org/download/download-easy.html.en#warning)

Software Engineering Institute (SEI) of Carnegie Mellon University (CMU) (origin of CERT and "responsible disclosure") [attacked](https://motherboard.vice.com/en_us/article/carnegie-mellon-university-attacked-tor-was-subpoenaed-by-feds) the Tor network on a Department of Defense "research" project.

[Why TOR failed to hide the bomb hoaxer at Harvard](http://theprivacyblog.com/anonymity/why-tor-failed-to-hide-the-bomb-hoaxer-at-harvard/) TLDR; Hoaxer used TOR and Guerrilla Mail, but was the only one on Harvard Campus connected to the TOR network while the emails were sent.

## Does Tor Work? (When used properly?)

Ask the NSA (c/o Edward Snowden): [Tor stinks](https://edwardsnowden.com/docs/docs/tor-stinks-presentation.pdf)

# Tor Hidden Services/Tor Onion Services

Are .onion-adresses the same as hidden services?!

Think: own/parallel DNS-system

base64-encoded; hash of public-key (=> self-authenticating!)



riseup.net

[wikileaks](https://wikileaks.org/wiki/WikiLeaks:Tor) has a .onion address

http://suw74isz7wqzpmgu.onion/

which only works with Tor running.

hidden services directory

https://ahmia.fi/search/

http://thehiddenwiki.org/

# Applications

- [Tor Browser](https://www.torproject.org/projects/torbrowser.html.en) ::

display "Tor circuit" in browser through onion menu

- Orfox :: Android
- Tor Messenger/Ricochet :: chat client (for OTR)
- Tails

Library Freedom Project
ALA, Freedom to Read Statement "Freedom itself is a dangerous way of life -- but it is ours."

# Darknet

bad term; https: is a security measure, .onion is also one

surface web (indexed by google)
deep web (not indexed but accessible)
dark net/web (only accessible via Tor, i.e. anonymously); most URLs end with .onion

search engines:
- [onion.city](http://onion.link/), [onion.to](https://tor2web.org/), [NotEvil](https://hss3uro2hsxfogfq.onion.to/)

is based on hidden services

# References and Links

- [Tor Project](https://www.torproject.org/)

## Videos

- **Roger, David Goulet, asn**, [Tor onion services: more useful than you think](https://events.ccc.de/congress/2015/Fahrplan/events/7322.html) (english), presentation at 32C3, 29 Dec 2015
- **Roger, Jacob, Mike Perry, Shari Steele, Alison Macrina**, [State of the Onion](https://events.ccc.de/congress/2015/Fahrplan/events/7307.html) (english), presentation at 32C3, 29 Dec 2015
- **Annette Dittert, Daniel Moßbrucker**, [Das Darknet -- Eine Reise in die digitale Unterwelt](http://www.daserste.de/information/reportage-dokumentation/dokus/sendung/das-darknet-reise-in-die-digitale-unterwelt100.html) (german), ARD-documentary, 09 Jan 2017

## Audios

## Documents

- Sueddeutsche Zeitung, ["Das Darknet macht keine Waffen](http://www.sueddeutsche.de/digital/tor-netzwerk-das-darknet-macht-keine-waffen-1.3101766) (german), interview with Falk Garbsch, 31 Jul 2016

Phil Rogaway: ethical implications of cryptography: grim reaper instead of Alice and Bob
