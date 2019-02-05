# My visit to FOSDEM19

## Introduction
FOSDEM (Free and Open-Source Software Developers' European Meeting) is an annual conference that happens on the first weekend of February and is hosted by the Free University of Brussels in its Solbosch campus. It gathers about 5000+ engineers and includes a very broad programme, revised each year, of keynote speeches, main track and thematical ("developer room") talks, flash talk (15 min.) reports and project stands, where you can listen to and speak with the leading people of the biggest open-source projects in the world as well as very small promising projects.

## Saturday
I came into this edition of FOSDEM on Friday and had its evening devoted to walking on the streets of a beautiful city of Brussels.

My first day at the conference started with a tour of the stands in K building: getting acquanted with (or asking about the advances of) different projects, snatching giveaways for free or for money. This time I stopped for some time on the stand of [\[matrix\]](https://matrix.org) project, an effort to develop a platform for secure p2p instant messaging that is sponsored and promoted by French government. Another interesting project new to me was [Hackages](https://hackages.io/) online learning platform, some cross between Stackoverflow and Udacity/Udemy. I was a bit skeptical of both of them, and I am quite interested to see what comes out of them! Might be that my skepticism is groundless.

After some wandering around and networking with people I went to the "Open source design" devroom to listen to a [talk](https://fosdem.org/2019/schedule/event/cost_of_not_doing_user_research/) on the consequences of and lessons from not doing proper user research in a software project, its real cost and methods and recommendations to do it "the right way".

Then I went to the H building to see what stands they had there. I stumbled upon a [WolfSSL](https://www.wolfssl.com/) stand and got myself interested in the tools they offer:
- an embedded SSL library with a very long list of features, own API and well as OpenSSL compatibility layer;
- a crypto library with the same availability and broad feature set, supporting many embedded HW chipsets (crypto acceleration?);
- a library with TPM2 API;
- secure MQTT and SSH libraries;
- secure bootloader;
- some other modules related to embedded and IoT security.
All of it is available on a long list of embedded SW platforms, e.g., FreeRTOS and Mbed, in addition to the usual Win/Linux/Mac.

After I have wandered around for some time and had a lunch, I went to Janson auditorium to listen for a [presentation](https://fosdem.org/2019/schedule/event/tpm2/) of TPM2 API and open-source development effort around it.

The next [talk](https://fosdem.org/2019/schedule/event/mender/) I was especially interested in was about an over-the-air embedded SW update project/toolset named Mender. The talk included an overview of popular update methods, as well as motivation behind design choices taken in the project.

## Sunday
My second day at the conference started in "Hardware enablement" devroom with a [talk](https://fosdem.org/2019/schedule/event/hardware_raspberrypi/) on RaspberryPi history, model set, use cases and perspectives. Then I rushed into "Security" room to get myself a space to sit on, because I new that although the UD2.218A auditorium was big, it would be completely full for the next [couple of talks](https://fosdem.org/2019/schedule/track/security/). I was just in time to see [Dmitry](https://fosdem.org/2019/schedule/speaker/dmitry_eremin_solenikov_lumag/) challenged with quite interesting questions about his [talk](https://fosdem.org/2019/schedule/event/gost_crypto/) on Russian crypto.

Then I sat in that room [watching](https://fosdem.org/2019/schedule/streaming/) a talk in another room about the U-Boot in general, accompanied with some interesting technical details, given by a [maintainer](https://fosdem.org/2019/schedule/speaker/jagan_teki/) for several U-Boot subsystems. Unfortunately, it was in too short a time to cover such a big topic, so he went way fast for me to keep up.

After that talk I put down my headset and paid attention to a very interesting talk by [Tobias](https://fosdem.org/2019/schedule/speaker/jagan_teki/) about what happens when you request a webpage on a protocol level, how the latest performance improvement efforts (in TCP extensions, TLS 1.3 and QUIC), in part because of IoT, have compromised security and what can be and is being done to fix things. As the talk was about "bugs" in newest/coming protocol revisions that attempted to address problems in versions currently in use, you can imagine the mess with current protocols in use in IoT!

After that talk I plugged again my headset to watch "UEFI boot for mere mortals" talk in "Hardware enablement" devroom. I expected a bit more info on the topic (what was [advertised](https://fosdem.org/2019/schedule/event/uefi_boot_for_mere_mortals/)), but got a comparison of Tianocore and U-Boot from the aspect of UEFI, with a "brief" introduction of the term itself.

Then again I switched back to reality in the "Security" room to listen about USB security, security-related UI/UX principles and how the problem is being addressed in the Gnome desktop. With 3 main questions addressed by the [talk](https://fosdem.org/2019/schedule/track/security/), I was quite surprised how well it was structured to cover all of them in just 25 minutes. Likewise, I was impressed with things you could do by plugging a "specially designed" USB device into a modern(ish) laptop (say, Ubuntu 16.04) or another host, like gaining root access and installing a snooping malware in a split second. Imagine all those "charge your phone points" in the airports and other public places! A brief overview of a history of fighting such attempts has been given, all critisized from the point of view of an ordinary user. Again, I couldn't disagree with a statement that each attempt to force a user to make a permanent security-related decision (whether to block a device/website/certificate/whatnot or to trust it) considerably reduces a user base for your software.

Next, developers from Ecuador introduced me to the "Off-the-record" messaging protocol and its coming version 4, in which several real world conversation properties (like deniability) were scientifically formalized and proven to hold. This talk restored my hope for the future of communication in our orwellian world! I must admit that due to my ignorance I never knew such a thing existed since 2004 and people were not just "seriously concerned with" an absence of privacy in instant messaging but were actually fighting it in a truly secure manner (i.e., devising methods open for public scrutiny and review).

The next [talk](https://fosdem.org/2019/schedule/event/recordflux/) in the same room was about an interesting but early stage project to formally specify and validate communication protocols from the security perspective. Like many "early stage projects" advertised at FOSDEM, this can potentially prove to be a good one and used worldwide in a matter of a few years!

After that I went to "CAD and open hardware" devroom in AW building to listen to two talks in a row about free and open source tools you can use to design your hardware, as well as methods and advice on manufacturing PCB and mounting components. The [first](https://fosdem.org/2019/schedule/event/idea_to_prototype/) one was more focused on overview and comparison of tools, while the [second](https://fosdem.org/2019/schedule/event/guide_to_oshw/) covered methods, common pitfalls, advice to avoid them and success stories in open hardware community.

Those two were followed by a talk on [PSLab](https://pslab.io/) hardware/software project to provide a very cheap (about 60 EUR) and open source up-to 2 MSample/s oscilloscope/logic analyzer/waveform generator with multimeter functionality and plug-and-play measurement for tens of off-the-shelf I2C, I2S and SPI sensors that works with your PC or an Android/Fdroid smartphone.

From "CAD and open hardware" room I went back to "Hardware enablement", to listen to a [report](https://fosdem.org/2019/schedule/event/kernelci_a_new_dawn/) on renewed interest in KernelCI project on the part of big corporations (G and M, you know them!) and Linux Foundation to systematically test Linux kernel: its current infrastructure, status, test methodology and perspective for the coming years. The report included an overview of existing methods for testing kernel, in which I was especially interested. Questions asked after the report were very interesting to see answered as well.

## Conclusion
That concluded my second day at this edition of FOSDEM. A few takeaways I gathered include doing homework on such projects as:
* PSLab;
* Matrix.org;
* Sofa;
* Hackages;
* Mender;
* up-to-date embedded systems-focused SSL implementation and tools WolfSSL;

as well as tools:

* electronic circuit simulator [ngspice](http://ngspice.sourceforge.net/);
* schematics capture and PCB layout suite [KiCAD](http://kicad-pcb.org/);
* mechanics design tools LibreCAD, OpenSCAD, FreeCAD, QCAD, Blender;

and various popular off-the-shelf components, like a very cheap and powerful WiFi module [ESP8266](https://www.espressif.com/en/products/hardware/esp8266ex/overview). Also I got some material ones like a free 9,5% vol. beer (unthinkable as a give-away in Finland!) from WolfSSL guys, an OpenSUSE beer and a number of geeky t-shirts.

All-in-all, even if you are not a speaker, but a sneaker (well, lurker), FOSDEM is a very good means to be aware of latest SW-related technology, because much, if not all, of it happens with open source effort. As my visit is supported in part by my employer, [Etteplan Software and Embedded Solutions](https://www.etteplan.com/expertise/software-and-embedded-solutions) (for which I am very grateful), I consider it a perfect investment into self-education!
