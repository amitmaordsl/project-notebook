# Design notebook for week ending April 3, 2016

## Last week's critique

Josh's critique was *very* helpful to my project -- thanks Josh! I think the biggest thing I took from the critique was to continue to keep my target audience in mind. Because my target audience is middle school-age kids with probably little to no design experience, it's really important that I make sure the syntax is as simple as possible; thinking about that from the critique led me to change the way I want to have the user interact with the language. Instead of having them type in commands or use the language in an internal-DSL-y way, I want the user to interact with a terminal which prompts the user in a certain way. The terminal will ask the user to enter a text file, or create a rhyme scheme, or similar prompts.

There weren't too many pressing issues in the project, considering that it was the first week of the project. That said, it was nice to know the parts of the project that Josh liked and that he agreed on the parts that would be challenging. He also brought up something I had not considered -- that in a rhyme scheme, it's entirely possible that the first word is the faulty word, and not necessarily that the following words are at fault. It made me realize that the rhyme checking algorithm I would use would need to be a bit more nuanced than I had thought originally. 

Overall, the critique was very helpful and well timed. I think that, in combination with our critique meeting, definitely put me on the right track. The critique meeting was also helpful because I was told by the group that rhyme schemes feel a lot like regex's, so I may want to use a regex checker in my project.

## Description

I think the biggest thing that happened was that I switched officially from Scala to Python on Thursday. (My code is still in a temp folder, but that's because I have some architecture decisions still unresolved). The other big change is that I now want the user to interact with the language through a prompting type system, i.e. have the DSL ask "enter a poem:" and "enter a rhyme scheme:" and things like that.

As of now, I can take a poem, split it into lines and words, and check words against each other to see that they all rihyme. This is a pretty exciting milestone, with a *major* caveat; I'm limited by the APIs that I'm using, and they sometimes omit really basic words from their responses for some reason I'm still not totally sure of. For example, for the word "beer," rhymes returned by the API include things like "pap smear" and "fallow deer" but not the word "here." Because doing my own rhyme checking would be really time-ineffective and probably prone to errors, I feel I am reliant on APIs to help me out. I'm toying with the idea of combining results from multiple rhyme APIs to get better coverage, but this still doesn't guarantee completeness and that really concerns me.

I am currently still fudging a bit with my architecture and I don't really like where it's at currenly. I am planning to solidify my architecture on a whiteboard tomorrow and possibly show it to my critique partners, so I'm not super worried, but for now I have an amalgam of files in a temp folder which do what I want but without a solid ordering or idea that the current setup is at all what I want.

All that said, I'm overall quite pleassed with the progress I've made. The list of to-do's is really quite large, which is great because there are lots of unsolved problems, a list which keeps growing because the project excites me and I like working on it. As of now, beyong the API issue, I have a couple other open ended ideas that I'm considering. The first is that rhymes are not always a single word ending a sentence, and slant rhymes are not necessarily returned. It is a similar problem as I am depending on the API for results, but some amount of these problems (I hope) I can actually solve and provide some level of functionality for. Additionally, I'm not yet at the rhyme scheme stage of my process, but I need to be able to add support for the first word in a rhyme scheme being the problem, rather than having the first word "define" the rhyme.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I feel like the current most pressing issue is that of the incomplete rhyme results from an API. It may not actually be most "pressing" per se, as the architecture is also a deifinite unresolved thing, but it feels most pressing because I've thought about it a lot and don't really know what to do about it.

**What questions do you have for your critique partners? How can they best help
you?**

Do you have ideas about the API problem described above? It seems like a big blocker. Also what are your thoughts about the multi-word rhyme issue?

Also, what do you think about language commands? Do you agree with how I think the syntax should work? Do you think it makes it easier for the target audience (who likely has no CS experience) to use?

I'm wondering if my ideas for architcture are good. I'm not totally fixed on my architecture, so thoughts on this would be really helpful.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

Probably about eight hours. I spent a lot of time not getting Scala to work, which was frustrating. I also am in a musical at Pomona and show week is this upcoming week, so I've been unspeakably busy with that. Still, I'm pretty proud I got close to the required hours, especially since I plan to "backload" my work hours on this project for the three weeks post-show.