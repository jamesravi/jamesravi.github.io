---
layout: post
title: Thoughts on switching to Linux (and why you could)
excerpt: <p>Linux isn't perfect, but given its emphasis on being free (in multiple ways) means it could be a viable choice for you.</p>
tags:
  - main post
---

<img src="{{ site.baseurl }}/images/tux-enhanced-v2.svg" alt="Tux the penguin, mascot of Linux" height="350" />
*[Tux the penguin](https://en.wikipedia.org/wiki/Tux_(mascot)), mascot of Linux* [^0]

&nbsp;

You’re probably heard of [Linux](https://en.wikipedia.org/wiki/Linux).[^1] Here I’ll try to summarise some advantages and disadvantages, some of which I have found when switching myself to Linux Mint.

(also feel free to scroll down to the end for a quick tl;dr if you’re running a little short on time)


## Advantages

There are many advantages of Linux (privacy; customizability - that’s a common one; philosophical (i.e. a community effort to build an operating system and software rather than using the proprietary ones provided by a company) etc.) that I’m sure many people have said on the web ([this is a good Reddit comment I found](https://www.reddit.com/r/linux_gaming/comments/7n6bc9/switching_to_linux_is_it_worth/drzef6x)), so you’re free to check those out. Two main ones that might be the most applicable:



* **Linux is free**. Of course, Linux is philosophically free “as in speech” ([as Richard Stallman phrases it](https://www.gnu.org/philosophy/free-sw.html)) being [free and open-source software under the GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License), and from that it’s also free “as in beer” i.e. price. [Linux distros](https://en.wikipedia.org/wiki/Linux_distribution) are typically[^2] free to download and install[^3], so it’s quite easy to find one and try it out. In turn, given the community around it, **much of the software on Linux is free and open-source** as well.


* **Linux works better than Windows on older hardware**. Have older hardware? Don’t use outdated operating systems such as Windows XP! Simply slap a Linux distro on it, and you’ll be able to keep using your computer and still receive the latest security and software updates. Of course, as I’m about to mention, it won’t be a 100% seamless transition, but for most everyday activities such as browsing the web, emailing, writing documents etc. it should be perfectly fine.


## Disadvantages

Of course, Linux is, as you are probably aware, developed by a community of volunteers around the world, and although there is some commercial support from companies such as Canonical and Red Hat, it’s hard to compete with more proprietary companies who spend lots of time and money “polishing” their operating systems for mainstream usage (more specifically, the user interfaces).[^4] Nonetheless, I feel it’s prudent to say Linux can’t be easily dismissed, due to its extensive community and [much usage](https://en.wikipedia.org/wiki/Linux#Commercial_and_popular_uptake) on servers, [supercomputers](https://www.zdnet.com/article/linux-totally-dominates-supercomputers/)[^5] and most famously Android, and it definitely is (in my opinion) 99% of the way there as a desktop distro for the mainstream (a lot of people are using it as a daily driver perfectly fine) - but if you’re considering switching, you do have to be aware there are a few rough edges.

Here are two I encountered (the first one being more of an issue for me at least):



* **Lack of HiDPI support**. Linux desktop environments seemingly (or at least consistently) [haven’t caught up with the high-resolution displays released](https://www.reddit.com/r/linux/comments/n05z7k/why_is_hidpi_support_on_linux_still_so_bad/) in the last decades or so.[^6] You can see [an overview on the Arch Linux wiki](https://wiki.archlinux.org/title/HiDPI) (which is famed for being a well-reputed source of Linux-related information). To my knowledge (and as of mid-2021), recent versions of GNOME, KDE Plasma, Xfce and Cinnamon (which I use on Linux Mint) should work okay, but DEs like MATE, Pantheon, Enlightenment etc. may need some more workarounds.

    Regardless, even if the desktop environment does attempt to support it, desktop applications on Linux can use different application frameworks (such as GTK, QT etc.), so you may have to manually pass environment variables ([here’s a random example for OBS Studio](https://obsproject.com/forum/threads/font-scaling-in-the-obs-ui.110176/post-498812)) and other fixes to get them to scale correctly, and even then it may be slightly buggy.



* **Less software support**. Of course, most developers (particularly commercial ones) only make software (such as video games, video editing software, music production software, Outlook etc.) for Windows, so you’ll have to find alternatives that run on Linux.

    Although there are tools such as Wine, Lutris, PlayOnLinux etc.,[^7] and [Valve particularly is pushing development on its own fork of Wine called Proton](https://steamcommunity.com/games/221410/announcements/detail/1696055855739350561) so most of your [Steam](https://en.wikipedia.org/wiki/Steam_(service)) video games can be run out-of-the-box, if you run Windows software using these tools you can encounter performance issues and bugs, so it is always preferable to find native Linux versions, which (although subjective) you might find inferior.


    It’s worthwhile however to point out there is a lot of high-quality and respected open source software equivalents (which you might prefer to use even on Windows compared to their proprietary equivalents), such as [VLC Player](https://www.videolan.org/), [LibreOffice](https://www.libreoffice.org/), [GIMP](https://www.gimp.org/), [Handbrake](https://handbrake.fr/), the amazing [Blender](https://www.blender.org/) etc. so I’m sure you’ll find something (or a workaround at least).

So, which Linux distro to choose? Well, it’s up to you, but **[I highly recommend you read this guide I found on the Reddit subreddit “FindMeADistro](https://www.reddit.com/r/FindMeADistro/comments/5sg4f7/how_to_select_a_distro/)**”. It very clearly goes through the crucial differences between different distros, and gives a few use cases at the end that you may be able to apply to yourself.

But if you’re a complete beginner and you’re not really sure[^8], I’d recommend **a Ubuntu-based distro** would probably be a good choice. I personally recommend **Linux Mint** (which I use) because:



* It has **a Windows-like interface**, the Cinnamon desktop environment (I mean, you could probably get used to it, but I feel GNOME 3 may be initially confusing for a beginner). 
* It is a **Ubuntu-based distro**, so you get all the advantages from that (convenience/being usable out-of-the-box, solutions on the web for Ubuntu will probably work with Linux Mint).
* There are **lots of easy-to-use GUI tools in Linux Mint**, such as the Update Manager, Driver Manager etc. so this nicely hand-holds you into the world of Linux and therefore **you don’t need to touch the terminal at all on a day-to-day basis** (personally I don’t find the terminal - being an aspiring programmer - that scary at all, but these tools will probably let you avoid using it completely[^9])


* There’s **plenty of beginner-friendly help around on the Linux Mint forums** - particularly this [beginner section](https://forums.linuxmint.com/viewforum.php?f=90) - so feel free to ask there if there’s a problem or you’re unsure about how to do something.


## Arch Linux?

I’d like to say first I don’t want to trigger any Arch Linux fans out, but given that it is notably famous, I will mention I personally **wouldn’t recommend it for beginners** (and to be honest - as someone who’s quite busy as a student - even myself), because:



* Arch Linux **heavily focuses on customizability**. There is no easy installer as on Ubuntu or Debian - everything, from partitioning the disks to setting up the desktop environment, has to be done on the initial command-line terminal. If you [follow the wiki](https://wiki.archlinux.org/title/Installation_guide) you’ll probably be able to set up fine, but if you’re expecting an out-of-the-box distro you might be quite frustrated.
* Arch Linux is a **rolling release distro**. I’ll probably do a longer post about it later, but in a nutshell it means software from the repositories is served straight from the authors i.e. upstream (unlike distros such as Debian and Ubuntu which freeze the software, pass it through several stage of testing, and then only apply security patches and (very) minor bug fixes once released). This means you will get the latest software and hardware support[^10], but also the latest bugs, crashes and other random changes. Then again, it’s not definite that you will experience any of this, but it is more likely.

**I’m not saying it’s something that doesn’t have its merits** (for instance, [Valve chose it to build on for SteamOS 3.0 for the upcoming Steam Deck](https://en.wikipedia.org/wiki/Steam_Deck), likely due to its emphasis on customizability and faster updates for drivers etc.) **and as with all Linux distros**, if you have a decent amount of time (and perhaps a spare machine or [a virtual one](https://www.howtogeek.com/196060/beginner-geek-how-to-create-and-use-virtual-machines/)), you can check it out if you’re curious.


## Conclusion

In the end, feel free to have a read around (particularly [recommending that guide I mentioned earlier](https://www.reddit.com/r/FindMeADistro/comments/5sg4f7/how_to_select_a_distro/)) and choose which distro + desktop environment (DE) you like the look of in general and that you feel aligned with its philosophy/release cycle/community best.[^11]

However, I’d like to point out one last thing - **I recommend you keep Windows around at the side** as a kind of “lifeboat” (I still do this myself). You can do this through methods such as [dual-booting](https://www.howtogeek.com/214571/how-to-dual-boot-linux-on-your-pc/), [running Linux in a virtual machine](https://www.howtogeek.com/196060/beginner-geek-how-to-create-and-use-virtual-machines/) or using Linux on a second device. One thing is that you might not like Linux and prefer Windows (which is fine - use whatever you like), but most importantly I think (from experience) that trying to 100% migrate everything that you may do on Windows daily wouldn’t be instantaneous (you’ll have to find equivalent software, maybe find workarounds for bugs or other requirements etc.). **This is particularly important to note if you need to use your computer for important daily work** (e.g. you have to attend frequent virtual work/school/university meetings/lessons). But it might be a nice thing to try out Linux when you have time.


## tl:dr;

If you want to try out Linux as a beginner:



* **Read [this guide](https://www.reddit.com/r/FindMeADistro/comments/5sg4f7/how_to_select_a_distro/) for a good comparison** between the distros.
* If you’re not sure, consider choosing a **Ubuntu-based distro** (I recommend **[Linux Mint](https://linuxmint.com/)**).
* **Keep Windows around in case** you don’t like a distro and/or need to row back (especially if you’ve got important daily work you need to do).

[^0]:
    ["Tux Enhanced"](https://www.gnome-look.org/p/1102260) by Frank Souza (licensed under [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/))

[^1]:
     I mean, there are obviously a large number of resources etc. surrounding Linux, but I found the [TED talk from the man himself](https://www.youtube.com/watch?v=o8NPllzkFhE) really gives a nice overview of how it fits into the bigger picture.

[^2]:

     There are some such as [Red Hat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux) that require a commercial license - although even that has become [free now because of backlash against the discontinuation of CentOS](https://arstechnica.com/gadgets/2021/01/centos-is-gone-but-rhel-is-now-free-for-up-to-16-production-servers/).

[^3]:
     Of course, downloading it in the first place and writing it to a USB/CD may require you to have a computer with another OS installed, but given most OEM laptops have Windows installed as part of the price, you probably have one around.

[^4]:
     And of course, these companies typically associated with more proprietary operating systems and software have also embraced open source in some respects, such as [Google](https://opensource.google/), [Microsoft](https://opensource.microsoft.com/), [Apple](https://opensource.apple.com/), [Facebook](https://opensource.fb.com/) etc.

[^5]:
     Even Microsoft uses Ubuntu on its four supercomputers!

[^6]:

     To be honest, even companies that make proprietary OSs struggle with this as well apparently.

[^7]:

     To be clear, the latter ones all use Wine (or are compatible with forks such as Proton), but they make it much easier to use Wine which can be quite difficult to configure.

[^8]:
     Actually, if the [amount of choice available](https://upload.wikimedia.org/wikipedia/commons/8/8c/Linux_Distribution_Timeline_Dec._2020.svg) is causing you to "distro-hop", I recommend watching [this video](https://www.youtube.com/watch?v=3zpgQpdy_fI). You don’t have to watch it all (I only watched the first few minutes) but the critical parts in my opinion are roughy 1:52 to 2:09, and 2:51 to 3:20 - it basically says you **don’t need the find the "best" distro** (because it doesn’t exist), you just **need one to get the job done (i.e. your day-to-day work)**. If there is a big problem that you can’t work around **then you can switch**, but **otherwise stick with the one you currently got.**

[^9]:

     I mean there might be a problem that does require you to use it, but I’m sure the people on the Linux Mint forums will guide you through it, and Linux Mint is pretty stable so you’re unlikely to encounter them.

[^10]:

     Note it’s not as black-and-white. Ubuntu realised this newer hardware support problem and provides [a newer kernel via what they call the "Hardware Enablement Stack"](https://askubuntu.com/questions/248914/what-is-hardware-enablement-hwe) (and I guess you could try to drop one in yourself in any stable distro anyway) and newer software can be brought in on a stable distro via [backports](https://backports.debian.org/) or through new technologies such as [AppImages](https://appimage.org/), [FlatHub](https://flathub.org) and [Snaps](https://snapcraft.io/) ([although the last is controversial](https://www.reddit.com/r/linux/comments/j3ajnf/whats_wrong_with_snaps_why_so_many_people_hate_it)).

[^11]:
     I know on most distros other DEs than the default can be installed later, but some distros will work with and look better with certain DEs (e.g. Cinnamon is heavily customised for Linux Mint), and switching will probably be inconvenient as configuration files that multiple DEs might share would interface with each other.

