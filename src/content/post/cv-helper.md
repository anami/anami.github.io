---
layout: ../../layouts/post.astro
title: Getting AI to help with job applications
description: Introducing CV Assistant - your private AI-based CV helper
dateFormatted: Feb 11, 2026
---

Does the 'upload cover letter' button fill you with dread?

It's hard going applying for roles. Some websites require just a LinkedIn URL and CV, easy peasy! Some require you to go to an external site and re-enter all your personal details, answer some questions, and add a cover letter. After doing this a handful of times, you think, it's something that you just have to do. After about 20 times, it gets more than tedious, it's hard work.

<div style="width: 100%; aspect-ratio: 16/9; overflow: hidden; border-radius: 0.5rem; margin-bottom: 2rem;">
  <img src="/assets/images/posts/coverletter.png" alt="Cover Letter entry field"  />
</div>

You now have logins to various websites, a bunch of bespoke cover letters and CVs, and you can't remember if you auto-generated passwords for them or not. Your mind is tired from having to conjure up answers for questions you just cannot copy and paste a generic answer to.

<div style="width: 100%; aspect-ratio: 16/9; overflow: hidden; border-radius: 0.5rem; margin-bottom: 2rem; transform: rotate(-2deg);">
  <img src="/assets/images/posts/coverletters.png" alt="Bunch of cover letters"  />
</div>

## A Better Way

After spending more time writing answers and bespoke cover letters, I gave in — there has to be a better way. After getting rejected literally 15 minutes after applying, it wears you down. It certainly wore me down. I would stop dead when I had to answer a question or upload a cover letter.

I was copying and pasting excerpts of my CV to ChatGPT so it could help me at least get started. It became a job in itself, repeating myself for almost every job application.

I've been tinkering with Ollama and RAG systems for a while. I thought perhaps I could have a local version of ChatGPT where I could paste my entire CV and job descriptions without worrying about privacy.

## Introducing AI Career Assistant

<div style="width: 100%; aspect-ratio: 16/9; overflow: hidden; border-radius: 0.5rem; margin-bottom: 2rem;">
  <img src="/assets/images/posts/career_assistant.png" alt="CV Assistant"  />
</div>

I created [AI Career Assistant](https://anami.github.io/ai-cv-helper/), with Claude's help, to streamline my process of filling in job applications. It uses a local Ollama model with a RAG pipeline — you feed it your CV once, and it draws on it to generate tailored cover letters and answer application questions for each role. Because everything runs locally, your personal data never leaves your machine.

You simply paste in a job description, and CV Assistant uses your CV as context to produce relevant, personalised responses. No more repeating yourself for every application.

I'm using it about 30% of the time right now, so it certainly needs further tweaking before I can completely detach myself from ChatGPT. But even at this stage, it's already saving me a good chunk of the repetitive effort. If you're in a similar boat, give it a try — I'd love to hear how it works for you.
