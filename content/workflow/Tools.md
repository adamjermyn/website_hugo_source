+++

date = ""
title = "Tools"
hidden = false

weight = 0

+++

## Tools

Tools should make work easier, more effective, and more fun.

This is an incomplete list of the tools I use, along with commentary on why I use them.

### Computers/OS

To help with work/life balance I use two computers, one for work and one for everything else. Both are Macbook Pro's running macOS, one is 15" (work) and the other is 16" (other).

Because [Tools Should Express Values](https://adamjermyn.com/posts/tools_values/) I use [GeekTool](https://www.tynsoe.org/geektool/) to display a list of values over my desktop background (but below all windows). I do this on both machines, with values tailored to either work or life.

I often run calculations on remote machines which I don't manage. Those almost always run some variant of [Debian](https://www.debian.org) Linux.

### Phone/Tablet

I use an iPhone as my primary handheld device, along with an Apple Watch and iPad Pro (12.9"). Because I look at my phone often, and because [Tools Should Express Values](https://adamjermyn.com/posts/tools_values/) I use the [Widgetsmith](https://apps.apple.com/us/app/widgetsmith/id1523682319) app to produce widgets that just feature text reminding me of values I under-use, and these live on my home screen.

### Scheduling and Task Management

I use [Fantastical](https://flexibits.com/fantastical) for calendar management on iOS and iCal on macOS. I find Fantastical provides a more information-rich display on a small screen, whereas iCal is cleaner to look at on the big screen.

I use [Things](https://culturedcode.com/things/) on both macOS and iOS for tracking todos. I like the look and feel of Things, and it is powerful enough for most of what I want to do, including recurring tasks. I also make daily task lists in markdown files to ensure I make a conscious decision of what I want to accomplish each day.

I use [Due](https://www.dueapp.com) for tasks that I have to do by a particular time. It's great at reminding me over and over when that time comes, in a way that's much harder to ignore than either a calendar event or a Things todo.

### Automation/Search

I automate tasks on my Mac using [Alfred](https://www.alfredapp.com). I also use Alfred to search documents and folders.

Alfred supports [Workflows](https://www.alfredapp.com/workflows/), which are a powerful way to build automated tasks. For instance I have a workflow (activated with the command `nlog`) that creates a time-stampted markdown file in a "Research Log" folder, populates it with a template, and opens it. I have similar workflows for my [Weekly Reviews](https://adamjermyn.com/workflow/feedback/) which further open the previous week's prospective and review.

### Notes

I write [notes](https://adamjermyn.com/workflow/notes/) in [Markdown](https://en.wikipedia.org/wiki/Markdown) with MathTeX using [Typora](https://typora.io). Typora is by far my favorite Markdown editor. It provides inline previews as I type, supports beautiful formatting themes (I use [Mysty Light](https://theme.typora.io/theme/Misty/)), has a fast-feeling interface, and provides a minimal integrated file browser in the sidebar.

### Pen-and-Paper

In 2019 I switched from using pen-and-paper for calculations to using an iPad Pro with a 2nd generation Apple Pencil, and I haven't looked back. I tried the previous generation pencil and found it too cumbersome to use regularly, but the new ones (especially with 'double tap for eraser') feel strictly better than pen-and-paper.

### Analytic Calculations

I mostly do analytic calculations with pen-and-paper or equivalent. I use [Mathematica](https://www.wolfram.com/mathematica/) for more complicated expressions and more investigation-style work (plotting, inspecting expressions, etc.).  

### Email/Collaboration

I use [Gmail](gmail.com) to host my email and access it with the [Superhuman](https://superhuman.com) client. Superhuman has the best filtering tools I've seen, the most easy-to-remember keyboard shortcuts, works offline, and the interface is **fast**. Interface speed is underrated and they're among the best.

For more interactive collaboration I use [Slack](https://slack.com), [Zoom](https://zoom.us), and [Skype](https://www.skype.com/en/). I prefer Zoom over Skype because I find it easier to use, especially for sharing a tablet's screen.

### Software Development

I've had trouble using sophisticated IDE's. I usually find their interfaces clunky and/or slow.

I edit code with [Sublime Text](https://www.sublimetext.com). I use [Git](https://git-scm.com) for version control and [Github](https://github.com) for hosting repositories (including this website!). I find it difficult to work with Git in the command line, so I use the [Tower](https://www.git-tower.com/mac) graphical Git client.  

I use [Anaconda](https://www.anaconda.com) to manage my Python environment. I've found this more robust than manual management with pip.

### Presentations/Graphics

I make presentations and schematic figures in [Keynote](https://www.apple.com/keynote/) and [Powerpoint](https://www.microsoft.com/en-us/microsoft-365/powerpoint). 

### Utilities

I use [zsh](http://zsh.sourceforge.net) with [oh-my-zsh](https://ohmyz.sh) for my shell. The most useful feature for me is the ability to search for matching history commands with the up arrow.

I use [exa](https://the.exa.website) as a replacement for `ls`. By default it shows the information I want, and it shows it with pretty colors. I suspect I could configure `ls` to do the same, but this was easier.

I use [bat](https://github.com/sharkdp/bat) as a replacement for `cat` because it provides line numbering and syntax highlighting.

I use [dust](https://github.com/bootandy/dust) as a replacement for `du` because I find it faster and it defaults to more human-readable output.

### Simulations/Numerical Calculations

I manage remote simulations using my [RemoteExperiments](https://github.com/adamjermyn/remote_experiments) Python package because I frequently want to perform reproducible numerical experiments and managing them all by hand became difficult.

I simulate stellar evolution using [Modules for Experiments in Stellar Astrophysics (MESA)](https://docs.mesastar.org/en/latest/) because it is open source, it's the code I have the most experience with, and it's a code I help develop.

I perform Bayesian inference using [dynesty](https://dynesty.readthedocs.io/en/latest/) because I like its Python interface and the way it sets up inference problems in terms of likelihoods and priors meshes with how I think about them. I also like the fact that the underlying [Nested Sampling](https://en.wikipedia.org/wiki/Nested_sampling_algorithm) method provides estimates of both the likelihood and the uncertainty in the likelihood.

### Spaced Repetition

I use [Anki](https://apps.ankiweb.net) for [spaced repetition](https://adamjermyn.com/workflow/spacedrepetition/). It came highly reviewed by [Michael Nielsen](http://augmentingcognition.com/ltm.html). That said, I'm actively looking for alternatives because I've run into limitations with Anki. In particular, inspired by [Andy Matuschak](https://andymatuschak.org), I would like to be able to queue tasks with spaced repetition, and Anki is not well set-up for that. I also want to be able to mark cards as 'bad' (meaning 'refactor this card'), but haven't found an easy way to do this in Anki.

 I mostly **review** cards using Anki on iOS and **create** cards using Anki on macOS.

### Habits/Health

I track habits using [Way of Life](https://wayoflifeapp.com). I picked this because it doesn't try to impose its own goals on my habits, and it lets me easily see my progress on each habit through the week.

On Way of Life I only track whether or not I performed a habit each day. I separately track details of exercise-related habits using my Apple Watch as well as the [fitlist](http://www.fitlist.com) app on iOS, which I found provided an easy-albeit-clunky way to enter, review, and export data. 

Until the end of 2020 I tracked my eating habits with [MyFitnessPal](https://www.myfitnesspal.com). In 2021 I switched to [FoodNoms](https://foodnoms.com). I found FoodNoms provided quicker data entry, and provides more useful feedback and reports on my habits. A downside of FoodNoms is that its food database is much less extensive than that of MyFitnessPal, so I end up having to think of similar foods or decomposing foods into ingredients more often. I've been tracking my eating for years so I'm pretty good at that, but it would give me pause in recommending FoodNoms to someone just starting out on tracking food.

I meditate with a combination of [Headspace](https://www.headspace.com) and [Waking Up](https://wakingup.com). Headspace gives a more 'standard' experience whereas Waking Up provides a broader diversity of guided meditations. Because of that I would recommend starting with Headspace and using Waking Up as a supplement later on.

I've found I have trouble sleeping when there's too much on my mind, so before bed I write down whatever I'm thinking about in Apple Notes in the form of a todo list. I keep one running list for the week, and review that week's list on Sunday. The idea is that I then know each thought  will be considered again at a later date, so I don't need to keep thinking about it. I considered just using [Things](https://culturedcode.com/things/) for this but found that it's too clunky for entering a lot of todos at once, particularly as they're all for a future date.