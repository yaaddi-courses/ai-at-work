# Everyday work tasks: writing, meetings, learning and data

**Covers:** Style sample, Transcript, Analogy, Data cleaning

## Where AI saves time at work {#overview}
Most useful work with AI is not dramatic. It is small tasks done faster: a first draft in your own voice, notes from a long meeting, an explanation of something unfamiliar, a messy table made tidy. In each case the pattern is the same: give the AI good material, ask for a specific result and then check it. This article shows four such uses.

## Style sample {#style-sample}
A style sample is a piece of your own writing that you paste into a prompt so that the AI copies your voice and your word choices. Without one, AI writing tends to sound like everyone else: smooth, generic and a little too enthusiastic. With one or two short samples, such as a few emails you wrote, the draft sounds more like you.

How to use it: paste the sample, say what to copy ("sentence length, how I greet people, how formal I am"), and then give the task. Review the result against your own sense of your voice. Use only samples that you are allowed to share. Do not paste a client's private email.

## Transcript {#transcript}
A transcript is a written, word-for-word record of a spoken meeting or call. Many meeting tools can create one automatically. It becomes much more useful when AI summarizes it: key decisions, who does what by when, and open questions.

Practical points: a transcript can contain mistakes, especially names, numbers and technical terms, so check those against your memory or the recording. Make sure everyone consented to recording, and follow your privacy rules. For long transcripts, ask for the decisions and action items first, and then for more detail where needed.

## Analogy {#analogy}
An analogy is a comparison that explains something new by likening it to something you already know. "A firewall is like a security guard at the door of a building" helps a beginner immediately. AI is good at producing analogies on request, and at tailoring them: "Explain compound interest using an analogy from cooking, for a teenager."

Treat analogies as a way in, not as the full truth. Every analogy breaks down somewhere, so ask the AI where the comparison fails, and check the facts after the picture is clear.

## Data cleaning {#data-cleaning}
Data cleaning is fixing messy data, such as duplicates, typos and inconsistent formats, so that it is ready to be analyzed. A column with "NY", "New York" and "new york" counts the same city three times. Dates in different formats cannot be sorted.

AI can suggest formulas, write a short script or propose consistent names. But it can also quietly change values or invent them. Work on a copy, test on a small sample, and compare the counts before and after.

## A worked example {#example}
You have a customer list with inconsistent city names and want a clear count per city.

| Raw entries | Count (raw) |
|---|---|
| NY | 3 |
| New York | 5 |
| new york | 2 |
| Boston | 4 |
| boston | 1 |

You ask the AI for a rule: "make all names lowercase, then replace 'ny' with 'new york'". Check it by hand on the sample:

1. New York: 3 + 5 + 2 = 10 entries after the rule.
2. Boston: 4 + 1 = 5 entries.
3. The total before cleaning is 15 entries, and after cleaning it is 10 + 5 = 15. The counts match, so no row was lost or invented.

The same pattern fits the other tasks. For a transcript, check one decision against the recording. For a style sample, compare the draft with a real email. For an analogy, ask where it breaks.

Time saved is real: cleaning by hand might take half an hour for a thousand rows, and the AI rule plus your 5-minute check takes less than ten minutes.

## A common mistake {#mistake}
Trusting the tool's result because it looks tidy. Cleaning, summaries and analogies all look convincing even when they are wrong. Another mistake is pasting private data into a public tool to save time. Use the approved tool, and remove personal details first.

## Key points {#key-points}
- A style sample makes drafts sound like you. Use your own writing only.
- A transcript plus an AI summary gives fast notes, but check the names and numbers.
- An analogy is a good first step. Ask where it fails.
- Data cleaning needs a before-and-after check, and work on a copy.
