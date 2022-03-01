+++
title = "Automated Project Reviews"
date = 2021-05-25T15:04:36-04:00
tags = ["Tools", "Workflow"]
categories = [""]
draft = false

+++

# Automated Project Reviews

Getting things right without feedback is **really** hard, but not all feedback comes from other people! One quick way to generate meaningful feedback is by [looking back at past work](https://adamjermyn.com/workflow/feedback/).

A challenge with looking back is doing it at the right time. For some kinds of feedback this is easy: schedule weekly/monthly/quarterly reviews, with prompts tuned to the relevant time-scale. But some areas of life don't run on a regular schedule. For instance, I've noticed lately that I can avoid many dead-ends and wrong-turns if I do a literature review early on in a new project. But how early on should this happen?

"Right at the beginning" is a tempting but dangerous answer. After all, the earlier the review happens the more it can influence the project and the fewer wrong turns I'll take. The problem is that my projects tend to begin in a very exploratory phase, and many don't live past that. Even a brief literature review is an investment of at least an hour, often several, so it doesn't make sense to do one until a project has survived for more than a ~10 hours of real work.

So the question then becomes: how do I make sure this happens at or around the 10 hour mark?

What I settled on is time tracking plus some automation:

1. I use [Timing](https://timingapp.com/?lang=en) to track how I spend my work time.
2. At the end of each week I have a recurring todo to export my data from Timing.
3. I then run a Python script that analyzes how I spent my time.
4. If that script sees a project that crossed the 10 hour mark in the last week, it prompts me to do a literature review.

It's a bit clunky, but it works. New projects appear in Timing as part of my existing time tracking routine. The export and Python script take just a minute, so it's low-overhead. And it's rare that a new project takes more than 20 hours in its first week, so there's a very good chance that doing this weekly catches projects in their first 10-20 hours.

This workflow also supports other timing-based prompts. So for instance the same script prompts me to write a brief review of the status of each project when it passes increments of 50 hours, as a way of making sure that I still think each project is a good idea on a longer-term basis.

More broadly, I think this approach of combining time tracking with automated analysis and prompts has the potential to avoid a lot of wasted time and rabbit holes by serving as an automated reminder of goals ("What is this project meant to achieve?") and values ("How do I ensure that I do that well?").
