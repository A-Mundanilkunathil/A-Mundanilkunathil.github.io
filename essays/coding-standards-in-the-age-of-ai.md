---
layout: essay
type: essay
title: "The Squiggly Lines Are Not the Point"
image: ../img/coding-standards/bored-squiggle.png
date: 2026-09-24
published: true
labels:
  - Coding Standards
  - ESLint
  - AI
---

<img class="img-fluid rounded pb-3" src="../img/coding-standards/bored-squiggle.png" alt="A robot writing clean code while a bored red squiggly line sits unemployed">

## Do I buy it?

My professor believes that "if you can only implement one software engineering technique to improve quality, it should be coding standards." I do not buy it, at least not in this day and age. If I could only pick one thing to improve software quality right now, it would not be a linter. It would be how systematically you approach the problem and how you approach your prompts, because that is where quality actually gets decided now. The formatting side of quality has quietly become a solved problem, and it was not coding standards that solved it.

## A week of squiggly lines

My honest first week with ESLint: it was irritating. I did not understand why we have to deal with such small trivialities, single quotes versus double quotes, a missing newline at the end of a file. And I think I know why it felt that way. I have become used to using AI for coding, and I have basically never had to deal with linting issues. During the assignments I tried it both ways, writing code with AI and without it, and the AI version came out with no linting issues to fix. The linter had nothing to say. For the world before large language models, I totally understand why this mattered so much. If every character was typed by a human, you needed a tool nagging every human toward the same style. But when the code is generated already conforming, enforcement is no longer the hard part.

## Where I actually draw the line

That does not mean I think nothing in a coding standard matters. I draw the line at the parts that carry meaning: comments, function definitions, and how variables are named and used. Those deserve real attention. The squiggly lines about brackets do not. The difference is easy to see:

```typescript
// passes every lint rule and still tells you nothing
function proc(d: number[]): number[] {
  return d.filter((x) => x > 2);
}

// what I actually care about
// drops readings below the sensor noise floor
function filterNoise(readings: number[]): number[] {
  return readings.filter((reading) => reading > NOISE_FLOOR);
}
```

Both versions make the linter happy. Only one of them helps the next person. I have worked in robotics and hardware, and I noticed that nobody there really cares about coding standards, and honestly it was not a big deal. Most of the work is creating functions, and I write simple comments describing what each function does and name it aptly, so anyone who looks at my code and knows what the machine does can see exactly what the function is for. The meaning-carrying parts of the standard were doing all the work, without any tool enforcing them.

## Coding standards need a rewrite for the LLM age

Here is what I actually think coding standards should become. The standards we are learning were designed for humans typing every line. But today the standard has to be geared toward large language models and how we as software developers interact with them. We need to think about what kind of variable names, what kind of comments, and what kind of function definitions work well when a model is reading and writing your codebase alongside you. Do you want your comments and function descriptions to be actually descriptive and easy to understand, or just super technical definitions? That choice now affects not just the next human reader but what the model does with your code. To me, that is the interesting coding standards question of this era, and a linting rule about quote style does not touch it.

I will also say the startup side out loud: coding standards are very hard to adopt when you are trying to prototype quickly and get things out the door. Nobody stops to set up lint rules mid sprint, even though skipping them is exactly how small long-term problems pile up. I have lived that tradeoff and I understand why it happens.

## Will I set it up on day one?

Honest answer: no. On my own next project I will not be installing ESLint on day one, because for me it is annoying and a waste of time I would rather spend building. What I will do instead is tell my large language model that these are the coding standards in place for this project and this organization, and let the code come out conforming from the start. Right now I use ESLint because my assignments force me to. That is the truthful state of things, and I think it points at where this is all heading: the standard stops being a gate you pass at the end and becomes part of the instructions you give at the beginning.

## How AI was used for this essay

This essay was written from answers I voice typed to interview questions about the module. I used Claude to organize my own spoken sentences into sections and clean up grammar and transcription errors. The opinions, experiences, and examples are mine from those answers. The header image is AI generated.
