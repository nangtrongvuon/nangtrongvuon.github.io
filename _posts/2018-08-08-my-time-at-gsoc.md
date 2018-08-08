---
layout: post
title:  My time at GSoC
date:   2018-08-08 9:00:00
---

## Before GSoC 2018
I really wanted to write about my time with the Google Summer of Code program, specifically, working under the Xi Editor project. It's been quite the long absence since my last blog post, but here goes anyway.

Ever since I was little, I spend most of my time on the computer. Being a poor kid from a third world country, my family couldn't afford things such as games or software beyond the initial computer purchase. I remember feeling very amazed when I found out about open source projects. How can such good and useful software be free? I spent my childhood pondering that question. To me, open source software, projects such as Linux, 7-Zip, VLC were projects of passion, built mainly by people who loved the art of developing good software, and were willing to share it with the world.

My last 10 years of life was inspired by this way of thought, and it continues to guide me until this day. When I first heard of GSoC in 2016, I really wanted to be part of the open source community, but its project were daunting, and being the scaredy freshman I was in college, I quietly watched as the chance slipped away. After that, I started to take learning software development much more seriously, hoping one day I could contribute something useful, and leave my mark on the community.

I found about Xi Editor during 2017, when a post about Raph Levien and Xi Editor hit Hacker News. At the time, I remember hating Atom for its sluggish performance and high battery consumption, and being the nerd I was, I wanted to have the newest and coolest tools. Seeing all the promises of performance and native UI implementation lured me into downloading macOS's Xi. Much to my disappointment, many of the features I've grown used to with Atom weren't available, such as code completion, or quick help highlights, or the rich ecosystem of plugins that Atom had access to. Even though I didn't really catch on to Xi at the time, seeing that it was written in Swift, which is a language I've grown really accustomed to having dabbled in iOS greatly, gave me hope that one day I could also contribute to it.

## My journey with Xi
Early 2018, I saw Xi Editor on the GSoC 2018 Project list. Deciding to try my luck and dive into the scary world of open source, I posted my first message on #xi, the IRC channel on which discussion of Xi's development happens. I was welcomed by Colin (@cmyr), who guided me gently through my first feature contribution to Xi-Mac, [the error log](https://github.com/google/xi-mac/pull/151) (which lives in master even up to this day!) This started my journey with Xi-Mac, and I decided to finally apply for GSoC, for Xi Editor's **"Improve Xi-Mac’s UI and polish its core editing experience"** project. With help from Colin, I polished my proposal and had it submitted to the organization. Xi approved me, and we were set for the summer! It wasn't a very hard project, speaking from a purely software engineering perspective, but I was ready, and it was one of the few ways I knew how to help.

I had a very long list of things I wanted to do, such as split views or navigation views. Colin knew better, and cut it down to just 4 major projects - a status bar, a hover view (where you can see what a symbol is in a code editor by hovering on it), a goto definition view (where you can go to the definition of a chosen symbol in code), and the autocompletion view. Eager to prove myself, I was initially slightly discontent, but I soon found out why Colin made that decision.

It's probably good to mention that before Xi, I had no experience with developing on macOS. I've been doing iOS quite a bit up until that point, but I had done no macOS whatsoever. The challenges were clear - macOS/OSX had much less user base and thus less resources, be it documentation, updated APIs or Stack Overflow questions, Of course, the semantics for both UI and UX on a desktop environment is much different than a small phone. When I started to work on the status bar, I had huge trouble just having a white rectangle on the screen. However, with my novice understanding of Swift, I was able to dive into AppKit and make progress.

The status bar project went relatively smoothly in my opinion, and it was when I started to really get an understand of macOS development. An `NSView` wasn't really a `UIView`, but Swift was just still Swift, so I didn't have too much trouble here. However, I had to quickly change my haphazard development practices such as writing overly long commit messages to frequently pushing in bad code (to be honest, I still do this, but I try my best to keep in down!) after starting to work on Xi. I began to learn to think like a real engineer, to break problems in small portions and to think of all the possibilities that could happen and how the user would interact with the feature. After much struggle, I was eventually able to get [my status bar](https://github.com/google/xi-mac/pull/183) merged! Hooray!

Next was tackling hover and goto definition. Both of these were well known LSP features, and many editors have been supporting them for a long time. With support for Hover, Goto Definition and Autocomplete, Xi-Mac would once again turn into the flagship client for Xi. With these projects, I worked closely with Pranjal (@betterclever), another GSoC student working on Xi for the LSP features project. He worked on the LSP features on Xi-Core, which would eventually get support in frontend clients, starting with Xi-Mac. 

Going beyond a simple status view, I began to dive more in depth into AppKit development, as I learned about `NSPopover`, `NSViewController`, and the many interactions and commands Mac apps tend to support. Me and Pranjal started to collaborate on hover, and with Colin's guidance throughout, we got [hover working in Xi-Mac](https://github.com/google/xi-mac/pull/228). Even though currently hover and goto definition is still quite rough around the edges, we at Xi already learned alot from implementing these - A lot of nuances that covered Xi's implementation of things such as the core and client relationship began to surface upon interaction with many LSP features.  

## Beyond GSoC
Now, nearing the end of GSoC, as expected with the original workplan, right now I'm doing my finishing touches on the initial UI implementation for autocomplete. The base support has already been done, and now it still needs a bit more polish before it can get reviewed and merged.

Overall, being with GSoC and the Xi Editor Project was a very meaningful and enjoyable experience. After all, growing up as a little kid admiring all those cool programs, I can now proudly say I'm part of that world too - the open source world. I'd also like to specially mention Colin, eagerly acting as my guide throughout every step of the way. Colin nudged me towards the right direction when I was stuck, shed insights on Xi code and practices in software engineering in general, and be there when I really needed it. To me, my period working with Colin has been the period where I've learned the most so far throughout my short beginnings as a software developer. Going through a project with a mentor at your side, that's something I think the modern software world needs more of. I believe that out of everything, *this* is worth passing on.

Of course, GSoC ending doesn't mean I'll stop contributing to Xi - as far as I can see it, I'll still stick around as a contributor for quite a while longer. There's still much work to be done, after all, and I'm just getting started.

## Contributions under GSoC

### Xi-Mac
* **Status Bar** - [https://github.com/google/xi-mac/pull/183]
* **Status Bar tracks plugin items** - [https://github.com/google/xi-mac/pull/210]
* **Hide Status Bar when showing no items** - [https://github.com/google/xi-mac/pull/211]
* **Hover View** - [https://github.com/google/xi-mac/pull/228]
* **Small Xi-Mac Refactors** - [https://github.com/google/xi-mac/pull/214]

### Xi-Core
* **Tests for refactor** - [https://github.com/google/xi-editor/pull/620] 
* **More refactor tests** - [https://github.com/google/xi-editor/pull/623]
* **Send RPC notification on config_changed** - [https://github.com/google/xi-editor/pull/671]
* **Add status bar RPCs** - [https://github.com/google/xi-editor/pull/677]
* **Include plugin name with RPC** - [https://github.com/google/xi-editor/pull/725]

