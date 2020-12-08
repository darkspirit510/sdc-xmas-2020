# sdc-xmas-2020

Great news that you're interested in my x-nmas workshop! After this course you'll be able to do small setups with openHAB. My planned agenda is short:

- A general introduction into smart home and how openHAB *sees* the world (important wordings, basic definitions and ideas, do's and don'ts, limitations)
- Free work 🕺 (i'll prepare some tasks until christmas)
- Small lookout what can/could be done with openHAB

I'll try to setup some remote instances, but the prefered way is an own openHAB installation. Don't hesitate to contact me if you have questions or need assitance with your setup.

## Preperation

This step is only necessary if you wan't to run your own instance. openHAB offers several ways to be run. My recommendations are:

- If you have a spare Raspberry Pi, run [https://www.openhab.org/docs/installation/openhabian.html](openHABian) on it
  - Pro: Basically just flashing an image and everything is there
  - Con: Might bring more than needed (like SMB access and some other things)
- Even simpler - just run openHAB with [https://www.openhab.org/docs/installation/docker.html](Docker)
  - Pro: Just openHAB, nothing else. Fast and easy to maintain/update, also can be run with other software
  - Con: Requires Docker 😅

Either way, during first access openHAB asks which UIs should be installed. Select "recommended" and wait (depending on your platform this might take some time). If you can access the PaperUI, that's it. Now you're ready for the workshop.

## Presentation

### Smart Home
*Home automation or domotics is building automation for a home, called a smart home or smart house. A home automation system will monitor and/or control home attributes such as lighting, climate, entertainment systems, and appliances. It may also include home security such as access control and alarm systems.* (Wikipedia)

### Common problems with smart stuff
- Lots of proprietary software / mobile applications
- Usually no (public) API
- Often dependent to internet connection
- rules across (eco)systems?

[![Standards](https://imgs.xkcd.com/comics/standards.png)](https://xkcd.com/927/)

### Smart Home systems

#### Homekit

Pros:
- Requires certification from Apple, you can expect this to work
- Does not require additional hardware
- Offers (rudi🍻mentary) rule engine

Cons:
- Certification will increase price
- Limited to "what Apple allows"

#### Vendor (Hue, Homematic, ...)

Pros:
- Hardware usually "just works"
- As a paid product, you can expect this to be tested
- Limited to vendors components

Cons:
- Blocking of non-approved hardware, even if the same (wireless) standard is used
- May be restricted with updates
- May stop working if vendor's cloud dies (for whatever reason)

#### Self Hosted Software (ioBroker, openHAB, ...)

Pros:
- Almost no limitation (especially because open source software)
- Marries different systems
- Rules can be created across systems/vendors

Cons:
- Requires own hardware
- Setup and learning can be time-consuming (in theory 😉)
- Sometimes working on reverse-engineered/unofficial APIs
- Might be blocked from systems if (non-official) APIs are used without approval

### openHAB




#### Binding

*Library* to connect openHAB with something external. Although there are bindings for generic stuff like HTTP, MQTT or even XMPP, more specific bindings exists for the outside world. Those bindings handle authentications, refreshs, transformations and other technical problems. Most of them can act bidirectional and even support auto detection of new things.

#### Thing

A thing is openHAB's representation of an external entity. This can be physical (a smart bulb, television, smartphone, gas station, ...) or something theoretical (network device, clock, weather provider). Things are used to group and identify external information via channels.

#### Channel

Something readable from or writeable to a thing. Has a type (which also brings transformation/extraction from thing) and can be transfered to openHAB.

#### Item

Compareable to a global variable in any programming language. Can (but does not have to) be linked to a channel of a thing. If linked to a channel, updates gathered through from a binding will be written to the item and updates to the item will be published via the binding.

## openHAB hands-on

tbd
