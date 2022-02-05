---
layout: page
title: "A TEI XML Editor’s ‘Hello, World’ Exercise"
date: '2020-06-10 06:53:00 -0000'
permalink: /foundational-skills-and-knowledge/a-tei-xml-editors-hello-world-exercise
published: true
category: 'Foundational skills and knowledge'
tags: 'Hello World'
---
Anyone who has ever studied a programming language has likely seen a ‘Hello, World’ programme. They’ve been around for over 40 years and are usually the first programme you type in. The exercise is straightforward. You’re given the code to output the words ‘Hello, World’. You enter the code, do what’s necessary to run it and are rewarded with the output ‘Hello, World.’

I never thought much about ‘Hello, World’ exercises. I certainly never believed that I’d say the [TEI community](https://www.tei-c.org/) needs one. After reading a [recent article by Charles Martin](https://stackoverflow.blog/2020/03/05/a-modern-hello-world-program-needs-more-than-just-code/), however, I felt compelled to create one.

## Aims and objectives

Before we can establish the aims and objectives of a ‘Hello, World’ for TEI Editors, it’s useful to first understand why Brian Kernighan and Dennis M. Ritchie included it in their *The C Programming Language* (1978). Those reasons are as valid today as they were over four decades ago.

‘Hello, World’ might seem to be a light-hearted exercise, but it’s not. Completing it requires that you are able ‘to create the program text somewhere, compile it successfully, load it, run it, and find out where your output went.’[^1] This simple programme establishes whether you have the necessary tools and mechanical skills to start learning the language. Without them, any attempt to learn is a theoretical exercise.

This leads to the question: ‘what does a TEI Editor need to be able to do to create his or her transcriptions?’ There is no single correct answer to this question. For some, it might involve nothing more than being able to create valid TEI files. For others, it could mean knowing xPath and even XSLT. My answer to the question treads the middle ground. I believe that all TEI Editors should have the ability to:

1. open, edit and save XML files
2. validate their code against a TEI schema
3. store their work in an environment that helps prevent data loss and enables them to work collaboratively with others

These are the skills that will allow them not only to create valid TEI XML resources but to see their projects through to completion.

## Summary of the exercise

The exercise has three parts.

‘[Installing your XML Editor](/foundational-skills-and-knowledge/installing-your-xml-editor/)’ discusses the application that will be central to your work: your XML Editor. I discuss what an XML Editor is and recommend a couple you might consider using. I then walk you through their installation and configuration.

‘[Work safely by storing all your transcriptions in a Git repository](/foundational-skills-and-knowledge/work-safely-by-storing-all-your-transcriptions-in-a-git-repository/)’ explains what a versioning control system is and why you should use one. I then show you how to create a free private repository on GitHub and to download, install and configure a Git client to use it.

‘[Saying ‘Hello, World’ in TEI XML](/foundational-skills-and-knowledge/saying-hello-world-in-tei-xml/)’ concludes the series. This is the TEI equivalent of the traditional ‘Hello, World’ exercise. You’ll enter the sample TEI code, validate it, correct any errors, save the file and commit it into your git repository.

The successful completion of these three exercises establishes that you have properly installed and configured all the necessary software. It also demonstrates that you can create a valid TEI XML transcription and store it safely within your repository. Having accomplished all this, you’re now in the perfect position to get down to the fun stuff: learning to code in TEI.

*Continue with part one of this exercise by [installing your XML Editor](/foundational-skills-and-knowledge/installing-your-xml-editor).*

[^1]: Brian Kernighan and Dennis M. Ritchie, *The C Programming Language* (1978) pp. 5-6.

