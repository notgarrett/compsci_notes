---
date: 2025-03-13
tags: 
---
The purpose of this project is to help a customer hone its model to take on increasingly challenging everyday prompts. This prompt generation project has two main components: **prompt, model error identification, and correct response**. Your job is to create prompts that represent challenging real-world use cases. You will create prompts that cause AI models to make **reasoning** **errors** and provide the objective correct answer so the model can learn from its mistakes. 🤖

**Step 1. Understand the Prompt Requirements** 

When writing a prompt, you’ll be asked to write within a specific **domain -** this is a suggestion based on current project needs, so you are encouraged to follow this topic but it is not mandatory if it is a poor fit.  Here’s a brief explanation of each one of those requirements

**Domain**

![[Pasted image 20250313162846.png]]
﻿The best prompts read like authentic human communication - straightforward, purposeful, and focused on the task at hand. If you need inspiration, check out your previous interactions with LLMs for prompt ideas!

  

Write a prompt that is:

1. ✅ **Natural** - Prompts are written conversationally and reasonably clearly, the way that someone would actually "talk" to a chat bot, friend or colleague. Writing isn't overly formal or so casual that it's hard to understand.
2. ✅ **Complex** enough that they require the model to reason - Prompts must ask for more than simple trivia that could be quickly retrieved in a simple Google search. Prompts must require a model to use some reasoning or judgement, or to curate information that isn't otherwise easily retrievable.
3. ✅ **Close-ended** so that there is only one correct response to the prompt and it can be quickly and objectively identified as correct or incorrect based on reputable data or mathematical principles. 

**✅ Prompts should:**

1. Sound natural and realistic
2. More complex than trivia that can be answered through a simple Internet search
3. The prompts should make the model fail naturally in reasoning **and** final answer. 
4. The prompts should follow the domain type 
5. Prompts should have a single, correct answer that can be objectively evaluated
6. Prompts are topically diverse
7. Prompts do not rely on real-time information

  

**⛔️ Prompts shouldn’t HAVE:**

- Unnecessary constraints
- Justifications for constraints
- A backstory unless it's necessary
- Stacked questions
- Multiple possible answers

**✅ Good Prompts**

- ✅ **Prompt**: How many squares of prime numbers are also perfect numbers?

  

- ✅ **Prompt**: A standard deck of 52 playing cards contains 13 hearts, 13 diamonds, 13 clubs, and 13 spades. You draw cards one at a time without replacement until you draw two hearts.

Let X be the number of draws required to get the second heart.

What is the expected value of X?

-  ✅ **Prompt**: Consider an ant moving in the x-y plane. The ant's goal is to move from (-1,2) to (1,-1) following the shortest path that adheres to the following constraints:

* The path must be comprised of exactly two line segments.

* Each line segment must start and stop at points with integer x and y coordinates.

* The path must not pass through or touch the circle x^2 + y^2 = 1/3.

  

What is the length of the path that satisfies these constraints?

  

- ✅ **Prompt**: Jessica's private safe password consists of 7 unique digits. Four people made the following guesses:

A guessed: 5381467

B guessed: 9204813

C guessed: 7038941

D guessed: 2973416

Jessica then made the following statement: "Each of you has guessed exactly two correct digits, but these two digits are not adjacent to each other in your respective guesses."

With this information, what's Jessica's private safe password?

  

A. 5234917

B. 7038941

C. 2084917

D. 7918263

  

  

⛔️ **Bad Prompts**

- 🟥 **Prompt**: I'm a big fan of Harry Potter. I wanted to make a video for my channel and I need some information. Which spells used in the saga are most used and mentioned by wizards? Do a check and show the order of the 10 most mentioned in the saga. Next to each one, describe what it is for and what it does to the opponent. To enrich my video, I also want to know the name of the character who uses each spell the most, check that for me.
- **Not related to reasoning.**

  

- 🟥 **Prompt**: How many ducks would be in a pond if it’s spring and the last count was 40?
- **This problem doesn’t have a correct answer as it’s highly subjective to know how many duck the pond would have**.

  

- 🟥 **Prompt**: What’s the value for x if the equation is x+5=10
- **Too simple that the model wouldn’t fail**

![[Pasted image 20250313162917.png]]
When evaluating the model failure, you’ll have to confirm that **both** of the following are true for at least one response:

  

✅ The response must contain a clear **reasoning error**, which should be in the **steps the model takes to come to a final answer**.  A reasoning error does **not** include:

- Inaccurately citing a number or piece of information
- Misinterpreting or making an incorrect assumption about the “ask” of the prompt
- Solutions steps that are in themselves correct/logical but violate prompt instructions
- Intermediate calculations which are incorrect

  

A reasoning error **does** include:

- Deductions which are **inconsistent with the** information presented 
- A progression where one step does not make **logical sense** based on the previous one and which is **not justified** by any reputable information or problem-solving strategies

✅ The **final answer** provided in the response is incorrect:

- For **numerical** answers, a wrong final answer must differ from the correct answer by more than 10% in either direction
- For **categorical** answers, the model’s final answer(s) must be definitively incorrect and cannot simply be misspellings or alternate names for the same object

![](https://static.remotasks.com/uploads//8df10ddc-8469-4424-a1cf-9d9d11181b6b/image.png)

Finally, when you confirm whether or not the model failed on reasoning and final answer, you will also be asked to explain the error - do so **clearly and concisely** in a single sentence and be sure to indicate **which response(s)** contained the error.

  

﻿![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe2hfB7fSI5EtuA-M5h3n3XlPy5F0YTr6dac0lw9c9VvLREm_-CCo1hBVUqeLLfDkeSTjI8JEfCDOxhYWHiq3FJqgzLMhlL0XdYZ0u6ZjQgs2pII3zqzLS_Eu4KAe5qWhw_yTJrRA?key=THSO8z3FOVfgqOLR7Jb_CMyi)

## **What happens if the model doesn’t fail in any of the error type categories?**

  

One of the most important parts of writing prompts is to naturally make the model fail in both reasoning and final answer - however, when none of the responses fail, you must come up with another prompt. To create a new prompt, follow these easy steps: 

1. Click on the reload symbol ⟲
2. Create a new prompt and click “Finish editing” 

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfalP-dSf6xZqKzHe4jmRb50H8OMP2109QHDNSaKtUOO_I41ejHvuBSpQRVl0L_KgH8J_6MgVKrobDMnmAAJriA6QtSw_rAnIeFeOwe6XLL9jQgN8Vh6fIvaGax_MJMuzC-qHdm9w?key=THSO8z3FOVfgqOLR7Jb_CMyi)

_Example video on how to create a new prompt_

  

Some possible ways to retool your prompt to encourage a model failure:

- Make your ask **specialized** and focused on details or subject matter you are highly knowledgeable on
- Think of ways that your prompt can force the model to make **more decisions and logical leaps**
- Be creative with the details in your prompt, and think of ways to create ambiguity, double-meanings and misreads without being unnaturally opaque
- Add **a natural constraint** that increases the complexity of the prompt without making it contrived or less human-sounding


Finally, provide the **single correct answer** to your prompt in the box below the responses.  This answer should be as concise as possible and should **not** include reasoning steps, unless this is an explicit ask of your prompt (and there is only one possible set of solution steps).  Verify that:

- Your answer is the **only correct answer** to the given prompt (not including order, in the case of an unordered list)
- Your answer is sufficiently different from the one(s) you have identified as incorrect in Step 3:
- For **numerical** answers, a wrong final answer must differ from the correct answer by more than 10% in either direction
- For **categorical** answers, the model’s final answer(s) must be definitively incorrect and cannot simply be misspellings or alternate names for the same object
- Your answer complies with any formatting, labelling or units specifications set in the prompt

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXchNejTDDU3NAnpZRpAGF5ysfr3uKAPrbq2LIdyQ-N48stRYO1jdmTtnFva5zfm7ZCT6gaAOS30I7XYYDyjtkFdBmUjW7QFWWNW8JKlFu0AF0jNshG9YVW3uVoU5ry4QrD_vhni?key=THSO8z3FOVfgqOLR7Jb_CMyi)

  

Once you’ve checked all the above, you can hit the purple **Save and Continue** button! ⬆️

To avoid some of the **common errors** made on this and other reasoning projects and set yourself up for success, please review the following examples and keep them in mind as you determine whether you have written a **high-quality prompt** and found **real reasoning errors**

![](https://static.remotasks.com/uploads//f65f14c3-0347-4a43-95c7-5fe41ec18717/image.png)

Evaluate the following prompt and determine if it's high or low quality based on the guidelines of the project:

- **Topic: Life Sciences & Biolog**y

**Prompt**_: can you help me create a training plan to run a half marathon? I'll be running it on november 9 and today is march 3, my goal is to finish it in 2 hrs_

Good quality

**Bad quality**

What happens if the model only fails in one of the following categories per response?

- **Incorrect Final Answer**
- **Presence of Reasoning Error**

Nothing, the model is good and I completed my part

**I have to make a new prompt until the model fails in any of the model-failure categories**