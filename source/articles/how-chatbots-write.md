# How a chatbot writes, and what it can and cannot remember

**Covers:** Chatbot, Next-word prediction, Knowledge cutoff, Token, Context window, Memory

## Fluent is not the same as true {#overview}
A chatbot can write a polished paragraph on almost any topic in seconds. That fluency is easy to mistake for knowledge. To use these tools well, it helps to know how they actually produce text, what they can see while they do it, and what they cannot know. In this article we will go through the mechanism in plain terms.

## Chatbot {#chatbot}
You have probably used one already: a program you talk to, by typing or speaking, which answers in conversation. Chatbots have existed for decades and used to follow scripts. Modern ones are powered by large language models, so they can respond to nearly anything you write. Behind the friendly chat window there is a text generator that produces a reply to the conversation so far.

## Next-word prediction {#next-word-prediction}
How does the generator write? Next-word prediction is the answer. The model looks at the text so far and estimates which piece is most likely to come next. It adds one piece, then repeats, again and again, until the answer is complete. It is like the suggestions your phone's keyboard offers, but vastly more capable, because it has seen enormous amounts of text.

This explains the main strength and the main weakness. Because it has seen so many patterns, it writes fluent, well-organized text. But it is choosing what sounds likely, and it is not looking facts up. It can therefore produce a confident sentence that is false. The model has no built-in check on whether what it writes is true.

## Token {#token}
The model does not read letters or whole words. It reads tokens, small chunks of text, often a short word or a part of a longer one, one at a time. In English, a token is roughly three-quarters of a word, so 100 tokens is about 75 words. Common words are one token, and rare or long words are split into several. Other languages and code often use more tokens per word.

Tokens matter because limits and prices are counted in them, and because the model "sees" the text as tokens, not letters. That is why it can be surprisingly weak at tasks like counting the letters in a word.

## Context window {#context-window}
The model can only keep so much text in view at once, and that limit is the context window. It covers your messages, the earlier replies and any documents you paste in. Everything inside the window can influence the answer. Everything outside is invisible to the model.

Windows differ between tools and have grown a great deal, from a few thousand tokens to hundreds of thousands. When a long chat goes beyond the limit, the oldest parts drop out, and the chatbot may seem to forget what you said at the start. Starting a new chat with a short summary often works better than continuing a very long one.

## Memory {#memory}
Some chatbots can save facts about you between separate conversations, such as your job, your preferences or your family's names, so you do not have to repeat them. That feature is called memory. It is different from the context window, which lasts only for one chat.

Check what the tool has saved, and whether you can view, edit and delete it. A saved fact can be wrong, or private, or no longer useful. Do not rely on it for anything sensitive.

## Knowledge cutoff {#knowledge-cutoff}
The model learned from text collected up to a certain date, and it has no training data after that. That date is the knowledge cutoff. Anything that happened later is unknown to it, unless the tool can search the web. A model with a cutoff last year may confidently describe "the latest" version of something that has since been replaced.

Ask the tool for its cutoff date, and check recent facts, such as prices, laws and news, with a current source.

## A worked example {#example}
You paste a 3,000-word report into a chatbot that has a context window of 8,000 tokens, and ask for a summary. Let's see what fits.

1. Convert words to tokens: 3,000 words divided by 0.75 is about 4,000 tokens.
2. Add your question and the reply: say 200 more tokens. The total of about 4,200 fits within 8,000.
3. Now continue the same chat for an hour, pasting in three more reports of the same size. The total would be about 4,000 x 4 = 16,000 tokens, double the window.
4. The earliest report has dropped out of view. If you ask "what did the first report say about costs?", the chatbot may guess instead of answering from the text.

A better plan: summarize each report in its own chat, then paste the four short summaries into a new one.

Similarly, if you ask "who won last night's game?" and the model's cutoff is a year ago, the answer cannot be reliable, however fluent. A tool with web search can look it up.

## A common mistake {#mistake}
A common slip is treating a smooth answer as a checked answer, or assuming the chatbot remembers everything you ever said. Neither is true. It predicts plausible text, and it sees only what is in the window and in its saved memory.

## Key points {#key-points}
- A chatbot is a conversation tool that is built on a language model.
- It writes by predicting the next piece of text, so fluent text can still be false.
- Tokens, about three-quarters of a word each, are the units for limits.
- The context window is what it can see now. Memory persists between chats. The cutoff is where its knowledge ends.
