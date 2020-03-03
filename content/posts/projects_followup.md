+++
title = "Three projects is one less than four"
slug = "three-projects-in-may-actually"
subtitle = "This post is a form of self-assessment"
date = "2019-06-26T12:45:59.324310806Z"
+++

Last month [I created a plan for myself](https://pauljmiller.com/posts/four-projects-in-may.html): instead of just tinkering with various projects, I would bring four projects to a point of portfolio-worthiness. One project a week.

The result? I did three of them! And, also, did other things as well. Here's what went right, and what went wrong.

### Code on tape

The moral of this story is: write your own components if you can. I've always approached programming as "the idiot in the room." That is, I assume everyone else's GitHub code is so much better than mine that I'd be a _fool_ to try and write my own implementation.

But, in this case, it turned out way more efficacious — and, more importantly, more educational — to write my own component for wrapping the [Monaco Editor](https://github.com/Microsoft/monaco-editor). And a hook to [record audio](https://codesandbox.io/s/81zkxw8qnl). I still got stuck a lot, and still copied a lot of code from GitHub. Also, that hook [ended up being fixed by React's own Dan Abramov](https://twitter.com/dan_abramov/status/1126264624326823942), which feels a bit like cheating, but...

The moral is still the same! Writing, or at least attempting to write, my own components instead of instantly reaching for whatever's hot on npm lead me to much better understanding of what I was doing, and therefore more steady progress instead of eternal stuckness.

Unfortunately, while I got Code on tape to a working state, I didn't get it to an easily shareable state. Maybe I'll do that someday! This knocks my number of "finished" projects down to three, but of course "finished" is a very subjective thing.

Oh, one more sidenote: I did state management in Overmind because it seemed to offer similar advantages to Redux but with much less boilerplate. I think that proved to be true!

(Github: [Code on tape](https://github.com/futurepaul/code-on-tape/tree/overmind))

### Calculator 2

This was easily my favorite project to build. Like with Code on tape, I had built a version of it before in React, but decided to rewrite it in Svelte 3 this time. And, because Svelte was such a breeze to work with, I ended up with more time to achieve two nice-to-haves:

1. Using Rust to do math. My earlier versions of Calculator 2 had used some random Javascript library to evaluate the math expressions. But now I'm using [RSC, a Rust crate](https://crates.io/crates/rsc), for which I created a simple WASM wrapper. It works, it feels fast and "solid," if that's worth anything. And, also: it works!

2. Because of Svelte and WASM, I was already dabbling in Webpack, which led me to make the boldest move of all: I wrote my own Webpack loader to turn mathematical notation into SVG. Earlier versions of Calculator 2 had used the excellent MathJax at runtime to accomplish the same thing. But, thanks to my Webpack loader I'm able to run MathJax at compile-time, saving gobs of Javascript at load-time and making everything just feel better.

(Github: [Calculator 2 on Github](https://github.com/futurepaul/calculator-2))

### Fragment Notes

Again I switched to Svelte 3 for the frontend, instead of the weird non-React view library I had been using. I also rearranged the project into three pieces: the pure Rust library (that does the full-text search, mostly a ripgrep wrapper), the native module library (that wraps the Rust library with [Neon Bindings](https://neon-bindings.com/) to make it work on Node), and the Electron app. This worked very well.

Except.

There's something I just don't really understand about how Node compiles native modules. When I try to compile a "release" version of my app to run as a binary, it ends up gigabytes big and insanely slow. But when I run `npm run start` from my project folder it works fine! And I find the build process so difficult, obtuse, and random, that I have zero motivation right now to track down a solution.

So Fragment Notes is now a working product that I use for my own notes-searching purposes. But I don't know how to package and share it, unfortunately.

(Github: [Fragment Notes](https://github.com/futurepaul/fragment))

### My Own Personal Blog

Instead of totally revamping the My Own Personal Blog project to be the static site generator for normies, I merely added the functionality necessary to [add the projects page](https://pauljmiller.com/projects.html). So, in a way, this is still undone. That said, I really love using my own static site generator, and am always glad I chose to roll my own instead of attempting sticking with Hugo.

(Github: [My Own Personal Blog](https://github.com/futurepaul/my-own-personal-blog/tree/genericify))

### svg-to-piet

Woah, what's this? This wasn't in the original plan!

That's right, during this month of working seriously on my own projects I also got extremely involved in the Piet / Druid community. My biggest work in this regard was a collab with [Connor Brewster](https://github.com/cbrewster) to build a [Piet backend with Raqote](https://github.com/futurepaul/piet/tree/master/piet-raqote). That is to say, Piet is a API for 2D graphics, Raqote does the grunt work of laying down pixels, and what we wrote was the adapter between them.

While piet-raqote is mostly an educational project, what I'm really excited about is [Druid](https://github.com/xi-editor/druid), which is a GUI framework built on Piet. With Druid I can make real, native apps using Rust — for instance, once Druid has the necessary functionality, I will be re-writing Fragment in Druid. Sorry, Electron, but you know this day would come eventually!

To help with some Druid development I was doing, I made svg-to-piet, which is a simple utility to convert an SVG into Piet draw calls.

If I had to pick a programming job out of a hat, I hope it would be a job that involved more or less straightforward data transformation of the kind that svg-to-piet turned out to be.

It wouldn't, however, involve writing Rust macros, which was the actual hard part of svg-to-piet.

(Github: [svg-to-piet](https://github.com/futurepaul/svg-to-piet))

### What's next?

I can't decide, tbh. This month was a great idea. I ended up with a portfolio I'm proud to share, and I learned a lot in each individual project. But I don't have another four projects of a similar character sitting on my back burner. I have a bunch of vague ideas that require education and exploration, which is a much more meandering process.

If you'd like to help me pick my next project, [perhaps consider hiring me](mailto:paul@pauljmiller.com)!

