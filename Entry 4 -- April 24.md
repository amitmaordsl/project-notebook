# Design notebook for week ending April 24, 2016

## Last week's critique

I did not receive a critique last week :(. However, critique group time in class was extremely useful. I wasn't sure if I wanted to add more functionality or focus on making the current functionality as strong as possible, and the group were strongly in favor of the latter. It was interesting because it was something of a toss-up for me but they were really adamant that this is the way to go, so I went with it. I think it was the right move.

## Description

There were three main things that I added this week. The biggest was error messages. I don't love that the error messages are currently not in their own class, but I think that's something that can be adjusted later very easily. The error messages should now encompass all possible problems that can happen with a rhyme scheme, including wrong number of lines, incorrect form for a schema, and other issues like words not rhyming that should rhyme. Because of the target audience, it's really important that the error messages are descriptive as possible, and I really tried to do that.

The second thing implemented was checking the number of lines in a poem based on the given rhyme scheme. This is important because it happens befor any API calls are made, and the APIs are by far the most time consuming part of the language. As such, if a user inputs a poem that cannot possibly parsed by a rhyme scheme (considering the available patterns and so on) then the interpreter will stop executing even before starting the API calls. This has led to a dramatic performance increase, especially on poems of length 10 or more lines.

The last important thing I implemented was the form dictionary, where users can input rhyme schemes and save them, and then check poems against the saved rhyme scheme. They can also input a name (like "sonnet") and call it based off of that. Currently, the user has to specify if they are checking a poem using a rhyme scheme that is saved or one that they are inputting, and I think I want to keep it that way to avoid confusion. I'm open to suggestions on this though.

I also added a LOT of error checking, which went hand in hand with the improved error messages.

With the remaining time I can go one of two ways. One thing I can do is fix up the architecture as much as possible, which would be really helpful for future extensibility. I don't actually think this is something that I'll want to spend time doing, but the thought of programming and designing with good practice in mind is appealing to me and important to think about, especially as I start working in programming this summer. The other thing I could do is add functionality. I think syllable counting could be helpful, though I'm hesitant to add it because I think it would be really clunky syntactically to use as a user. If I can think of a good way to add this, then I totally will; if not, I think I'll stick to adding small amounts of functionality and perfecting the architecture and file composition.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Not sure. How is the syntax? Is it usable enough? The obvious best way to present this to a real user would be through a graphical interface, but is the syntax okay for the purposes of this project?

**What questions do you have for your critique partners? How can they best help
you?**

Well, am I done? Is it worth trying to add syllable functionality? How should that be added syntactically? Some poems, for example limericks, don't have the same number of syllables per line, and I could see this actually being somewhat burdensome to specify as a user...

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**
I probably spent 10-12 hours on the project this week. I tried to add as much error checking as possible, and the number of lines functionality was actually quite difficult to implement in the end logically. I also made sure adding a rhyme scheme worked well and also error checked.

