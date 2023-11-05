---
layout: single
title: The YARG postmortem (YARGortem?)
toc: true
toc_label: "The whole ménagerie"
toc_icon: "brain"
tags: yarg gamedev postmortem

header:
  teaser: /blogimages/YARGPostmortem/teaserYARG.png
---

Hello! This is the big YARG postmortem! It's a very ramble-y blog post where I just dump all of my thoughts, past and future, into a big mass of text. Feel free to skim it and skip to the bits you think you'll find more interesting.

I started writing this in October of 2022, and now it's... Jesus, almost 2024? Let's just get it over with.

But first, some history.

---

# SOME HISTORY

> "When I was a child, I caught a fleeting glimpse / Out of the corner of my eye"
> - [_Comfortably Numb_](https://youtu.be/x-xTttimcNk), from The Wall by Pink Floyd

## The beginning

I first came up with the idea of YARG [back in 2019.](https://twitter.com/santumerino/status/1151867300519264257)
Ever since I started making games, I had an idea for a platformer where... something happens. I don’t want to tell because I still want to make it one day, and the idea is both extremely simple and not something I’ve ever seen.

Anyway, I didn’t want to jump straight into my first big game idea. That’s like, Game Development 101! Instead, I thought “hey, I’ll make a simple platformer! How hard could _that_ be?”

## The very sudden ending

...very hard, if you have no experience and the idea isn’t good.

The original idea was to make a short, 15-level game where a narrator character would constantly berate you for being so bad at the game. If it sounds familiar, that’s because it’s an extremely generic premise.

Of course, I knew that. Which is why I had a great idea in mind!

...the great idea was to call the game “Tuberbait”. Like, y'know, YouTuber bait?

![tuberbaitMockup.png]({{site.baseurl}}/blogimages/YARGPostmortem/tuberbaitMockup.png)
(what a logo might've looked like)

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

> "I got a feeling there's too much at stake / Down and out again, on a brand new day"
> - [_Room to Breathe_](https://youtu.be/JhUF4Beb9Y4), from Room to Breathe by Vine

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

I wrangled the level editor together with the help of [this tutorial](https://www.youtube.com/watch?v=7zqKzZA6Z2o) by Almightyzentaco —a sort of Brackeys for the Clickteam Fusion community. But I barely understood what I was doing, and the end result is something that worked for me as a dev tool, but which isn’t the best thing for players. Objects disappearing, files being overwritten... I still have nightmares about the screenshot system.

The level editor is the reason why the game came out in the first place (I spoke more about it [right here](https://santumerino.itch.io/yarg/devlog/310188/the-power-of-level-editors)) but it is held together with duct tape and dreams. More so then than now, thankfully, because the focus of the first major update was fixing the whole thing!

### The level editor... 2!

At some point even I got tired of staring at this bloody thing:
![LvlEditorOld.png]({{site.baseurl}}/blogimages/YARGPostmortem/LvlEditorOld.png)

So, after recuperating a bit from the postpartum depression every Creative™ feels after releasing their work to the wild, I got to work on re-building the whole thing:
![LvlEditorLatest.png]({{site.baseurl}}/blogimages/YARGPostmortem/LvlEditorLatest.png)

If you haven't used the old level editor and want to experience the pain, the first public build of the game is available on Steam (under "Betas") and Itch.io (as a separate .ZIP). But let me tell you right now, it sucks. On controller, all the dropdown menus would activate if you tried to place items over them. Also, sometimes you wouldn't be able to place items at all. _Also_ also, deleting things would sometimes not work. And so many other things I've lodged in the deep recesses of my mind, for remembering them would surely end me.

With the new version, I redesigned everything. No more dropdowns; now it's an entirely separate toggleable menu. No more problems with placing tiles; I rewrote everything. No more ugly Windows 98-looking menus; now it all looks like it belongs with the rest of the game's menus. Less _Microsoft Excel_, more _Mario Maker_, if you get what I mean.

As much as YARG means to me (a lot, as you'll read X paragraphs from now), I was sick to death of looking at it after I released it. And yet, I somehow gathered enough energy to work and fix something that was really bothering me!

This is still unexplainable to me...

## The name

I kept the name "Yet Another Rage Game" and I regret it every day of my pitiful existence.

At some point I realised that was stupid, so I began calling it YARG everywhere and left the long version as a sort of subtitle. But it was far too late to fully rebrand the whole thing.

...and then, in 2023, a _vastly_ more popular YARG [came out of nowhere](https://github.com/YARC-Official/YARG) and took my game's Twitch game page with it. To be clear, I am not upset at them in the slightest. I talked to one of the devs and they seem like good people. Wish them all the success in the world, from the bottom of my heart...

...but now my game is fully doomed to SEO hell (even more than it was already). This could've been avoided! It only happened because we both coincidentally chose to be Quirky and Self-Deprecating, and "rage" and "rhythm" happen to start with the same letter.

Should've stuck with "Tuberbait".

---

# LAUNCH DAY (AND WEEK AND MONTH AND YEAR)

> "When I have nothing to say, my lips are sealed / Say something once, why say it again?"
> - [_Psycho Killer_](https://youtu.be/tqQGWhge5yo), from Talking Heads: 77 by Talking Heads

## What everyone wants to know

How much money did I make?

Well, I don’t think I’m allowed to say how much money I made on Steam. But if I add what I sold on Itch.io and round it up a bit, I should hopefully stay out of trouble.

So, as of the last time I checked, the 4th of November 2023, YARG made...

:drum: :drum: :drum:

...about $75 before tax. Not even enough to break the $100 threshold for Steam to pay out (if this total were on Steam only). So I made, effectively, $0.

That... doesn’t sound great. But if you remember what I said X paragraphs ago, you’ll know it doesn’t matter! My measure of success was just getting the game out there. Thankfully this isn't my job.

But there are some reasons why YARG wasn’t _economically_ successful.

### Marketing

There was none.

I made a lot of Twitter posts talking about the development of the game. Mainly talking about milestones (showing images and video where possible!). But, of course, the people who search the #gamedev tag on Twitter are usually gamedevs themselves.

If the idea was to get people to buy the game (which, again, it wasn’t!), then it seems obvious that they should know about the game first. That’s the reason marketing’s so important.

Even then, I still somehow managed to get some wishlists!

### Wishlists

From what I’ve read, usually a developer can expect the number of wishlists for their game to go down on release, as people buy the game.

I went in with a modest 181 wishlists (to be clear I treasure each and every one of them, thank you). I released the game, woke up the next day, checked my PC and it had... gone up to 188? And now it’s at over 220??

It seems very weird, but I think it makes sense. If I had to guess, Steam’s algorithm pushed the game to a lot of people on launch day, and some amount of them found it interesting enough to wishlist, but not interesting enough to buy right then and there. I also saw some small peaks here and there whenever I ran a sale, but nothing massive.

Also as an aside I tried using one of [Steam's visibility rounds](https://partner.steamgames.com/doc/marketing/visibility/update_rounds) to coincide with YARG's first anniversary. Like 15 people clicked on it, and none wishlisted it or bought it.

### The fact that it's a 2D pixel art indie platformer in an oversaturated market of 2D pixel art indie platformers, some better and some worse

YARG is a 2D pixel art indie platformer in an oversaturated market of 2D pixel art indie platformers, some better and some worse.

Something that Steam users might not be aware of is that developers can see why they decided to refund a game. With YARG, only 4 people refunded it (which I don't mind either way, people are well within their right to ask for a return if they're not happy with it, but I _am_ happy that the number's in the lower single digits :)). But one of these people said something interesting:

> "This is just a poorly made clone of 'Not Another Needle Game' you clown. Can't believe you didn't credit it. Cashgrabbing game devs, grumble grumble..."
> - Anonymous gamer (paraphrased)

If you, like me, had never heard of [Not Another Needle Game](https://delicious-fruit.com/ratings/game_details.php?id=12534) up until this point, it's a 2013-ish I Wanna Be The Guy fangame that features a lot of spikes. I suppose it must have some sort of following within the IWBTG community, but as someone who hasn't even played the original, I promise you I'd never heard of it.

...and yet, I can understand why this upset gamer felt like both games shared a lot of the same DNA:

1. Both games are 2D pixel art indie platformers.
1. Both games feature spikes, sometimes quite prominently in some levels.
1. Both games have a Quirky title, except theirs isn't as Self-Deprecating.

You might think this describes a bunch of games out there, and you'd be correct. But the point is that, when it comes to this genre, it is _absolutely crucial_ to have something that makes it stand out. A gimmick, if you will.

YARG's gimmick is the amount of hidden lore. Throughout the story, you are meant to feel that something is off, and near the end, you get a glimpse of the truth —and there is a new game mechanic to indicate the shift. Then, on subsequent playthroughs, you can pick up previously inaccessible unlockables to progress the story further and, ultimately, unlock a different ending.

The problem with this is that it's... well, hidden. In terms of gameplay, it might as well be like any other 2D pixel art indie platformer featuring spikes and a Quirky title, up until near the end. What I failed to consider is that some —_most_— people wouldn't bother to see it all the way through and get to the bits where the game _does_ switch up.

This was by design. Unfortunately, the design here was flawed.

---

# OK DUDE, COOL STORY, LET'S WRAP IT UP NOW

Okay, jeez!

> "Romántica entonaba sus poemas más brillantes / Susurrando al oído de mi representante: / Te amo, te odio, dame más"\
> ["Romantically, she recited her best poems / While whispering into my manager's ear: / I love you, I hate you, give me more"]
> - [_Peperina_](https://youtu.be/8VDXZbxRlHQ), from Peperina by Serú Girán

## YARG 20XX: Raging Boogaloo

What's the future of YARG?

Well, I'll always be around to fix bugs, obviously. And I had a really big update in the works for it that would allow for custom content to be added in (kinda like a Minecraft resource pack: custom textures, music, voice lines, levels, variables for physics/movement/features/etc., all working as if it were an independent game). That one was almost done.

But, quite frankly, I am tired of working on YARG. I sent it out into the world as a sacrificial lamb, to prove my mettle as a game developer and see if I could manage a larger-scale project. And I succeeded! In my mind, it's served it's purpose.

However, I can see so much I want to add, and so much I want to fix. There is so much potential here that I could tap into!

...that's a fool's errand. No game is ever "done", it's only ever "good enough to release". I could invest my time and effort into so many other ideas I have, but now with the renewed confidence that comes from having finished something that, at the time, I considered to be insurmountable. And yet, I... surmounted it?

So that's what I'll do, I think.

## Small thoughts on YARG: Prologue

On YARG's anniversary, I re-released an old demo I made for it. It's available wherever the full game is for free.

It's got a bunch of stuff I won't spoil (just in case) that makes it a truly stand-alone experience. So, in a way, I got two games for the price (in years off my life...) of one! Wowie!

I think it would be cute to make an HTML5 build of it, as if it were an old Flash game of yore, and (re-)release it onto the open internet... but I'll have to see how I'm feeling about it.

## Conclusion

Thank you for everything, YARG. I sent you out to die, and you took it like a champ.

Because of your sacrifice, I can move on to so many greater things. You proved that this is a sensible path for me to take.

Thank you. I love you. Please forgive me.
