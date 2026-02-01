---
layout: post
title: "Retrofitting networked MIDI to analog audio gear"
---

**Cool news: We're starting to offer MIDI over Ethernet/WiFi/Bluetooth retrofits for analog audio
hardware!**

The intent is mostly for studio equipment, but also synths, drum machines etc:
MIDI over Ethernet/WiFi and Bluetooth for remote control from your DAW, tablet/iPad or smart phone.
These use tiny microcontrollers (see picture below) can interact with control voltage (CV) or
specific parts of circuits; *for example* in an outboard studio equalizer that has switched pots/knobs
to control frequency/volume of a given EQ-range or shape - you can
change the resistance of a switched knob thereby remotely controlling the
position without having to turn anything on a unit that may be further
away/outboard in a rack. Obviously this doesn't replace motorized fader/poti
automation as many are used to from SSL and other consoles, but can make day-to-day
studio life a lot quicker and more reliable: as this also adds easy recall via MIDI.


![img](assets/images/posts/midi_esp.png)

#### Why MIDI instead of XYZ?

MIDI is an old protocol, but it's still ubiquitous in the pro-audio
landscape. MIDI because it works for 98% of use-cases we can think of
and is universally supported by DAWs, Operating Systems, Tablets &
Smartphones. Today there are lots of very complex MIDI routers and hubs
for big production and home studios and MPE (MIDI Polyphonic Expression)
now also widely available due to DAWs like Ableton and support in new synth
hardware, MIDI-Controllers and supporting products. 


#### Why networked MIDI?

Of course you would also be able to pair or directly connect any MIDI controller you prefer.

Today a lot bring out of the box support for networked MIDI via software
or can easily be integrated to use MIDI over Ethernet/Bluetooth via
adapters.

What protocol are we specifically talking about?
[RTP-MIDI](https://en.wikipedia.org/wiki/RTP-MIDI).
It's an open standard that most MIDI-support products (switches/routers/hubs)
support. As does Windows, MacOS X/iOS and Linux/Android.

- [RTP-MIDI or MIDI Over Networks
(midi.org)](https://www.midi.org/midi-articles/rtp-midi-or-midi-over-networks)
- [rtpMIDI-driver for
Windows](https://www.tobias-erichsen.de/software/rtpmidi.html)
- [An Implementation Guide for RTP MIDI (RFC 4696)](https://www.rfc-editor.org/rfc/rfc4696.html)

###### What about ipMIDI? or BLEMIDI?

There's an older non-standardized spec of MIDI over IP (Internet
Protocol) which of course also works over Ethernet and WiFi but is less
flexible. There's some support in software and old SSL products, some
commercial applications use it, but very few. Support is possible and
easiy added - we will add support if it's requested. The ESP
microcontrollers have readily available libraries for all modern MIDI
transports including RTP-MIDI, ipMIDI, BLEMIDI and MIDI over USB.

- [Arduino MIDI Library -
Transports](https://github.com/FortySevenEffects/arduino_midi_library?tab=readme-ov-file#other-transport-mechanisms)

###### Is this going to support SysEx?

This would be possible, depending on application and retrofit device.
SysEx is very seldomly used anymore these days and won't be a standard
feature in any of our default implementation and software releases/updates
for the microcontroller driving MIDI and configuring your retrofitted
device.

#### What about adding MIDI Jacks and MIDI Through?

Some people love using specific keyboards as their MIDI Master. No
worries:

1. There are adapters and the possibility to retrofit THAT device as well
2. In bigger synth/production setups there's usually a MIDI
   Router/Hub/Switch around anyway, check the details of the one you
   have, most likely it supports MIDI via Ethernet in some way, often
   even Bluetooth along with the now more and more common MIDI over USB
   option many vendors offer on their products in addition to DIN 5-Pole
   MIDI jacks.
3. A lot of DAW remote-control software already uses MIDI over
   Ethernet/Bluetooth; most iPad/Tablet Apps work this way.

Furthermore:     

For older units or such that only support classic MIDI cables we can fit
new MIDI in/out & through on most mentioned hardware but please don't
hesitate to ask in detail and just contact us via the form on this page.
If you're interested get in touch with us for details about specific 
products you may want to retrofit and if it's possible on a given 
unit/price of the HW upgrade and..


..Stay Tuned for more!

![img](assets/images/posts/midi_feather.png)


