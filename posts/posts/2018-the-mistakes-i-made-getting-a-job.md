---
title: the mistakes i made getting a job
author: bryan
date: 2018-10-04T01:01:00.000Z
---
![angery think emojo](/images/2018-09-27-11_47_48.jpg)

alright now that we're here, it's time to explain.

back in june, of this year actually (it's 2018), i got an internship. ok wait no, let's rewind.

**back in February**, i went on this crazy job hunt. i was updating my linkedin, signed up for a profile on [angel](https://angel.co/) and did all those job hunt things - you know: resume writing, applications, frantic searching, all that "good" stuff.

eventually after searching so much on sites like indeed, monster, ziprecruiter, cheesecake factory careers, i finally landed a "job". it wasn't that big of a job, really. it was an internship. i can't name this company, and i'd rather not honestly, so let's call them Parasol Technologies, Inc. (made up the name, it's fiction, don't sue me ugh)

anyway - an internship woohoo!!!1 it was really simple to get in. i saw their application link on either angel or LinkedIn, and i clicked it. it took me to their corpo site with the details and all that fancy jazz. it required a bachelor's degree in computer science, apparently, but i didn't care. i applied anyway. i wrote up some info and the cover letter, whatever. i applied.

got an email back if i agree with Parasol's company culture (take notes, i'll touch upon this again in a bit). it was probably the most generic, vague stuff i've ever read. i had to agree on all points and elaborate. it was something like this:

* Growth: build up with other people in a positive way
* Fluidity: no bureaucracy, supposedly. there aren't people constantly monitoring you to see if you're doing what you're supposed to do. this one emphasizes that the company is very startupey 
* Teamwork + Trust: working together as a team
* Speed: just be fast/ efficient/ whatever
* Excellence: making things as best as possible
* Dedication: basically sticking to doing stuff right for the long-term
* Initiative: this one was wordy, it basically said that something needed to be done daily, no matter how tiny or trivial

cool, next they wanted me to complete this single-page app thing. it was a calendar. the only problem was that this calendar wasn't touch-friendly (yikes). i was tasked with making it so that the calendar worked well on mobile devices. what happens is that you tap the calendar on your phone, and it makes a popup. that popup lets you select a range of a date and time. i patched it in about an hour, it really wasn't that hard. it mostly used jQuery (since that was part of it already) and overall I kept it simple and functional.

surprise; they liked it

it went on to an interview with the ceo guy. i'll call him Jack. i think i still have the call recording from that, probably. it's somewhere in my dropbox account. it went well, we arranged on having an _unpaid _internship for the summer. i was naive, and i said sure. we went ahead, and i mistakenly signed all these legal documents with unreadable technocratic legalese jargon in it.

## Big Mistake #1: Not reading the legalese jargon.

i'll come back to this one soon.

yup so that was february. in the months between that and june, i received many internship opportunities from linkedin in my inbox - from companies like [Cyxtera ](https://www.cyxtera.com/)to Big Corpo like [Accenture](https://www.accenture.com/). guess what i did? apply? nah, i was confident that the opportunity at a small startup like Parasol would be promising, and so i ignored the offers. _i was literally receiving these offers about internship opportunities for 2 months straight and did nothing about it._

## Big Mistake #2: Sticking to self pride and being closed-minded.

the internship starts. woo, let's get into it. i get my stuff ready on a friday, it's supposed to start monday, but whatever. i get my new email, gitlab account, and they used slack. cool, so i join all that stuff.

monday starts and i try setting up the web server stack on my personal computer. that does not work well. see, they used Go. and they used Docker. also, most of the team (it was under 10 people at best) had macbooks. I use windows. docker does not run well on windows. worse, the web server required that the API server (that connected to the database) be on the same machine. why? the API server was firewalled out of public access, so only the web server is publicly accessible. they did this due to "security" reasons but in reality it just makes things more bloated and unnecessarily complicated. the API server also connected to a cassandra database, but that had to be locally running as well because the staging + production DB was firewalled out of public access. that's a good thing, but the API server being locked out is **not a good thing**.

i spent days - in fact, most of my time there, actually - attempting to get this broken server stack to work. i tried a lot of things: running the stack on my computer natively, which failed; installing the thing on ubuntu, which didn't work either; and installing the stack on ubuntu server, which worked sometimes, but then ultimately stopped working for some reason. it was a whole mess. i didn't understand why it had to be like this.

there were daily standup calls, which i did not like. it was over skype, which is okay, but i guess that's just how Parasol does stuff. on top of that was the weekly "mandatory" team call on wednesdays. i quoted that last word because, in reality, both were pretty much mandatory. it wasn't a matter of "i can't make it", but "why didn't you make it". Jack the CEO man really pressured it (90% of MBA graduates really don't have great minds). i was pretty much under constant surveillance by the Jack, which is kind of ironic considering Parasol mentioned the whole anti-monitoring thing before in the culture statement.

## Big Mistake #3: Not researching beforehand.

there were people on linkedin who were listed as having worked for Parasol before. i could've very easily gotten in touch and asked how the company worked and the like. i didn't. neither did i look into the company background, or registration papers - none of that. i could've really gotten a taste of what to expect had i done that.

back to story time. i was tasked to work on fixing this feedback button. the CSS on the website was an incompetent mess, but i worked around it anyway. i fixed the feedback button - it was all just a minor issue with the CSS media queries. I did fix the problem, and did it in such a way that nothing else broke. after a few days, Jack commented on the GitLab issue. **the Jack CEO man did not like the changes. **supposedly i changed the button's behavior in some drastic, major way (all I did was change 760px to 360px in the width breakpoints).

earlier that week, i came home exhausted from school and passed out on my bed. that wasn't fun, it was a great nap though. i wake up and realize that i missed the standup call that tuesday (remember that the "mandatory" one is on wednesdays), and afterwards The Jack** **got really mad about this. on that GitLab issue, after I clarified that I didn't somehow magically ruin the button, he began to lie that I'm "lazy" for missing out on the team call \[that "isn't mandatory"] and for "barely" completing a single issue within a week at Parasol.

overall, a very rude guy.

remember that line a couple paragraphs back? i spent most of my time getting the server stack to work. and i did. did it work very well? nope. am i to blame for a poorly-done setup? not really. it was a bit nasty how Jack replied, moreso with emphasis on the poor temper and rudeness (hey remember the Teamwork and Growth parts of Parasol's culture?)

i did leave later that day, after Jack went bonkers and tried to shoot me down because he can't manage to get competent developers on his team. to be fair, though, i don't believe anyone was getting paid there. it was a fully remote company, and the only mentions of compensation ever was shares of equity between 0.3% to 3.5%. it really wasn't a great deal. i was doing a junior developer job for free, which is bad.

## Big Mistake #4: Accepting no compensation, undervaluing your own skillset.

i deleted my slack account from there, deleted the gitlab, and logged out from the email account. i received an email from their lawyer basically saying i was under some PIIA legal obligation or whatever, since I signed that document many months earlier. a non-disclosure agreement, basically. it was annoying, and i just told them to go away. i blocked the emails and i could finally sleep at night.

oh, did i mention? that whole drama show lasted about a week and a half. it was a hectic week, really stressful. i didn't dive too much into details, because most of it is micro-stuff that doesn't really matter much.

do I wish I had applied for those other offers? yes, definitely. but, now that i fell for job bait, i know how to avoid it in the future. thankfully i did learn now, too. someday, when the matter of getting a job turns from wanting experience to desperately needing income to survive, i'll know how to detect and steer away from the people who don't share my same values. 

do your research before accepting the job, seriously.

a team should work together and grow for the long-term - that's great! but, when the CEO comes in and brings the hammers down without a care in the world, that's just carelessness. it's a recipe for disaster. avoid the troubles, go the extra mile. there are lots of people out there who will value you more than Jack will, and actually pay you for the work.
