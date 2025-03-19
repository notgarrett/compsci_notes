---
date: 2025-03-13
tags:
---
**Project Objective**

Choosing a pair of **skills/topics,** you will create a prompt and the model’s chain of thought (CoT) to that prompt will be generated. The model should be prompted to present its chain of thought (CoT) reasoning while answering the prompt before presenting the final answer. 

You will have the choice to choose both the prompt **complexity level** and **difficulty level.** Your task is to **rewrite** the CoT following guidelines while correcting any errors along the way, until the model eventually reaches the final answer. 

**Complexity levels:** Tag a complexity level based on the educational achievement required to have the tools needed to solve the problem.

- **[9-10th grade, 11-12th grade, lower undergraduate]**
- **Please refer to the complexity guide** [**here**](https://docs.google.com/document/d/e/2PACX-1vT_oMZ8PWzHLkFAHbwDbwVpJ9bKYL170G5NcVHGV_6HjTVZAFqCTRfk-idMtiZadNbzUXr5sdPjYy5l/pub) **on more info.**

**Difficulty Level**: Tag a difficulty level based on the amount of effort required to solve the problem from a qualified student.

- **[easy, medium, hard, competition]**

Prompts are to be constructed using concepts from the **competition level high school and lower undergraduate math questions**. 

Additionally, the prompt should be complex enough that the latest model produces errors in its response. Prompts must be solvable and not rely on brute force computation. Prompts should be structured so that they give a succinct final answer; **please avoid prompts that require proofs or explanations.** Prompts should not be found in any mathematical competition archives. Blatant plagiarism and cheating will result in disables from this project.

Topics of interest include, but are not limited to, **High School Algebra, Geometry, Trigonometry, Combinatorics, Number Theory, Game Theory,** and **Calculus**. 

**If the GTFA in the initial Full Chain of Thought (CoT) is correct, ALWAYS rewrite the prompt, even if there are reasoning errors. Conversely, a prompt should only be considered acceptable if the initial CoT contains an incorrect or incomplete GTFA or lacks one entirely. More info on this later.**

Each skill **must** be incorporated into the prompt and subsequently required for the response in a non-trivial manner. A passing reference to the skill is not enough. 
## **Bad Example**

Given the skills “ratio and proportion” and “geometry”:

- A square garden is to be divided into 4 smaller square plots by two paths that are 1 meter wide and cross each other at right angles. The paths run North-South and East-West, splitting the garden symmetrically. If the total area occupied by the paths is 36 square meters, find the side length of the original square garden.

**Why this is not sufficient:** the prompt trivially includes “ratio and proportion”.

  

## **Good Examples**

Given the skills “exponential growth” and “geometric series”:

- A container starts with 500 mL of water. Each minute, the scientist adds water equal to 1/2 of the current amount. What is the smallest positive integer n such that the number of liters of water in the container is never in the interval [n, n+1]?

Given the skills “recursive functions and sequences” and “multiplication and division”:

- A sequence is defined recursively as follows: the first term a_1 is 2, and for n > 1, a_n = 2^(n-1) + n. What is the logarithm (base 2) of the average of the first 50 terms of this sequence? Round down to the nearest integer.

The ultimate goal of the task is to obtain a correct, verifiable answer to the prompt you’ve written. The model should be used as an assistant in arriving at the answer. The general workflow is outlined below:
  
The ultimate goal of the task is to obtain a correct, verifiable answer to the prompt you’ve written. The model should be used as an assistant in arriving at the answer. The general workflow is outlined below:

1. Write a solvable prompt that induces an error in the model.
2. Ensure that the final answer is **machine-verifiable and succinct (refer to more info below).**
3. Format all math expressions using proper LaTeX.
	1. Review the response and check for errors. The model must produce an incorrect final answer on its first turn. If the model reaches the correct final answer on the first turn, **go back a step and edit the prompt** to make it more complex to stump the model.
	2. Correct the step with the first error occurrence and finish the model’s response all the way to the final answer. Please keep in mind that this may include **both calculation and/or reasoning errors.**
	3. **If the GTFA in the initial full Chain of Thought (CoT) is correct, ALWAYS rewrite the prompt, even if there are reasoning errors. Conversely, a prompt should only be considered acceptable if the initial CoT contains an incorrect or incomplete GTFA or lacks one entirely.**
	4. **You SHOULD NOT mark a Chain of Thought (CoT) as incorrect solely because it is incomplete, there needs to be a valid error in the model generation.**
	5. Mark the first Chain of Thought (CoT) that the model generated where it includes a calculation, arithmetic, reasoning, **or** logical error, and if the step has substantial information, mark that step as **incorrect and rewrite it.**
	6. **Some generated chunking steps may be short such as “let me think about this” or “wait”, this DOES NOT constitute incorrect CoT as this is not a valid mathematical error.**
	7. Continuous repetition by the model’s CoT should be marked as **incorrect**. However, this alone is **not sufficient and does not constitute “stumping the model”.**
	8. Model output formatting errors alone **should not** be marked as incorrect CoT. (LaTeX formatting, grammatical errors, etc).
	9. It is **acceptable** to mark a step correct where the model makes a mistake and corrects itself in the same step. 
	10. If the model makes contradictory mathematical or reasoning claims in a CoT as in the previous steps, the CoT should be marked as **incorrect;** **however, this is not sufficient if this is the only error in the model CoT and does not constitute “stumping the model”.**
	11. For more guidelines on what errors constitute in RW, please refer to this error doc [here](https://docs.google.com/document/d/e/2PACX-1vRMFxO2rNxcp1sSAKT5R7xYkMmAbJZySfRxX_bBve7Nmr0WZxeWf3UqIFripa7fUZ7RTsCyPPsLwRk7/pub) for more information. Please note that this is not meant to be exhaustive.
4. Write a justification for your rewrite.

# **What are Machine Verifiable Answers?**

_Machine-verifiable answers must be numbers, mathematical expressions, or outputs that tools like Python’s SymPy can interpret without ambiguity. We also cannot accept mathematically undefined answers._

_Examples:_

- **_Allowed_**_: "Find the smallest value of θ that satisfies…" (Has a unique answer)_
- **_Not Allowed_**_: "Determine if f(x) is irreducible over…” (Does not require a machine-verifiable answer type)_
- **_Allowed_**_: True/False answers._
- **_Not Allowed_**_: Yes/No questions, infinity (∞) as an answer._

_Note: Proofs are not machine-verifiable and should be avoided._

####   

**_Examples of_** **_allowable_** **_verifiable answer formats:_** 

- Number values: any floating point value or integer
- Expressions
- Symbolic expression (must follow LaTeX format)
- x + y
- \int_0^1 x \dx
- 0 \geq t \geq N
- Variables (can be defined in the prompt)
- Matrices

\begin{bmatrix}

1 & 1 & 0 & 0 \\

1 & 1 & 1 & 0 \\

0 & 1 & 1 & 1 \\

0 & 0 & 1 & 1

\end{bmatrix}

- Sets with explicitly enumerated elements
- \{ 1, 5, 13, 21, 34 \}
- \{ x, z, t\}
- Tuples
- ( x, y)
- (-3, 4)
- Interval notation
- \left( 0 , t \right]
- Boolean value: 
- True
- False

  

**_Examples of_** **_unacceptable_** **_verifiable answer formats:_** 

- Number values with included units
- 5.2 seconds
- 3π223π​ radians
- Plain English final answer
- Yes
- Left
- Middle
- Rule-Defined Sets
- {x > 0 | x \in \mathbb{R}} 
- {n \in \mathbb{N} \mid n \text{ is prime}} 
- {x \in A \mid P(x) \text{ holds}}
- Infinite Sets/Infinity
- \infty
- \mathbb{R}
- (0,\infty)
- Proofs

  

# **Unique Correct Final Answer**

The problem must have exactly **one correct answer (aka GTFA or Ground Truth Final Answer)**.

**_Good Example:_** _“What is the minimum of the roots of x^2 + 5x + 6 = 0?” (Answer: -3)._

**_Bad Example:_** _“Find all the roots of x^2 + 5x + 6 = 0” (Answer: -2 and -3, which violates the one-answer rule)._

Taskers should edit the response by correcting errors and text with the following goals as a guide. The categories are in order of importance, but it is vital that _Deep Thinking_ and _Correct and Comprehensive_ are satisfied.

**Deep Thinking**
- Never rush to conclusions, focus on extensive contemplation
- Express thoughts in natural, conversational internal monologue
- Break down complex thoughts into simple, atomic steps
- Embrace uncertainty and revision of previous thoughts

**Correct and Comprehensive**
- The thought process must lead to a correct final answer at the end of the last step
- The thinking process should not exhibit any laziness in calculations. Intermediate calculation steps should be present, within reason.
- The thinking process should explore all the solution paths that it proposes.

**Avoid Repetition**
- The CoT (Chain of Thought) must not become stuck, repeating similar approaches or the same text in a loop. 
- Repetitive sections should be edited or removed.

**Consistency and Coherence**
- Steps in the thought process should be systematic and coherent throughout.
- Format and tone should be similar throughout the thinking process.
- The thinking process should present a clear, logical, and consistent argument or narrative, with ideas and concepts that are well-connected, well-organized, and easy to follow.

**Appropriate Tone**
- _Informed:_ Info-centric, includes information at the center of responses rather than opinion or emotion. Cites sources when possible.
- _Straightforward:_ Clear and easy to understand. Aims to directly address the prompt. Does not use unnecessarily superfluous, excessive or flowery language.
- _Natural:_ Sentence and paragraph structure vary as a human’s would and feel conversational rather than forced, robotic, or templated. 
- _Non-Judgemental:_ Use of jargon and technical terminology should reflect the complexity of the prompt. 
- _Clear: The grammar and spelling should be correct._

**Formatting**:
- The model generation CoT may lack latex formating in math equations, please write your responses in proper LaTeX formatting

**Prompt** Grading Rubric=
This is the rubric the Reviewers will use to grade your prompts:

![[Pasted image 20250314191120.png]]

﻿**Response** Grading Rubric

This is how your response will be graded by the Reviewers:

![[Pasted image 20250314191138.png]]

**Internal monologue**

It’s recommended to use internal monologue when doing rewrites. Your internal monologue should include these characteristics, below are some examples:

1. **Natural Thought Flow**

```

"Let me think about this"

"Wait, that doesn\'t seem right"

"Maybe I should approach this differently"

"Alternatively, we can"

"Going back to what I thought earlier"

"Upon reflection"

```

  

2. **Progressive Building**

```

"Starting with the basics"

"Building on that last point"

"This connects to what I noticed earlier"

"Let me break this down further"

"Could we have simplified it differently?"

```

  

3. **Exhaustive Calculation**

```

"Let me calculate this explicitly"

"Let me restate the equations until now"

"Let me simplify these equations"

"Instead of looking for shortcuts or generalizations, let me actually try to solve these equations..."

```

  

4. **Verification and Self-check** 

```

"Double-check the algebra and arithmetic"

"Let's verify each step carefully"

"To verify the steps, let's retrace the calculations"

"Let's double-check the reasoning and calculations"

```


**Conclusion:**

If you got to this point in the course, hopefully you have a good idea of tasking on Red Wizards and the project expectations! If you have more questions regarding the project, [**here**](https://docs.google.com/document/d/e/2PACX-1vTZAJrHtrFLKvwZJG9sCgubEvUxbaoHMgR0Ybf-72-TYorcvVS6TgFBDE8qlLn43H5dNtjgWoJBPjL-/pub) is the attempter specification document we made. You can also reach out to us on Outlier Communities if you have additional questions. Happy Tasking!

**P.S. If the link above does not work:** https://docs.google.com/document/d/e/2PACX-1vTZAJrHtrFLKvwZJG9sCgubEvUxbaoHMgR0Ybf-72-TYorcvVS6TgFBDE8qlLn43H5dNtjgWoJBPjL-/pub

# **Appendix:**  

## **LaTeX Guidelines**

Please refer [to this guide](https://docs.google.com/document/d/12wirrYekv_ReVy9FcjvUZWBfCSkRcFAhZ_gbM5k3p_A/pub) for the LaTeX formatting guidelines.

  

## **Helpful Tools**

Use these tools to verify calculations and minimize errors:

- [WolframAlpha](https://www.wolframalpha.com/): Great for general math problems, calculus, and symbolic computation.
- [Desmos](https://www.desmos.com/): Perfect for graphing and exploring functions interactively.
- [Symbolab](https://www.symbolab.com/): Useful for step-by-step solutions in calculus, algebra, and more.
- [GeoGebra](https://www.geogebra.org/): A powerful tool for dynamic geometry, algebra, calculus, and statistics.
- [Calculator.Net](http://calculator.net) - Includes a number of useful calculators including quadratic formula, LCM, GCF, prime factorization, permutations, combinations, triangles, volume, hex, and much more.

  

## **Grammar Assistance**

You only need to install one of the following extensions:

- Quillbot: [Google Chrome](https://chromewebstore.google.com/detail/quillbot-ai-writing-and-g/iidnbdjijdkbmajdffnidomddglmieko) or [Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/quillbot-ai-writing-and-/cphpplikchcioccedpjacdanfibnimmh)
- Grammarly: [Google Chrome](https://www.grammarly.com/browser/chrome)
- LanguageTool: [Safari](https://apps.apple.com/us/app/languagetool-grammar-checker/id1534275760); [Firefox](https://addons.mozilla.org/en-US/firefox/addon/languagetool/); [Google Chrome](https://chromewebstore.google.com/detail/ai-grammar-checker-paraph/oldceeleldhonbafppcapldpdifcinji?utm_source=lt-homepage)