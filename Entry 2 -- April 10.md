# Design notebook for week ending April 10, 2016

## Last week's critique

Didn't receive a critique for last week :/ but, the Monday meeting was quite helpful in helping me talk through some design issues/bigger questions that I had. I think the most pressing issues in my project (about the rhyme API, for example) were answered in that meeting and I found that to be very helpful.

## Description

Highlights:

**Architecture**: Sat down with Prof. Ben and finally got my architecture sorted out and in a good place. I figured out what my IR looks like and then spent some time in class (and out of class) reworking my file structure such that I could have my functionality that I had before (being able to check all lines rhyme with one another) but now in a much more extensible way.

**Scheme**: I started doing regex checking for ryhme scheme, and decided officially to use the regex method. Currently, a scheme will be described in regex form, and a poem will be broken down line-by-line into a string detailing which words rhyme with which -- i.e., the first line gets rhyme a, the second gets b unless it rhymes with a in which case it gets a, and so on. Then I'd match the string to the scheme regex, and if there is a match then the poem is valid.

With these two things in mind, I'm getting really close to my MVP on the project. I hope to have it for tomorrow but may not -- in the case that I don't, I'll be able to show it on paper. I do anticipate having something to show my critique group tomorrow for prototype, though. 

I'm now probably behind schedule if I'm going off of my plan at the beginning. I'm not super worried because I feel like my next steps are fairly straightforward and I know how I want to get them done, and my time should be better in the next couple of weeks to work on this, but at this point I do have a lot of work to do, especially considering that I have had a couple big rethinks of my project in the last couple weeks and my work still feels distinctly "square one"-y at the moment. So, it's kind of game on for these next two weeks.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I want to get my regex functions working! I don't think this will be hard -- in fact, I *might* have this done for tomorrow. If not, I think it won't take long. I'm using Python's re library and I've found it quite simple to use.

**What questions do you have for your critique partners? How can they best help
you?**

I'm not really sure... I think I'll have a better idea after prototypes. Because my prototype won't actually demonstrate how a user interacts with the language, I guess my question for now is syntax. Is the prompting idea (having the terminal prompt the user for commands like "check poem" and "insert rhyme scheme") the best way? Are there keywords or phrases that make the most sense? If my current way is not the best way about it, what would be a better solution?

I am looking forward to work session on Wednesday because I want to get a lot of good work done.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

To this point, I've spent probably about 7 hours on the project. I sprained my ankle Saturday and spent time in the hospital both Saturday and Sunday, so I lost almost all of the little time I had this week for work (I was also in the musical down at Pomona). About an hour was spent after Monday's meeting exploring different APIs, and another hour was spent Tuesday on doing rhyming optimizations that I eventually discarded (because I decided with Ben not to worry about the API too much), and another hour was spent on the critique of Josh. That said, I'm submitting this critique early because I don't know exactly when I'll get to do work tonight (and I plan to add hours tonight) and this is due at midnight. So, hours will probably be in the 8-9 range.


