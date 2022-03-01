+++
title = "Examples of Tools with Values"
date = 2021-01-23T17:51:55-05:00
tags = ["Tools", "Workflow"]
categories = [""]
draft = false

+++

I previously argued that [tools should express values](http://adamjermyn.com/posts/tools_values/). Here are some examples of tools I've made with an eye to values.



## A Brainstorming Environment

I have a shell script that sets up a work environment for brainstorming. It does this by copying and opening a template text document that says the following:

```
# Session:
- Maintain an attitude of suspended judgement.
- You're here to climb out of the basin.
- Cmd+E Will bring up an (incomplete) list of possible approaches.
- Have fun!
```

I'm still tweaking these values, but so far I'm fairly happy with them. They remind me that the whole reason I'm sitting down to brainstorm is to come up with new ideas further afield than I normally would. Only after I'm done generating ideas do I try to sift through and see which ones seem useful/promising.

Before I created this environment I found that I would usually write down ideas that were straightforward (and low-risk) extensions of things I'd done before. With this environment I've had more success at coming up with ideas that are genuinely different.



## Reminders on the Desktop

I use [GeekTool](https://www.tynsoe.org/geektool/) to display the contents of a text file on top of my desktop background. That text file is called `values.md`, and includes values like "Be Reproducible" (meaning, be sure that my science is reproducible) and "Do, Do, then Automate" (a reminder that many tasks benefit from automation, but not one-off's). These just sit on my background and I notice them from time to time. I don't have proof that they're helpful, but my subjective sense is that they are.



## Weekly Plans & Reviews

At the start of each week I [write a weekly plan](http://adamjermyn.com/workflow/feedback/) based on a template that gets me to ask:

1. What deadlines do I have this week?
2. What tasks do I want to complete this week?
3. What might get in the way of my doing this?

This is meant to give me something to compare against when I write a review the following week. These questions force me to write down what I want to achieve each week, and because I know there's a review coming later I have an incentive to make those plans accurate. The value here is "I want to do what I plan to do.", followed by a secondary value of "If I don't manage it, I want to know why."

In addition to getting at these questions, my reviews ask about my **habits** and how frequently I completed them. These are things like exercise that I want to do each day or each week, regardless of what else is happening. The value is "Consistency, every day, every week.", and I find that comes through from this process.

With plans and reviews the values are less explicit than my other examples, but they're still clearly encoded in the questions and templates.



## Remote Experiments

I frequently run numerical simulations on a compute cluster. To manage these I've made a tool called [RemoteExperiments](https://github.com/adamjermyn/remote_experiments) that uses a combination of `git`, `ssh`, and `rsync` to let me configure experiments on my laptop and then set them running (possibly in large numbers) on the cluster. Each experiment corresponds one-to-one to a commit that lives in a `git` repository, so if I ever want to reference the code and settings used in a past experiment I can.

I want to write about `RemoteExperiments` in more detail, but the connection to values is that if I use it to run my experiments I get reproducibility entirely for free. I don't need to do anything special. In this sense the tool is [robust](http://adamjermyn.com/posts/robust_tools/) against non-reproducible experiments. The value doesn't need to be expressed explicitly because the tool doesn't let you do otherwise.



## Where's the Value?

Two of these examples state their values explicitly. That's because they're primarily aimed to shape what I think about when I use them, and written words are an easy channel to do that.

With plans and reviews the values are less explicit, but they're still clearly encoded in the questions and templates and I'm very much aware of them as I work. They come across directly in the way the questions get me to think.

Finally, with `RemoteExperiments` the value is fully implicit. I don't need to think about reproducibility at any stage of using it because it handles that part for me. This is maybe the most common way that values are embedded in tools, and there's a good reason for that: embedded values don't cost the user anything. Whereas explicit values require the user to read and consider them actively each time, embedded values are just a part of how the tool works, freeing the user up to just **use** the tool.

