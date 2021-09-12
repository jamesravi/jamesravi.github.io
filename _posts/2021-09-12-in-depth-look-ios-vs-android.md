---
layout: post
title: An in-depth look into Android vs. iOS, in terms of security and freedom
excerpt: <p>We're going over the differences between the two with a very fine comb, but as you'll see, neither is perfect.</p>
tags:
  - main post
---

<img src="{{ site.baseurl }}/images/iphone-android-chess-battle.jpg">
*The battle of the duopoly* [^0]

&nbsp;

Now, in this post I’m going to dive into the whole rabbit hole of benefits and problems surrounding the two dominant players in smartphones today - **Android and iOS** - and whether there are any solutions in sight. We’re going over this with a very fine comb, so be prepared to brace yourself - **if you’re running short of time, don’t worry**, I’ve put an (admittedly vague) **conclusion at the end**, but as you are about to see (as with many things), **neither is perfect.**

**As a disclaimer before we start** - due to my perhaps soft heart for open source (although I’d think you would agree is definitely beneficial for all), **I do lean towards Android, but the irony is that I still begrudgingly use iOS devices** - you’ll probably see why but I’ll explain at the end anyway.


## iOS

Let’s start with iOS. To give credit to Apple, because they control all the hardware and software, they **will keep providing all security patches for your device** - but **only if you are running the latest major iOS version**. If you are not, you don’t need to worry too much, but [Apple **will only provide updates for severe vulnerabilities**](https://apple.stackexchange.com/questions/223170/what-is-apples-policy-for-supporting-security-updates-on-older-versions-of-ios) (such as against exploits in Safari) for iOS versions near to the latest one. In a sense, **[you might be more vulnerable if you are on much lower iOS versions](https://security.stackexchange.com/questions/135781/does-apple-backport-fixes)** (as Apple probably will presume most people will use the latest version for their device and not care to backport fixes too far) but **upgrading might [cause you to lose performance and more “stronger” jailbreaks](https://www.reddit.com/r/LegacyJailbreak/comments/li4te8/question_should_i_downgrade_ipad_3_from_935_to_841/gn15brz)** (such as those that use untethered exploits)[^1]

However, this control, although opinions may vary on this, comes at a cost in freedom. **Non-jailbroken iPhones can only download software from Apple’s curated App Store** - a “walled garden” in a sense (there’s [a nice explanation applying this analogy on Reddit](https://www.reddit.com/r/explainlikeimfive/comments/9qsbo8/eli5_what_is_a_wall_garden/e8blw0y)). Of course, the reasoning for this is so Apple can check apps are safe before offering them to users (instead of checking them yourself as on Windows or Android[^2]), and although the App Store does contain quite a lot of software, there is **a perception that Apple uses this in an additional way to reject apps that they don’t like.** For instance, **you cannot easily get software like emulators on iOS** (on Android, you can simply sideload them, but [Google seemingly does allow them on its Play Store, such as RetroArch](https://play.google.com/store/apps/details?id=com.retroarch)). Apple has faced criticism over its treatment of third-party developers from companies such as **[Valve](https://www.gamasutra.com/view/news/318850/Valves_Steam_Link_app_blocked_by_Apple_due_to_business_conflicts.php), [Basecamp](https://www.hey.com/apple/) and [most famously Epic Games whose lawsuit brought a massive amount of revelations](https://www.theverge.com/22611236/epic-v-apple-emails-project-liberty-app-store-schiller-sweeney-cook-jobs), shedding light on Apple and even other notable companies in the technology and game industries as a whole.**

&nbsp;

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/euiSHuaw6Q4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
*Epic parodied [Apple's famous 1984 advert](https://en.wikipedia.org/wiki/1984_(advertisement)) as it filed its lawsuit, alleging Apple holds a monopolistic position over its App Store.*[^21]

&nbsp;

I’d also point out that unlike Android[^3], **you cannot use custom ROMs or other operating systems on iOS devices.** This is because Apple employs **[a chain of trust](https://support.apple.com/en-gb/guide/security/secb3000f149/web) as a security measure during booting** that ensures each successive stage that runs is signed only by them.[^4] The very first stage is **written directly to the [ROM chip (Bootrom)](https://www.theiphonewiki.com/wiki/Bootrom), so it cannot be modified.[^5]** In theory, you could [boot another OS using a semi-tethered exploit](https://wiki.postmarketos.org/wiki/Apple_iPhone_7/7%2B_(apple-iphone7)) such as [checkra1n](https://checkra.in/) (but as the name implies, you need to have the iPhone connected to a computer to exploit it while it is booting, which is quite inconvenient).[^6][^7]

In response to iOS’s walled garden, a lot of users “break out of this jail” using community-developed **jailbreak** exploits. **Jailbreaking is [certainly legal, at least in the US](https://en.wikipedia.org/wiki/Jailbreaking_(iOS)#United_States)**,[^8] [despite Apple’s resentment to jailbreaking](https://support.apple.com/en-gb/HT201954) (and continuous cat-and-mouse patching with each new version) and it does allow you to have more freedom and control over your device like those who use Android. 

There are some, like Apple, that say jailbreaking is a potential security risk, and while I do agree that **if you remain on lower iOS versions[^9], you might be more susceptible to vulnerabilities that would have been patched** (although there wouldn’t be that many), and perhaps there is [some debate over the quality of some jailbreak exploits](https://www.reddit.com/r/jailbreak/comments/8wu4q9/discussion_can_we_speak_about_people_who_are/) (although to be honest I don’t think they would weaken the device to remote exploits at all, and jailbreak authors are simply trying their best to get around iOS’s security measures), it seems the risk of jailbreaking only simply allows the user to install untrusted software, and that **in itself isn’t really an issue with jailbreaking** but more **on the user to be wary of what they install** (especially from piracy or “cracked” repositories), just like on Windows and Android.

It’s also prudent to acknowledge **government-backed tools such as the [Pegasus spyware](https://en.wikipedia.org/wiki/Pegasus_(spyware))**, which has been receiving [considerable press coverage recently](https://en.wikipedia.org/wiki/Pegasus_Project_(investigation)).[^10] iOS is closed source, which means third-party researchers find it harder to find and report security issues. Google’s Project Zero has **[criticised Apple for being less accommodating to researchers](https://9to5google.com/2020/07/22/google-project-zero-ios-srd/) and [lax on iOS security](https://googleprojectzero.blogspot.com/2019/08/a-very-deep-dive-into-ios-exploit.html)** in general. It’s debatable, but it is concerning that [Apple’s BlastDoor service in iOS 14](https://googleprojectzero.blogspot.com/2021/01/a-look-at-imessage-in-ios-14.html), designed to protect against the zero-day iMessage exploits Pegasus was using in iOS 13, **clearly [isn’t working since Pegasus can still infect a fully updated iPhone on iOS 14.6](https://twitter.com/billmarczak/status/1416801637104902146).** Then again, given the [difficulty and cost of finding or obtaining these zero-day exploits](https://www.reddit.com/r/OutOfTheLoop/comments/opzpd2/what_is_going_on_with_pegasus_project/h6a9ssz/), it’s probably not a concern for the average user. But in the end, such incidents are leading to a general shift in opinion: that **[Android may actually be slightly more secure than iOS](https://www.wired.com/story/android-zero-day-more-than-ios-zerodium/)** (although you'll see the catch with this later)


## Android

Android, on the other hand, is **much more open**. [Android itself is an **open-source project** licensed under the permissive Apache License, and is bundled with the Linux kernel where Google’s patches to it are under GPL](https://source.android.com/setup/start/licenses).[^11] This means that anyone, particularly those in the cybersecurity industry, can **readily look and examine the code for security issues and other problems**, and **even contribute to Android themselves**.[^12]

**A lot of people consider Android to be insecure, but this seems to be a common misconception.** Android, unlike iOS, simply allows you to download and install (“sideload”) random apps from anywhere (once you’ve enabled a setting at first usually). Admittedly, [some malicious apps have been found on Google’s Play Store](https://www.zdnet.com/article/malicious-apps-on-google-play-dropped-banking-trojans-on-user-devices/), but even Google can’t validate them all ([as can’t Apple](https://en.wikipedia.org/wiki/XcodeGhost)), **the user should probably treat less known applications with caution before installing them** (as on Windows and other platforms), sandboxing measures in both iOS and Android should reduce the impact (though as we’ve seen with Pegasus and self-root/semi-untethered jailbreaking apps, these can be bypassed through vulnerabilities), and **both iOS and Android have measures to monitor and remotely remove malware from your phone** - as seen with [Google doing so with the Pegasus version on Android which they nicknamed “Chrysaor”](https://android-developers.googleblog.com/2017/04/an-investigation-of-chrysaor-malware-on.html).[^13]

Being a more open platform brings many other benefits as well, which I’ll list here in comparison to iOS:



* **Developers can make apps on Windows, Linux and MacOS for Android** using [Android Studio](https://developer.android.com/studio). **For iOS, you can only officially make apps on MacOS** since [XCode](https://developer.apple.com/xcode/) is only available there. There might be ways to make iOS apps using [the community SDK for jailbreaking called Theos](https://iphonedev.wiki/index.php/Theos), but I’m doubtful Apple will allow them into its official App Store if they are aware they’ve been made using it.
* **Developers can freely distribute apps on Android outside of the Play Store**, and if they want to release it on the Play Store anyway, it’s only [a one-time fee of $25](https://www.androidauthority.com/publishing-first-app-play-store-need-know-383572/) (for iOS, to release an app on the App Store you [must pay **a $99 subscription per year**](https://developer.apple.com/programs/how-it-works/), and you **officially sign the app on a Mac** ([although there are ways around that apparently](https://stackoverflow.com/questions/18739387/build-an-ios-app-without-owning-a-mac)). This is probably fine for most businesses who can afford it, but for open-source developers - such as the ones who made [the IRC client Mutter, which ceased development a while ago for presumably this reason](https://www.reddit.com/r/irc/comments/d3y75s/are_there_any_free_open_source_irc_clients_for_ios/f05ybf7) - and hobbyists it’s very cost prohibitive, and it’s why most iOS apps are more likely to be paid apps, or utilise in-app purchases and adverts. That’s why **on Android you readily get lots more cool stuff** such as [emulators](https://www.retroarch.com/index.php?page=platforms)[^14] and my favourite - [**F-Droid**, a large collection of **free and open-source applications**](https://www.f-droid.org/) that are safe[^15] and warn you of issues such as privacy before installing them.


* For Android, **apparently you can install third-party applications to better secure your phone** (of course, in a sandbox [these antivirus apps are utterly useless. Don’t really buy into them](https://www.howtogeek.com/232436/android-has-a-big-security-problem-but-antivirus-apps-cant-do-much/), especially more on iOS, but in general they are quite ineffective - and, in the end, it’s more effective to be careful what you install in the first place). [I speak more for **professional solutions that will probably affect the phone on the OS level**](https://www.forbes.com/sites/zakdoffman/2021/03/16/iphone-12-pro-max-and-iphone-13-not-more-secure-than-google-and-samsung-android-warns-cyber-billionaire/) such as those that run as root or patch the phone directly. Although I haven’t used them myself (so I can only speculate), it seems it would be **way easier on Android than iOS** to do this sort of thing due to **Android’s open nature**. **With iOS you are more 100% reliant on Apple to secure your phone** (and with things like Pegasus this can be a concern).

And finally I should mention (although you can probably guess), **Google happily gives the code away to all kinds of manufacturers such as Samsung, OnePlus, Sony etc.** to use as long as they are part of [Google’s Open Handset Alliance](https://en.wikipedia.org/wiki/Open_Handset_Alliance) (and even those who don’t want to join, such as Amazon, **[can still use Android due to its open-source license for their devices](https://en.wikipedia.org/wiki/Fire_OS)**).

Now, you’re probably wondering, what’s the catch? **Fragmentation is the catch, my friend.**

<img src="{{ site.baseurl }}/images/android-fragmentation-everywhere.png">

Fragmentation is probably the reason that Android is the most installed OS of all time (and fragmentation probably isn’t a bad thing in a sense that it allows you more choice), but it does lead to **severe problems with updates (more importantly security ones)**.

Basically, for Android, **Google hands the code through [like 5 different companies](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/)** who all modify it so it runs on the final device. So, essentially, **there’s probably hundreds if not thousands of forks of Linux** (with proprietary binary drivers etc.) **for each individual Android device**. Passing through updates, such as security ones, through that chain will be slow, and worst of all, when one of those companies decides it is no longer financially viable to support your device, **updates will completely stop**. There’s an estimated one billion Android devices, vulnerable to publicly known exploits such as [KRACK](https://en.wikipedia.org/wiki/KRACK) and [Dirty COW](https://en.wikipedia.org/wiki/Dirty_COW) and [Stagefright](https://en.wikipedia.org/wiki/Stagefright_(bug)) (and almost certainly dozens of vulnerabilities in default web browsers on the device and other programs). I mean, in theory, if you’re extremely careful, you might be okay, but it’s like walking on eggshells, and it’s much better if you get a new phone immediately.[^16]

Google is **trying to improve the situation with things like [Project Treble](https://source.android.com/devices/architecture#hidl)**, although [some do criticise](https://postmarketos.org/faq/#can-project-treble-help-postmarketos) that [the kernel and firmware do not receive any further updates](https://ollieparanoid.github.io/post/security-warning/#outdated-firmware-threatens-old-smartphones), and that older devices (unless supported by the community) never get the chance to experience Project Treble. Still, it is bringing out [faster updates for certain phones](https://www.androidcentral.com/project-treble-working-even-if-android-updates-dont-all-come-day-one) (for at least the OS component) and now has brought [generic custom ROMs](https://github.com/phhusson/treble_experimentations/wiki) that work with many devices, which is nice.


## Linux on smartphones?

To note, **Android phones do have the ability to use custom ROMs** like [LineageOS](https://lineageos.org/) (it depends on the phone in general, although [Google and OnePlus phones tend to have the best support](https://www.reddit.com/r/fossdroid/comments/ewd3rs/the_best_custom_rom_supported_phone/) apparently), but the ideal solution for supporting running Linux would be if all Android OEMs[^17] release the source code for the drivers on their phones,[^18] but of course all(?) of them do not.[^19] The good news is that there is **a community project called [postmarketOS](https://postmarketos.org/)** which is seeking to bring mainline Linux to old devices and therefore fix the Android longevity problem, [among others](https://cascardo.eti.br/blog/GNU_on_Smartphones_part_II/).

Personally, to be honest, I don’t mind sacrificing the higher quality (although it is subjective) that comes with iOS or Android for the true Linux freedom on a device - the only issue is that **[support for phone by phone varies](https://wiki.postmarketos.org/wiki/Devices)**, and even the [PinePhone](https://en.wikipedia.org/wiki/PinePhone) which is made to support mainline Linux **[isn’t up to the reliability of Android and iOS phones](https://www.reddit.com/r/PINE64official/comments/m9kc82/is_the_pinephone_a_suitable_daily_driver_yet/grnzaxc).** I’m not sure if it is down to either the hardware (as [this Reddit comment](https://www.reddit.com/r/PINE64official/comments/njjdfb/considering_of_buying_pine64_phone/gz7v296) and [this other Reddit comment](https://www.reddit.com/r/PINE64official/comments/n5xrwk/pinephone_thoughts/gx3ymhq) seem to imply) or the software ([as this review seems to suggest](https://boilingsteam.com/the-pinephone-can-it-replace-your-smartphone/)). Nonetheless, **it is very encouraging to see a community who is aware of the issues that face iOS and Android today trying to provide the ideal solution.**


## Conclusion (tl;dr)

In conclusion, though, then again it is up to you. It seems possible that **Android is slightly more secure (and certainly more open) than iOS** due to the former’s open source nature, but sadly, **much of this is negated by the poorer flow of updates received on most Android phones**. It’s exactly why I use iOS, because despite where I look, it seems unfortunate that Android phones ([even those reaching $1,000](https://www.reddit.com/r/Android/comments/grlik7/two_years_of_software_updates_is_no_longer_enough/) and [those being supported by Google directly](https://support.google.com/pixelphone/answer/4457705)) only get at least two years in updates, which pales in comparison to iOS devices reaching around six years (such as those released in around 2015/2016 still receiving updates today).

If you want something usable and reliable (more importantly, in calling and texting) at the present, you’ll have to pick between **iOS (less freedom[^20] and more expensive but with longer update support)** or **Android (more freedom and cheaper but with shorter update support).** Linux-based community efforts are encouraging, but they are not usable yet as a daily driver for most people (but hopefully they will be one day).

[^0]:
    ["iPhone vs Android"](https://www.flickr.com/photos/nrkbeta/3905907831) by NRKbeta / Marius Arnesen (licensed under [CC BY-SA 3.0 NO](https://creativecommons.org/licenses/by-sa/3.0/no/))

[^1]:
     By the way, if you did want to downgrade your old iOS device for jailbreaking purposes, there is [a tool on GitHub to do so](https://github.com/LukeZGD/iOS-OTA-Downgrader).

[^2]:
     On how to actually check them yourself, I’ll probably write another post about that - but basically, you can use websites such as [VirusTotal](https://www.virustotal.com). Note they’re not perfect - they might give false positives, or [sometimes even give a clean result even if what you’re scanning is malware](https://www.howtogeek.com/howto/30508/make-sure-downloads-are-safe-before-downloading-them/), but it’s a good rule of thumb anyway.

[^21]:
    It's controversial, but I have to give credit to Epic Games for this [clever move of irony, reframing Apple into the position it believed IBM were in 1984](https://www.polygon.com/2020/8/13/21367803/fortnite-1984-apple-app-store-epic-lawsuit-commercial-short-video). Interestingly, the NSA [also made the same comparison](https://9to5mac.com/2013/09/10/nsa-references-original-macintosh-ad-in-calling-steve-jobs-big-brother-and-iphone-owners-zombies/) privately, although perhaps for different reasons.

[^3]:
     Well, it’s easier on some Android devices than others, but definitely not near-impossible like on iOS devices.

[^4]:
     Fun fact: this is why you need to resign apps every week on newer jailbroken devices, because Apple utilises signing everywhere for software on iOS (more specifically, jailbreakers utilise development certificates to get around these signing measures, which is why they expire after a week). There are tools such as [AppSync Unified](https://cydia.akemi.ai/?page/net.angelxwind.appsyncunified) and [AltStore](https://altstore.io/) that negotiate around this in a way, but you can see it is more cumbersome than Android.

[^5]:
     Nice thing however is that even Apple can’t modify it, so jailbreak exploits from it such as the famous [checkm8](https://arstechnica.com/information-technology/2019/09/developer-of-checkm8-explains-why-idevice-jailbreak-exploit-is-a-game-changer/) cannot be patched.

[^6]:
     I’d like to point out there is [this awesome open source virtual machine app called UTM](https://getutm.app/) that allows you to run virtual machines with OSs such as Linux distributions or even Windows itself on iOS, but unfortunately for me [it only supports iOS 11 and above](https://github.com/utmapp/UTM/issues/405), so much like older Android devices and their updates my older iPad 3 will never see it :(

[^7]:
     Also for another thought - I wonder if you have an untethered jailbreak that perhaps you could boot into another OS from perhaps a partition on the device? It wouldn’t be perfect as you would have to boot into iOS anyway first which is annoying, but would it be possible? It feels similar to vein to asking whether it would be possible to switch execution and boot into a Linux distro while Windows is running (perhaps by killing off Windows processes). If I had more experience I would try it, but I wonder if it is possible.

[^8]:
     To be honest, I’m more amazed Apple somehow hasn’t taken legal action against Cydia for selling paid iOS apps and tweaks outside the App Store, given that Apple is quite willing to take legal action against companies for issues such as [source code leaks](https://www.theregister.com/2018/02/13/apple_github_iboot/) and [iOS virtual machines](https://www.theverge.com/2021/8/11/22620014/apple-corellium-security-virtual-iphone-dmca-lawsuit-settled), and Apple would certainly be aware of Cydia’s existence if not before [by its own lawsuit against the perceived iOS monopoly](https://www.theverge.com/2020/12/10/22167964/cydia-sues-apple-monopoly-anticompetitive-iphone). Perhaps paid iOS “homebrew” is legal?

[^9]:
     I believe updating is possible if you are jailbroken, although you have to wait for a jailbreak for the updated iOS version if there isn’t one available (since semi-untethered jailbreaks do not survive a reboot)

[^10]:
     If you are interested in reading more about Pegasus, [Citizen Lab](https://citizenlab.ca/tag/pegasus/) (who discovered it in 2016) has some excellent articles on it and the people affected. There’s also [this Reddit comment](https://www.reddit.com/r/OutOfTheLoop/comments/opzpd2/what_is_going_on_with_pegasus_project/h6avn1e/) which I found gives a nice balanced and wide overview surrounding the nature and origin of these tools.

[^11]:
     If you’ve confused by how Google is allowed to do this, my understanding is that Android is a program that runs on top of the Linux kernel and is not combined with it - [there’s a GPL exception in the Linux kernel for the syscall interface anyway](https://github.com/torvalds/linux/blob/master/LICENSES/exceptions/Linux-syscall-note). There are a lot of proprietary legal applications that run on Linux such as Steam and Microsoft Teams, so in a sense Android is legal.

[^12]:
     Some argue that the source code being public means that it is easier to find vulnerabilities in Android, but in my opinion that’s a good thing, because they can be patched quickly. The security of an operating system should never depend on its code being private - trying to do this is called “[security through obscurity](https://en.wikipedia.org/wiki/Security_through_obscurity)” - and it seems unanimously people agree it is a bad idea, as [exemplified by open source projects such as Debian](https://www.debian.org/security/).

[^13]:
     You can also see Google’s willingness to embrace third-party security researchers more readily than Apple, given that they [have uploaded Chrysaor binaries to VirusTotal (at the bottom of the post)](https://android-developers.googleblog.com/2017/04/an-investigation-of-chrysaor-malware-on.html). They even notified those who had been affected, unlike Apple.

[^14]:

     Yes, as a side note, it’s unbelievable that RetroArch supports this many platforms. Even though obviously on consoles it requires similar “jailbreaking” exploits to those on iOS to install homebrew like this, it blew my mind when I first saw that page.

[^15]:
     Almost certainly, at least, because in a similar vein to default software repositories on Linux distributions all the applications have open source code, so they can be checked by others and built into binaries on the servers themselves.

[^16]:
     You can see this isn’t good for e-waste either. Some would also say that the [slowing down of iPhones with newer software updates](https://en.wikipedia.org/wiki/Batterygate), but at least they last for longer in theory: iOS devices seem to last around 6 years, while Android devices such as those from Google may reach 2 years if you are lucky.

[^17]:
     I guess blame could be placed on OEMs for heavily customising Android for their devices (in the sense that they burden themselves to maintain their forks more rather than using features present in “mainline” Android/the Linux kernel), but some are also [shifting some blame onto Google](https://www.reddit.com/r/Android/comments/grlik7/two_years_of_software_updates_is_no_longer_enough/fs0c5gt) in the same vein.

[^18]:
     And also if there was [some standardised BIOS/UEFI for ARM like on PCs](https://www.reddit.com/r/AndroidQuestions/comments/mk3k3z/why_is_android_so_locked_down_compared_to_linux/gtdouq0?utm_source=share&utm_medium=web2x&context=3), but maybe that’s asking too much.

[^19]:
     Fun fact: given that Android uses the Linux kernel, and that the Linux kernel is licensed under GPL, in theory you can [legally ask your Android OEM to give you the source code for the kernel](https://www.xda-developers.com/oems-and-gpl-compliance/) because they obviously distribute the kernel as part of the phone.

[^20]:
     Of course, as mentioned, you can jailbreak, but as Android is more accommodating to openness in general it is considerably better in this regard, such as in terms of the amount of possible software.

