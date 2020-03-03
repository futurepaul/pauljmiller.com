+++
title = "How to fix the internet"
slug = "how-to-fix-the-internet"
subtitle = "A subjective definition of fix"
date = "2019-06-20T00:45:59.324310806Z"
+++

Here's my idea in a nutshell: make it more like WordPress. Take any popular service you use from The Big Bad Tech Boys and make it more like WordPress.

I'm giving you the least glamorous version of my idea up front to build trust. Is it working? Please don't leave. I understand that very few people love WordPress, especially not the people who work with it on a regular basis. WordPress is slow, old, bloated, complicated, and historically insecure.

Also, WordPress powers roughly 30 percent of the top 10 million websites. So not only is my idea bad, it's also the status quo.

But!

What if stuff was more like WordPress?

Let's say I want to start a new YouTube channel. But instead of starting it on YouTube, I start it à la WordPress.

1. I buy a domain name, or [use one I already own](https://elephantnames.com).
2. I set up hosting and connect it to my domain.
3. I install a YouTube-like CMS on my server (instead of WordPress).
4. I add videos, information, and design tweaks to the channel.
5. Nobody ever discovers my videos because they're not on YouTube.

Okay, so step five sounds disheartening. But we could solve this the way podcasts solved it: apps!

See, podcasts are like WordPress blogs. In fact, many podcasts that are hosted DIY, instead of through a platform like SoundCloud or Anchor, publish via WordPress.

A podcast is just:
1. An RSS feed.
2. A set of MP3s.

It turns out, it's really straightforward to write an app that can subscribe to RSS feeds and play MP3 files. Hence the proliferation of podcast-listening apps.

So if our WordPress-like YouTube replacement was just:
1. An RSS feed.
2. A set of videos.

We'd be doing pretty well, yes?

This is where we get to the inevitable: "That sounds like an obvious idea. If it were also a _good_ idea, it would've already been done. Therefore it must not be good."

Maybe.

Or perhaps we haven't had the incentive to self-publish our own video channels before now. YouTube was a good enough. The upsides, like discoverability and monetization, far outweighed the downsides: not owning your own distribution, a capricious algorithm, Google's discretion as to what's appropriate.

Hosting the videos is expensive, especially if we want anything close to the low latency and high quality of YouTube. And there's very little incentive to build a high quality app for these video channels because they don't exist (a classic chicken / egg scenario).

Also, for some reason, Google is the only company on earth with the budget to create a really good video player for the web.

### Fast-forward to the year 2025

There are many well-established content types. Just like .txt / .doc / .png, except for things like .tweet, .podcast, .video, .blog.

When I want to publish some content, let's say a video, I use my favorite app to package it into a standard .video file. That file is basically just the real video file, plus any metadata the .video format requires, such as title, description, etc.

I publish "paul-minecraft-lets-play-episode-4190.video" to my home server. My home server is just a black box in my closet that's plugged into power and ethernet.

My home server updates a list of .video files with the hash of my latest .video file and serves this file (like an RSS feed, except in the year 2025 maybe we don't use XML anymore). If I'm a very popular video creator, my home server seeds the video to a bunch of CDNs that serve the bulk of traffic. If I'm very controversial (I always dig straight down), perhaps my videos are only torrented. Or if only my mom watches my Let's Plays, she can probably load the video directly from my home server without a problem.

A subscriber is notified of my upload on her phone, because in this fantastical future, if you subscribe and click the bell icon, notifications actually work. She opens her app of choice for consuming this content. It might be an app focused only on .video subscriptions, or an app that can handle many different content type feeds.

If she likes the video, she can click the "fav" button and leave a comment, just like in the year 2019. But her fav and her comment aren't published to my server, or to a central server like YouTube, they're published to her server. A .comment file, a .liked index.

Insofar as the videos and other content she enjoys are presented to her via algorithm, it's an algorithm she chose herself that runs on her own server against her own data.

Someone who follows her .video channel, or her .blog channel, might be more likely to see my video in the "Other recommended channels" list. Or not! It's up to her. My server is simply notified that she's published a comment, and I can publish a reference to her comment without hosting it myself.

### Some notes of clarification on what the future's like

I think what we'll see very clearly in hindsight is that when we published our content on other people's servers, it always went bad. Instagram's algo made us sad. YouTube's algo made us mad. Twitter's algo mad us sad AND mad. Google Photos algo, it turned out, made us easily tracked and controlled by totalitarian governments. Oops!

Self-hosting will be the "difficult" and "cumbersome" option for a while, but by the year 2025 it will be easier than the centralized services are. Think about it: have you ever tried to upload a YouTube video? There are a ton of options, and the interface is kind of annoying, and it's a many-step process. This is because YouTube has to be designed to be a jack of all uploading trades, master of none. But when self-hosting is mature and common, you'll be able to pay for a highly specific app that streamlines the experience to match your exact needs. If you don't want to pay for a high-end app there will likely be a more general, harder-to-use, free and open source option as well.

And: any things that _are_ difficult about self-hosting are directly related to self-determination. "Nobody is obliged to host your shitty Let's Play. It's two gigabytes. You swear a lot, so we can't use it to sell soap. Four people watch it. And three of those people hit the thumbs down button." Correct.

What about popular, non-controversial content? Does this system work for that? "Caching is a hard problem" is something you might've heard. I don't think we'll have a perfectly decentralized internet by 2025 that can outpace high quality CDN services. But I do think we'll have new ways to pay CDNs for their service. A big company who wants its detergent ad seen by millions with a low buffer time might pay CDNs up front. But barely monetized user-created content might be mirrored by CDNs in exchange for some kind of per-use payment from viewers.

Standardizing on different content types is obviously a whole can of worms in itself. It does seem to be an improvement, however, on the current situation, where we have basically three main "open" content types for publishing:
1. RSS (for blogs)
2. Apple's bastardized RSS (for podcasts)
3. WWW, which is possibly the most complicated spec of all time.

I think WWW's ongoing role will be for discovering new content types, for interactive media, and for application distribution (maybe). But for well-established content types I think it adds way too much complication and bloat. If you think about it, most of what proprietary systems add to well-established content types is a way to consume them _without_ the pain and suffering of WWW. Medium, Twitter, Google Photos, YouTube, etc. Of course, in all of these cases, can serve as a completely fine fallback when you don't have the appropriate app.

### How do we get there from here?

If I knew exactly what the next step was, I'd be foolish to not be working on it. And yet look at me: blogging! I think, perhaps, creating easy-to-use self publishing systems (that put content on a creator's own Digital Ocean server, while we wait for the black box home server to arrive) is the right thing to do.

But do the content types need to exist first? Should I create a content type for ".blog" (probably Markdown with some TOML on top) and see if anybody likes using it? I tried to make a podcast generator entirely based on MP3 metadata but that was pretty difficult and probably not the right approach.

Should hosting be stateful, like a WordPress blog with a MySQL backend, or stateless, like a Hugo blog built with a static site generator? For plain text blogs, the static site generator works great, but if video files and images are involved we might want some sort of object storage?

Do the apps that consume this content need to truly know about the different content types? Could we do all of this by bastardizing RSS, like podcasts did?

Should I be looking into Activity Streams? Or is that just WWW being needlessly complicated again?

What we need:
1. Tools to package content for distribution.
2. Services to self-publish that content with minimal effort.
3. Apps to subscribe to channels and enjoy the content.

And, hopefully, all three steps will involve standard protocols and formats.

Then, once all of this works, we can build toward feature parity with existing services by closing the loop: the app you use to enjoy video channels can also publish comments to your home server, which are then somehow linked to by the video publisher's server. It gets dicey and unsolved-problem-ey!

All of this without monetizing via scam or raising money in such a way that incentivizes centralization. Most Web 3.0 efforts, sadly, fail this test. Maybe I should be taking [Sir Tim Berners-Lee's Solid](https://solid.inrupt.com/how-it-works) more seriously, but it feels needlessly alien to me.

So, please hit me up on Twitter and let me know what you think, let me know if you want to help, and let me know if you have any hot tips.

I think a better internet is possible. It should be more like WordPress, I think. As long as it isn't literally WordPress. Because it should be more app-ish. Also, I'm not going to bother to learn PHP after all these years.