+++
title = "Robust Tools"
date = 2020-12-30T10:37:04-05:00
tags = ["Tools", "Workflow"]
categories = [""]
draft = false

+++

Good tools are robust. This doesn't just mean that they don't fail, it means that in many instances they *can't* fail. They take common failure modes off the table, freeing you to *use* them and focus on your goals.

## Impossible Failure Modes

For a robust tool many failure modes are, by design, simply impossible, to the point where it's hard to imagine what those failure modes are.

Consider a solid metal hammer. What are its possible failure modes? I could hit my hand by mistake. That's pretty much it.

How about a hammer with a wooden handle and a metal head? This introduces new failure modes: the attachment between the head and the handle could fail, or the wooden handle could break.

On the other hand, in no universe does a hammer let me accidentally paint a nail, or embed the nail in a piece of wood ten feet away, or remove all the oxygen from the room. The hammer is **robust** to these failure modes, to the point where they seem nonsensical. That's what it means for a tool to be robust.

## Not All Failures Are Made Equal

`ls` and `rm` are two common software tools. `ls` lists the contents of a directory and `rm` deletes files. Both of these have failure modes, typically in the form of "I typed the wrong command by mistake". Do this with `ls` and the worst that happens is some unexpected output or an error message. Do this with `rm` and you could **delete everything on your computer**.

In this sense `ls` is more robust than `rm`, even though both support the same "bad input" failure mode. `ls` might hit your hand, but it won't remove the oxygen from the room.

## Simpler is More Robust

Simple tools are more often robust than complicated ones. Hammers are more robust than cars. A car *usually* transports people from one where they are to where they want to be, but it has a long list of exotic failure modes including

- Not starting.
- Exploding.
- Moving *into* a solid object (crashing).
- Not moving to the right place (getting lost).

and so on. Fortunately by careful engineering most of these failure modes can be made very unlikely, and can mitigate the consequences when things do go wrong. That's what's driven most of the reduction in fatal car accidents in the last century.

## Robust Patterns

Robust tools often use similar design patterns. Some of the commons ones are:

### 1. Modularity

Modularity means that the tool is composed of pieces, each of which solves a simpler problem. Because simpler tools are more robust than complicated ones, modular design makes tools more robust. Modules are also often re-used between tools, making it more likely that failure modes will be caught.

### 2. Consistency

Consistency means that the tool presents a consistent view of its internal state at all times. This makes the tool more likely to reflect a meaningful abstraction. For instance, if there isn't enough gas in the tank for the car to start, the fuel gauge should point to empty. If there *is* enough gas, the gauge should *not* point to empty. This makes the car reflect a useful abstraction ("a device with gas in the tank that is either sufficient or not"). *Failure* to be consistent allows the user to think there is enough gas and then have the car fail to start, or decide not to try starting the car even when there is enough gas.

### 3. Fail-Safe and Fail-Loud

Some failure modes are unavoidable. Sometimes the user gives a bad input. Sometimes they forget a crucial step. In these cases it is better to fail *safely* and *loudly*. **Not All Failures Are Made Equal!** This transforms the failure into feedback for the user.

In software safe failure usually means halting, saving state, or preserving an "undo" option. With physical tools safe failure means preventing damage, like a car that automatically slows down when it approaches an obstacle **even when the driver tells it to keep going**.

Loud failure means telling the user what went wrong in a way they can't ignore. 

## Robust Tools Express Values

In order to make a tool robust you, the tool designer, need to decide what your tool is meant for. This is a value judgement.

A car that ignores the driver and slows before an obstacle expresses the value that **cars are not meant to crash**. Software that halts on an error expresses the value that **errors are bad** and probably unintended. A hammer that doesn't also remove oxygen expresses the value that **hammers are for nails**.

These may seem like obvious values, but many tools pick contrary values, often for good reason. By default bash scripts and php code keep going even if they hit errors. This, too, expresses a value judgement. **"Halting is worse than an error."** And this value makes such tools robust against certain failure modes like "halting on bad input".

This also means that **robustness is relative to use case and user**. An obstacle-avoiding car is only robust in the hands of a user who wants to get from A to B. It's horribly failure-prone for a police officer in a high-speed chase. Similarly, bash continuing through errors makes it robust for users who can't tolerate halting, but fragile for users who really care about correct execution.