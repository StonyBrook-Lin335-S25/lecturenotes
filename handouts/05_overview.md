---
title: Computational Linguistics Handout
author: Thomas Graf
date: 2025-01-27
geometry: margin=1in, letterpaper
fontsize: 12pt
numbersections: true
fontfamily: mathdesign
fontfamilyoptions: charter
---

**Disclaimer**  
These handouts serve as a succinct reference of what was covered in a given class.
They are not meant to be a substitute for attending class and probably won't make much sense to you unless you were there.

# Computational linguistics & NLP

- Computational linguistics is a diverse area that spans multiple fields (linguistics, computer science, psychology, cognitive science, and more).
- Computational linguistics as engineering
    - solving language-related tasks with computers
    - focus on getting things done, pursuit of better tools
    - a good solution is a good solution even if we don't know why it works
- Computational linguistics as science
    - what can we learn about language using computational techniques (not necessarily computers, this could also be math, theory)
    - focus on understanding things, pursuit of deeper knowledge
    - a deep insight is a deep insight even if we don't know how to make it work
- Natural Language Processing (NLP) is often used to explicitly refer to the engineering part of computational linguistics, i.e. using computers to solve language-related tasks

# Three phases of computational linguistics

- As any field, computational linguistics has a complex history with lots of subtleties and nuances.
- This quick summary ignores all of that, painting the history of the field in the broadest strokes.
- It's the equivalent of a 10 minute Youtube video, don't expect more than the general gist.

## Hand-written systems (late 50s to late 80s)

### History

- Several independent developments in the late 50s
    - Noam Chomsky's work on generative grammar and formal language theory turns heads.
      Generative grammar endorses mathematical concepts, studies natural language through a computational lens.
    - vital role of computers for the Manhattan project has resulted in increased funding for building computers and making them do stuff
    - great interest in large-scale tasks related to language (e.g.~DOD interest in automatic translation of Russian communications)
- And thus, the field of computational linguistics is born.

### What was it like?

- **Systems**: based directly on linguistic theories, crafted by hand
    - *Example*: modeling rewrite rules in phonology (sound grammar) as finite-state transducers
    - *Example*: using context-free grammars to assign tree structures to sentences
- **Rules**: also crafted by hand, often by linguists 
    - *Example*: rewrite rule for stress assignment in English words
    - *Example*: designing a context-free rule for topicalization in English (as in *this phrase, somebody has topicalized by moving it to the beginning of the sentence*)

### Pros and cons

- Why was it a great time for computational linguistics?
    - tons of new ideas and approaches, many of which are still in use
    - since everything is designed by humans, it is perfectly clear how everything works
    - computational linguistics was truly interdisciplinary, with linguists, computer scientists, logicians and philosophers all working together to make progress
    - computational linguistics was the poster child of "old school AI": understanding human cognition by trying to make computers to act like humans
- Why was it a bad time for computational linguistics?
    - computers were incredibly limited (slow CPU, very little memory, often they didn't even have a hard drive); this greatly limited what kind of ideas could be explored
    - a lot of the stuff simply didn't work well; all the theoretical advances did not translate to real-world problems

## Probabilistic turn (early 90s to early 2010s)

- Some big changes in the computing landscape:
    - CPUs have gotten a lot cheaper and faster.
    - While still expensive, hard drives are becoming increasingly popular.
      By 1995, a consuer computer may well have a hard drive that can store over 1GB.
      Just a few years prior, you still had computers that could only use floppy disks, each one of which holds 1.44MB.
    - Computers are becoming increasingly ubiquitous, there's a real market there now (e.g. spell checking, speech recognition, speech synthesis).
- Computational linguistics is changing from a purely academic/governmental enterprise into an economically viable business proposition.
- Finally it becomes feasible to process large amounts of data to extract statistical regularities from them.
- Computational linguistics becomes all about finding generalizations in that data and integrating it with computational systems.

### What was it like?

- **Systems**: still based directly n linguistic theories, crafted by hand
    - *Example*: modeling rewrite rules in phonology (sound grammar) as finite-state transducers, but with probabilities guiding the transducer
    - *Example*: using context-free grammars to assign tree structures to sentences, but with probabilities telling us how likely certain constructions are in certain contexts
- **Rules**: creating the rules becomes increasingly automated
    - *Example*: set up a transducer that covers all logically possible options for English stress assignment, then use data to automatically estimate the probabilities for those options
    - *Example*: set up a grammar that covers all logically possible structures for English sentences, then use data to automatically estimate the probabilities for the rules

### Pros and cons

- Why was it a great time for computational linguistics?
    - we finally got systems that work reasonably well, and they weren't super-expensive; a normal person could buy the speech-to-text software *Dragon Naturally Speaking* for a reasonable price
    - the focus on probabilities created models also pushed the research forward, e.g. sentence processing (how do humans assign structure to sentences?) or semiring parsing (an algebraic abstraction of parsing algorithms)
- Why was it a bad time for computational linguistics?
    - the focus on real-world performance meant that niche problems that occur only rarely were completely ignored, even if getting those things wrong could have very bad consequences
    - engineering concerns were starting to consistently outrank scientific concerns
    - as a result, the different fields that had contributed to computational linguistics so far were no longer seeing eye to eye, drifting apart
    - Frederick Jelinek (IBM): "Every time I fire a linguist, the performance of the speech recognizer goes up."

## The neural network boom (early 2010s to present day)

- Neural networks have been around for the 1950s but simply didn't work all that well.
  Computers were too slow to handle large networks, and there wasn't enough data to train them on.
- But by 2010, all of that had changed.
    - Computers had gotten a lot more powerful (GPU computing)
    - a lot more data available, largely thanks to billions of people posting on the internet.
- Finally it is possible to "brute force" language by throwing more and more computing power and more and more data at it.
- We don't know yet how this phase of computational linguistics will turn out, but there is no doubt that this is the first time that it's tools and techniques are truly shaping the world.

### What is it like?

- **Systems**: they contain barely an ounce of linguistics, almost all is inferred from data
- **Rules**: same deal, all done automatically via machine learning

### Pros and cons

- Why is it a great time for computational linguistics?
    - computational linguistics has become mainstream and is actively powering the AI revolution
    - the field is bigger than ever before, with lows of new blood bringing exciting new ideas
    - scientists are trying to use neural networks to gain new insights into human cognition
    - there is now something resembling a standardized career path in computational linguistics, and it pays six figures
- Why is it a bad time for computational linguistics?
    - neural networks are black boxes, we have no idea what they're doing
    - old school AI as a means of understanding human cognition is largely dead, replaced by AI as a business proposition
    - because many businesses don't share their model architectures or training frameworks, improvements in specific models do not translate into an improvement for the whole field; knowledge is no longer shared like it was in the 90s
    - neural networks have no safeties and no guarantees; while they may do a great job in 99% of the cases, there's no limit on how bad things can go for the remaining 1% (think self-driving cars running over pedestrians)
    - the need for huge amounts of data puts smaller languages at a technological disadvantage
    - the models replicate and reinforce biases in the data (remember Microsoft's Tay turning into a raging racist?)
    - because there's so many new people entering the field, a lot of history has been forgotten and people keep reinventing the wheel
