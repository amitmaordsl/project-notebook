# Design notebook for week ending April 17, 2016

## Last week's critique

Josh's critique was very helpful once again and helped steer me in the right direction for this week. I was really thinking about using a terminal interface to interact with a user, and Josh steered me away from that and towards things like more helpful error messages and rhyme suggestions. Also our time talking together in class and with Prof. Ben gave me a better sense of which way to go and what kinds of things to focus my time on, especially as far as rhyme suggestion goes. Thanks Josh!

## Description

Where to start? I think the biggest thing that changed this week was that I completely re-did my rhyme scheme architecture. Instead of a pure regular expression being evaluated with the Python re library, I created my own simpler version of regex's that only supports for "*" functionality. However, the "*" itself is not actually typed in. What I changed it to was that "(ab)c" and "(ab)*c" are equivalent, though my scheme parser only accepts the former. I think this change is actually quite helpful because it makes the scheme feel less "programming"-y which is the intention with all the language decisions.

After doing that, I got my code to a point that it can parse a poem, a rhyme scheme, and tell you if the poem matches the scheme or if the poem does not, and if it doesn't, it can actually provide for you the incorrect line, telling you what word was wrong, what the word should have rhymed with, and a list of suggested additional ryhmes. Hooray! This is my MVP! At this time, the program provides up to 1000 suggested words, which is totally unreasonable, but the fix for this is pretty straightforward and I'm not worried about it at all. The error message is still quite helpful and in a format that I personally like.

This is part of the new push to add helpful error messages and little bits of functionality, though additional helpful error messages need to be added. I think one of the most helpful things Josh mentioned is that now it's all about adding extra stuff, like checking if the number of lines is possible in the rhyme scheme and things like that. There are a few different things that can be added here, so I think it's going to be about checking in with the critique group and deciding what's most important in this last week of programming.

There are a couple things I want to do to put the code in a better place. One is to clean up architecture. It's been easiest so far to centralize a vast majority of my code into one file, interpreter.py, and allow that file to grow more and more. It's *probably* fine if I leave it that way in order to add my last bits of functionality to the project, but I do want to leave it in as good a state as possible so that I could hypothetically improve on it in the future. Plus it's just good code practice. I also want to add much more testing, but am thinking maybe I should do that once I'm satisfied with the functionality I have. I'm sad I didn't do TDD like I said I would, but I'm perfectly on track with the project according to my plan, and I'm very happy with that.

It's all about adding bits of functionality now. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I"m not really sure. I think the language is pretty stable. There hasn't been much thought devoted to language -- perhaps that's next. I also want to restore my architecture as I mentioned above.

**What questions do you have for your critique partners? How can they best help
you?**

What are the most important additions to the functionality? Is it important for the user to be able to add a schema and have it stored in the program? Or is it more important to do more poem checking, like checking line count or syllables? I think the former makes the current functionality feel more complete, whereas the latter adds further *features* to the program. What do you think?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I don't really know exactly how many hours I spent, but it's probably something like 7-9 hours. Re-designing the scheme took a while, and after that it was all about getting the error message the way I wanted it to look, and designing and implementing the scheme algorithm after that. There isn't a ton of code being written, but the code being written is quite deliberate and non-trivial in terms of complexity.


