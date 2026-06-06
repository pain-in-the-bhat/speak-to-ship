# A friend teaches you Wispr Flow

I've been using Wispr Flow for a few months now. It's a voice dictation app that works in any text field on your computer or phone. Here's what I wish someone had told me when I started.

---

## What it actually does

You press a hotkey, you talk, and Flow types what you said — but cleaned up. No "ums," no false starts, no mid-sentence corrections left in the output. If you say "let's meet at 2, actually 3," it writes "Let's meet at 3." If you ramble, it structures the output.

This sounds small but it's the difference between a tool you use and one you abandon after a day. Built-in dictation (macOS, Windows, whatever) gives you raw transcripts with every "um" and correction. Reading them back is painful. Flow gives you text that looks like you typed it deliberately.

It runs on Mac, Windows, iPhone, and Android. Your dictionary, snippets, and settings sync across devices.

---

## Why you might want it

The obvious reason is speed. People speak at ~150 words per minute and type at ~40. That math is real, but it undersells what's actually good about it.

The thing I didn't expect: **speaking forces you to give AI more context.** When you type a prompt to an AI coding tool, you tend to be terse — "fix the auth bug." When you speak it, you naturally include more:

"Fix the authentication bug in the login flow. The issue is that the JWT token isn't being refreshed properly after expiry. Check the middleware in auth.ts — we added a refresh mechanism last week but it seems to only work on the first attempt, then fails silently on retries. The user should be redirected to the login page with a message if the refresh fails too."

That second prompt is going to get a much better result from any AI. Flow makes it effortless to produce.

The other reason: **it saves your hands.** If you code all day, adding typing to every Slack message, email, PR description, and doc edit — that adds up. Voice offloads a surprising amount of that.

---

## The core features that actually matter

### AI Auto Edits

This is the main thing. Flow removes filler words, handles mid-sentence corrections, detects punctuation from pauses and tone, and formats numbered lists automatically. You don't have to think about any of it.

You say: "Um, so the thing is, we need to, uh, add rate limiting to the, actually no, let me think — we need to add rate limiting to the API endpoints for the payments service. It should be, like, 100 requests per minute per user. And we need to return a, you know, a four twenty nine status code when they hit the limit."

Flow writes: "We need to add rate limiting to the API endpoints for the payments service. It should be 100 requests per minute per user, and we need to return a 429 status code when they hit the limit."

### Personal Dictionary

Flow learns words you use that aren't in standard dictionaries. When you correct a spelling, it remembers. You can also add terms manually: project names, team member names, framework names, API endpoints.

After a week of use, it stopped misspelling "Supabase" and "Vercel" for me. Small thing, big quality-of-life improvement.

### Snippets

You can set up voice shortcuts for text you type repeatedly. Say a trigger phrase, Flow pastes the full block.

Useful ones I've set up:
- "pr checklist" → a markdown checklist I use for every PR review
- "standup update" → a template with yesterday/today/blockers
- "bug report" → steps to reproduce, expected, actual, environment

The time savings here are honest. If you type the same PR template 20 times a week, that's real.

### Styles

Desktop and English only for now. Lets you set the tone: formal for docs, casual for Slack, enthusiastic for emails. It adjusts word choice and structure accordingly.

I mostly leave it on casual. The formal mode is useful for client-facing writing.

### Command Mode

You can give Flow instructions like "shorten that paragraph" or "turn this into bullet points" or "make this sound more professional." Access it from the Flow Hub. It's similar to asking an AI to edit text, but it works on whatever you just dictated.

### Whisper Mode

Works when you're whispering. Requires a mic close to your mouth — headset, gooseneck, or clip-on lavalier. Useful in open offices, coffee shops, or anywhere you don't want to be the person talking to their computer.

### Prompt Engineer (Opt+2)

This takes your dictated prompt and automatically structures it for AI tools. It adds a title, role definition, task description, context, and format specification. If you're using Flow to feed prompts into Cursor, Claude, or ChatGPT, this is worth knowing about.

---

## How it works with dev tools

### Cursor and Windsurf

Flow has specific integration with these editors. When you dictate in Cursor or Windsurf, Flow recognizes filenames as you speak and automatically tags the right file in your workspace. This means the AI gets full file context without you manually attaching anything.

It also handles code syntax correctly — camelCase, snake_case, acronyms, CLI commands, exact spacing. Dictation used to mangle these. Flow doesn't.

### VS Code, GitHub, Warp Terminal

Flow works in any text field in VS Code — terminal, editor, comments, everything. GitHub PR descriptions and code reviews are voice-friendly. Warp Terminal has native Flow integration for speaking shell commands.

### Everywhere else

Slack, Linear, Notion, Gmail, Obsidian, Google Docs, iMessage, WhatsApp — Flow works anywhere with a text field. It's not app-specific. It's system-level dictation that lands wherever your cursor is.

---

## Microphone stuff

### You probably don't need new hardware

Your built-in mic works fine. Most audio problems are configuration, not hardware. Before buying anything:

- In Flow's mic picker, select your mic manually instead of using Auto-detect
- Make sure your OS sound settings and Flow agree on which mic to use
- Restart Flow after switching audio devices
- Disable virtual microphones (NVIDIA Broadcast, VoiceMeeter, Teams Audio) — they can interfere

Wired earbuds or your webcam mic often work better than the built-in one. Try what you already have first.

### If you do want better hardware

The hierarchy for dictation accuracy: **wired > WiFi dongle > Bluetooth.** Bluetooth mics can be slow to connect, clip the first word, and introduce transcription errors. If you must go wireless, get something with a USB dongle (like Jabra Evolve2 Buds or Sony INZONE Buds) — they bypass Bluetooth profile switching.

For whisper dictation in shared spaces, you need a mic close to your mouth: a gooseneck mic, a podcast USB mic on a boom arm, a clip-on lavalier, or a boom mic that attaches to existing headphones.

### Clamshell mode warning

If you use a MacBook with the lid closed, the built-in mic is disabled. You need an external mic. Flow detects this and will tell you.

---

## How I actually use it

My workflow isn't some elaborate system. It's simple:

**Coding:** I type the code. I dictate the prompts to the AI. Speaking a detailed prompt into Cursor with automatic file tagging gets better results than typing a short one. It's not about speed — it's about the quality of context.

**PR descriptions:** I finish a PR, hit the hotkey, and talk through what I changed and why. Flow formats it. I paste into GitHub. Takes 30 seconds instead of 5 minutes of typing and formatting.

**Slack and messages:** Any reply longer than two sentences, I dictate. It's faster and, oddly, my dictated messages are better written than my typed ones — probably because speaking forces complete sentences.

**Documentation:** After finishing a feature, I open a doc and describe what I built and how it works. Flow structures it. I clean it up. Documentation that would've taken 45 minutes to type takes 15.

**Commute capture:** I use Flow on my phone when an idea hits. Open a note, dictate it. Review and clean up when I'm back at my desk.

---

## Things I wish were different

**The name "Wispr Flow" makes it sound like a meditation app.** I've had to explain to multiple people that it's dictation software, not a wellness product. This is a minor complaint but it's real.

**Styles are English-only and desktop-only.** I understand why — tone detection across languages is genuinely hard — but it means the feature doesn't work on mobile, which is exactly where I'd want it (quick messages on the go).

**The pricing is fair but the team features are enterprise-y.** $12/month for individual Pro is reasonable. Team plans get shared dictionaries and snippets, which are genuinely useful for consistency across a team, but the pricing and setup feel designed for companies with procurement departments, not five-person startups.

**There's a learning curve to dictating naturally.** The first week, I sounded like I was reading a script. You get better at it. Now I talk normally and Flow handles it. But nobody warns you that you have to learn to speak to a computer without sounding like you're speaking to a computer.

**Occasional hallucinations on technical terms.** Flow gets most dev jargon right. Sometimes it confidently writes something that sounds like code but isn't. Like any AI tool, you need to review the output before shipping it.

---

## Pricing

- **Flow Pro:** $12/month. 14-day free trial, no card required.
- **Teams:** $12/user/month. Centralized billing, shared dictionaries and snippets, usage dashboards.

Enterprise plans add SOC 2 Type II, ISO 27001, and enforced HIPAA compliance.

---

## Where to find more

- **Website:** [wisprflow.ai](https://wisprflow.ai)
- **Help Center:** [docs.wisprflow.ai](https://docs.wisprflow.ai)
- **Developer page:** [wisprflow.ai/developers](https://wisprflow.ai/developers)
- **Microphone guide:** [wisprflow.ai/microphones](https://wisprflow.ai/microphones)
- **AI prompting guide:** [wisprflow.ai/ai-prompting-guide](https://wisprflow.ai/ai-prompting-guide)

---

*If something in here is wrong or outdated, it probably is. Wispr Flow updates often. Check the official docs when it matters.*
