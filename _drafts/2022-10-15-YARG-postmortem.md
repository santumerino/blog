---
published: false
---
Hello! This is the big YARG postmortem! It's a very ramble-y blog post where I just dump all of my thoughts, past and future, into a big mass of text. Feel free to skim it and skip to the bits you think you'll find more interesting.

But first, some history.

---

# SOME HISTORY
> "I got a feeling there's too much at stake / Down and out again, on a brand new day"

> - [_Room to Breathe_](https://youtu.be/JhUF4Beb9Y4), from Room to Breathe
## The beginning

I first came up with the idea of YARG [back in 2019.](https://twitter.com/santumerino/status/1151867300519264257) 
Ever since I started making games, I had an idea for a platformer where... something happens. I don’t want to tell because I still want to make it one day, and the idea is both deceptively simple and not something I’ve ever seen.

Anyway, I didn’t want to jump straight into my first big game idea. That’s like, Game Development 101! Instead, I thought “hey, I’ll make a simple platformer! How hard could _that_ be?”

## The very sudden ending

...very hard, if you have no experience and the idea isn’t good.

The original idea was to make a short, 15-level game where a narrator character would constantly berate you for being so bad at the game. If it sounds familiar, that’s because it’s an extremely generic premise.

Of course, I knew that. Which is why I had a great idea in mind!

...the great idea was to call the game “Tuberbait”.

![tuberbaitMockup.png]({{site.baseurl}}/images/YARGPostmortem/tuberbaitMockup.png)
(just a mockup, the game never got to the "make a logo for it" phase of development)

It shouldn’t be surprising that I dropped the whole game not too long after. Especially when 2020 happened and sent me into a Big Sad Moment(tm).

## What now?

I abandoned the game, which by that point was already called “Yet Another Rage Game” (as an attempt to be Quirky and Self-Deprecating Lol Xd), which left me with nothing to do.

So I decided I’d give it another shot. With the idea of “make a platformer” in mind, I started working on a game called Cube Run! And to try and keep myself motivated to see it through to the end, [I even made occasional devlogs!](https://www.youtube.com/playlist?list=PLvotjS6-aeGHOXWCjuisWEt7Y_P6ablt7) _(WARNING: 17 year old kid with a strong accent and a bad microphone!)_

Cube Run was a story-driven platformer where you had to pick up all the coins in a level in a specific amount of time to progress. It was actually a revival of an older game project with the same name, but everything about it was brand-new.

Problem is, my implementation of the idea was just... not fun! In retrospect I can see the problems with it so clearly. It’s a game where you have to race against the clock, but you move super slowly. You have a story, but it’s told to you through walls of text. And so many more things that, if I listed them all here, this blog post would never end.

So to make a long story short, in October of that same year I dropped the project.

## The beginning (again)

After Cube Run, I started on another project (an expanded version of a game jam game, which I may revisit someday), but I wasn’t really making any progress with it, so it was also put on the shelf.

Honestly, I can’t tell you exactly why I picked YARG back up again. I think I was severely doubting my ability to finish a long-term project, and whether this whole thing was even for me in the first place. I opened the YARG project file for some reason, played it, and... it was actually fun?

I couldn’t believe it. With Cube Run, I started with a good (I think) idea and expected it to magically become a good game. With the jam game revival, I never got far enough to actually explore any interesting new concepts. But this? The story was bad, but the gameplay was fun somehow!

That was very promising, but I had to make sure I would actually see this project through to the end. So, at the beginning, I implemented a few rules for myself:

1. ~~I wouldn’t add any more gameplay elements than what was already there (spikes and lasers).~~ _I ended up adding drones and sawblades and the whole ending thing. Whoops._
1. I’d rewrite the story from scratch, ~~but it would only be alluded to through voice lines.~~ _I ended up adding the diskettes, as well as animated* cutscenes. Double whoops._
1. I’d set a deadline for myself. Sometime in mid-late 2022, actual release date TBD. _This one I actually kept!_

Now that I had these totally unbreakable rules in place, it was time to actually make the dang game! How hard could _that_ be?

---

# ACTUALLY MAKING THE DANG GAME
> "Just do what you want to / But more"

> - [_Birthday 31_](https://youtu.be/U32QYfNuRDQ), by Yotam Perel
## The story

First things first, the original story had to go. I thought it would be fun to, instead of playing the whole "evil AI" trope straight, to play around with it.

I decided to make the AI character be very nice to the player, but also make it seem like it was hiding something. That way, the player doesn’t really fully trust the AI (this is augmented by the contrast between the difficult levels and the character being all hopeful about it).

This, of course, lead to an important question: what is the AI hiding? For the longest time, I didn’t have an answer. I fully intended on having the AI imply that something was going on, but never elaborate what it was.
But then I had some sort of epiphany.

**_SPOILER WARNING: THIS WILL RUIN THE BIG REVEAL OF THE GAME!!_**

When you die in the game, you immediately respawn, right? Seems obvious, because it is a videogame, but what if that wasn’t just a given?

So, that’d be the big secret. You’re a test subject for a science experiment involving immortality. One of an untold amount of people who came before you and who... weren’t so lucky to have the test succeed.

You may be able to spot the issue with this right away. Surely the character would realise they’re dying, right? And you’d be right, every time you die, the character retains all their memories and feelings (so don’t die in the game ever!)

My solution to this was... one that worked for the game. I’m not really a writer, and I never wrote anything of this magnitude before, so some suspension of disbelief is required.

What I did was to try and distract the player from all that. I created another “secret”, but one which was so obvious that the player would instantly figure it out. And if they didn’t, the AI would tell them anyway.

It’s so obvious, in fact, that I won’t mention it here. Just know that when the AI “confesses its lie”, that’s not the end of the story.

...this section was a bit of a mess. Why don’t I move on to something I can talk more freely about?

## The level editor

Oh my god the level editor.

I wrangled the level editor together with the help of [this tutorial](https://www.youtube.com/watch?v=7zqKzZA6Z2o) by Almightyzentaco. But I barely understood what I was doing, and the end result is something that worked for me as a dev tool, but which isn’t the best thing for players. Objects disappearing, files being overwritten... I still have nightmares about the screenshot system.

The level editor is the reason why the game came out in the first place (I spoke more about it [right here](https://santumerino.itch.io/yarg/devlog/310188/the-power-of-level-editors)) but it is held together with duct tape and dreams. It’s definitely gonna be the focus of the next major update, but I’m getting ahead of myself.

## The name

I kept the name "Yet Another Rage Game" and I regret it every day.

---

# LAUNCH DAY (AND WEEK AND MONTH)

## What everyone wants to know

How much money did I make?

Well, I don’t think I’m allowed to say how much money I made on Steam. But if I add what I sold on Itch.io and round it up a bit, I should hopefully stay out of trouble.

So, as of today, the 15th of October 2022, YARG made...

:drum: :drum: :drum:

...about $50 before tax.

That... doesn’t sound great. But if you remember what I said X paragraphs ago, you’ll know it doesn’t matter! My measure of success was just getting the game out there. The money’s just nice to have.

But there are some reasons why YARG wasn’t _economically_ successful.

## Marketing

There was none.

I made a lot of Twitter posts talking about the development of the game. Mainly talking about milestones (showing images and video where possible!). But, of course, the people who search the #gamedev tag on Twitter are usually gamedevs themselves.

If the idea was to get people to buy the game (which, again, it wasn’t!), then it seems obvious that they should know about the game first. That’s the reason marketing’s so important.

Even then, I still somehow managed to get some wishlists!

## Wishlists

From what I’ve read, usually a developer can expect the number of wishlists for their game to go down on release, as people buy the game.

I went in with a modest 181 wishlists (to be clear I treasure each and every one of them, thank you). I released the game, woke up the next day, checked my PC and it had... gone up to 188? And now it’s at over 220??

It seems very weird, but I think it makes sense. If I had to guess, Steam’s algorithm pushed the game to a lot of people on launch day, and some amount of them found it interesting enough to wishlist, but not interesting enough to buy right then and there. I guess we’ll see what happens when a sale pops up!
