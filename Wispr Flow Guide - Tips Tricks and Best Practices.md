# A friend teaches you Wispr Flow

I've been using Wispr Flow for about a week. This is not an endorsement — I wrote [a whole essay](https://gurubhat.xyz/posts/what-we-lost-on-the-way-to-faster.html) about what gets lost when you replace typing with voice. The short version: the friction of typing *is* the thinking. The pause before you commit to a word is selection pressure. Voice collapses that pause. You commit to the first adequate framing instead of the best one.

I still believe that.

But I'm also curious whether there are specific situations where voice dictation earns its place — not as a replacement for thinking-through-typing, but as a tool for a narrower job. So I'm running an experiment: a week of using Flow to dictate prompts into OpenCode on my MacBook Pro, at home, by myself. No external mic. Just talking to my laptop.

This guide is what I've learned so far. It covers what Flow does, what's been useful, what's been broken, and what I'm still undecided about.

---

## What it actually does

You press a hotkey, you talk, and Flow types what you said — but cleaned up. No "ums," no false starts, no mid-sentence corrections left in the output. If you say "let's meet at 2, actually 3," it writes "Let's meet at 3."

This is genuinely different from built-in dictation (macOS, Windows, whatever). Those give you raw transcripts with every "um" and correction. Reading them back is painful. Flow gives you text that looks like you typed it.

It runs on Mac, Windows, iPhone, and Android. It works anywhere there's a text field — your IDE, your terminal, your browser, your messaging apps.

---

## What I'm actually using it for

Just one thing: **dictating prompts into OpenCode.**

When I'm working in the terminal, I hit the Flow hotkey, speak a detailed prompt, and Flow types it into OpenCode's input. That's it. No snippets, no styles, no Cursor file tagging, no Prompt Engineer transforms. I haven't explored any of that.

The theory I'm testing: speaking a prompt forces me to include more context than typing one. When I type "fix the auth bug," I get a short prompt and a hit-or-miss result. When I speak it, I naturally include which file, what the symptoms are, what I already tried. That richer prompt gets better AI output.

Whether that's worth the tradeoff — losing the selection-pressure pause that typing creates — is what I'm trying to figure out.

---

## The features that exist (whether I use them or not)

### AI Auto Edits

The core thing. Flow removes filler words, handles mid-sentence corrections, detects punctuation from pauses and tone. You don't think about it.

### Personal Dictionary

Flow learns words it doesn't know. When you correct a spelling, it remembers. You can add terms manually: project names, framework names, whatever. It syncs across devices.

### Snippets

Voice shortcuts for text you type repeatedly. Say a trigger phrase, Flow pastes the full block. I haven't set any up.

### Styles

Adjusts tone — formal, casual, enthusiastic. Desktop and English only. Haven't used it.

### Command Mode

You can tell Flow to "shorten that paragraph" or "turn this into bullet points." Access it from the Flow Hub.

### Whisper Mode

Works when you're whispering. Needs a mic close to your mouth.

### Prompt Engineer (Opt+2)

Takes your dictated prompt and auto-structures it for AI tools — adds a title, role, task description, context, format spec. Haven't used this either.

### Dev tool integration

Flow has specific integration with Cursor and Windsurf (file tagging from speech, syntax awareness) and native integration with Warp terminal. I only use it with OpenCode, so I can't speak to any of this.

---

## Hardware (or lack of it)

I use the built-in mic on my MacBook Pro. No external hardware. I'm at home, alone, so there's no social awkwardness to manage.

I have AirPods Pro that I might try at some point if I need better audio quality or want to test whisper mode, but I haven't yet.

If you're considering hardware: wired beats wireless beats Bluetooth for dictation accuracy. Bluetooth mics can be slow to connect, clip the first word, and introduce errors. But honestly, try your built-in mic first. Most audio problems are configuration, not hardware — select your mic manually in Flow's settings instead of using Auto-detect, and make sure your OS and Flow agree on which mic to use.

---

## Things that have gone wrong

### Transcriptions over a minute just... fail

This was the most frustrating issue. For a period, any dictation longer than about a minute would simply not produce output. The recording would stop, no text would appear. I suspect network congestion or a backend timeout, but I never confirmed the cause. It seems to have resolved itself, but it was bad enough that I nearly abandoned the experiment.

If you're trying Flow and hitting this, know that it's not just you. Restarting the app sometimes helps. Sometimes it doesn't.

### The learning curve is real

The first few days, I sounded like I was reading a script. You have to learn to talk to a computer without sounding like you're talking to a computer. It gets better. But nobody warns you about this.

### Occasional mis-transcriptions of technical terms

Flow gets most dev jargon right. Sometimes it confidently produces something that sounds like code but isn't. You need to review the output.

---

## What I'm still trying to figure out

The blog post I wrote in April argued that the friction of typing is load-bearing — it's not waste, it's the process. The pause before you commit to a word is where the thinking happens. Voice collapses that pause.

I still think that's true for writing. For constructing an argument. For work where the path to the idea matters as much as the output.

But dictating a prompt to an AI coding agent is not quite the same activity. It's more like giving instructions to a junior developer — you're describing what you want, not composing an argument. The cognitive mode is different. The stakes are lower. A bad prompt gets a bad result and you iterate.

So maybe voice dictation has a narrow lane where it's genuinely useful without the friction loss being a problem. Or maybe it doesn't, and after this week I'll go back to typing everything. I don't know yet.

---

## Pricing

- **Flow Pro:** $12/month. 14-day free trial, no card required.
- **Teams:** $12/user/month with centralized billing, shared dictionaries and snippets.

Enterprise plans add SOC 2 Type II, ISO 27001, and HIPAA compliance.

---

## Where to find more

- **Website:** [wisprflow.ai](https://wisprflow.ai)
- **Help Center:** [docs.wisprflow.ai](https://docs.wisprflow.ai)
- **Microphone guide:** [wisprflow.ai/microphones](https://wisprflow.ai/microphones)

---

*This guide reflects my experience as of June 2026. I'm a week into using Flow, skeptical but curious. If you read this months later and I've either abandoned it or integrated it deeply, neither outcome would surprise me.*
