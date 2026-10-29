# Showing examples and improving step by step

**Covers:** Zero-shot prompting, Few-shot prompting, Iteration, Chain-of-thought prompting

## The first answer is a draft {#overview}
Few people get a perfect result from the first request, and that is normal. Two habits raise the quality a great deal. One is to show the AI what a good answer looks like, instead of describing it. The other is to treat the first reply as a draft and improve it in rounds. In this article we will cover both, plus a method for problems that need reasoning.

## Zero-shot prompting {#zero-shot-prompting}
When you ask the AI to do a task with instructions alone, and no examples of a good answer, that is zero-shot prompting. "Write a one-sentence description of this product" is a zero-shot request. It is the easiest approach, and for common tasks it works well.

It struggles when the style or format you want is hard to describe in words, or when your needs are unusual. In that case, you can show the answer you want.

## Few-shot prompting {#few-shot-prompting}
Showing is often easier than telling. In few-shot prompting, you include a few examples of what you want inside the prompt, so that the AI follows the pattern. Two or three examples are often enough. An example carries information that is hard to write as rules: the length, the voice, the structure, the level of detail.

A good set of examples is varied but consistent. If all your examples are short, the AI will write short answers. Label the examples, and end with the new item left unfinished for the AI to complete.

## Iteration {#iteration}
After the first answer comes iteration: improving it through several rounds of follow-up, instead of expecting a perfect result from the first prompt. Each round fixes one thing: "shorter", "less formal", "add a number for each point", "remove the second paragraph".

Good follow-ups are specific and refer to what you saw. "Make it better" gives the AI nothing to act on. "The second sentence is vague. Give a concrete example of a customer saving time" does. Change one or two things at a time so you can tell what helped. Keep the good version, and go back to it if a change makes things worse.

## Chain-of-thought prompting {#chain-of-thought-prompting}
Some questions need several steps, such as a calculation, a comparison or a plan. With chain-of-thought prompting, you ask the AI to work through the problem step by step before it gives the final answer. This often makes the reasoning more accurate, because each step can build on the previous one.

Researchers showed in 2022 that adding a request such as "think step by step" improved results on many reasoning tasks. Some newer tools reason in this way automatically. Even so, you should read the steps. They also let you see where the reasoning went wrong.

## A worked example {#example}
You want short, friendly product descriptions for an online shop. Let's try each approach.

**Zero-shot:** "Write a description for a ceramic mug." The result is generic: "This elegant ceramic mug is perfect for your morning coffee."

**Few-shot:**

```text
Product: wool socks
Description: Warm, soft and made to last. Your toes will thank you.

Product: bamboo toothbrush
Description: Brush clean, feel good. Fully compostable, no plastic guilt.

Product: ceramic mug
Description:
```

Now the result copies the pattern: short, playful and with a benefit in each half. "Hand-glazed and sturdy. Keeps your tea hot and your mornings cheerful."

**Iteration:** You reply, "Good. Make it under 10 words and mention it is dishwasher safe." The next version: "Hand-glazed, dishwasher safe. Mornings made cheerful."

**Chain-of-thought:** For a calculation, ask: "A mug costs 8 dollars and shipping is 5 dollars per order. How much do 3 mugs cost? Think step by step." The reply shows 3 x 8 = 24, plus 5 for shipping equals 29. You can check each step: 24 + 5 is 29, so the answer is right.

Four prompts, each building on the last, took a bland result to a useful one in under five minutes.

## A common mistake {#mistake}
A common slip is giving only one example, so the AI copies it almost word for word. Offer two or three that differ.

A second slip is accepting a chain of reasoning without reading it. The tool can write convincing steps that contain an error, so check the arithmetic and the logic yourself.

## Key points {#key-points}
- Zero-shot prompting uses instructions only. Few-shot prompting adds a few examples to show the pattern.
- Iteration improves an answer through specific follow-ups, one or two changes at a time.
- Chain-of-thought prompting asks for step-by-step reasoning, which you should read and check.
- Treat the first reply as a draft.
