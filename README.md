<div align="center">

<img src="docs/known-mascot.svg" alt="Known, the mascot" width="150">

# Known

**Tell Cathay once. Be known everywhere.**

A personal AI voice assistant inside the Cathay Pacific app, for passengers who need assistance.<br>
It remembers what helps, so a family never has to explain again.

**Cathay Hackathon 2026 · Student Track First Runner-up**<br>
Team E497 · All Aboard · Premium Travel

[**Try the live app**](https://known-app-omega.vercel.app) · [Deck (offline HTML)](handouts/E497_Known_presentation.html) · [One-pager (PDF)](handouts/E497_Known_one_pager.pdf) · [5-minute script](handouts/Known%205-minute%20script.md)

</div>

<p align="center"><img src="docs/deck/01.jpg" alt="Known: tell Cathay once, be known everywhere" width="100%"></p>

> This is a showcase of the team's hackathon entry. It holds the deck, the one-pager and the speaker script. The source code stays in the team's private repository.

## Try it on your phone

<table>
<tr>
<td width="230" align="center">
<img src="docs/known-qr.png" alt="QR code for known-app-omega.vercel.app" width="200"><br>
<sub><a href="https://known-app-omega.vercel.app">known-app-omega.vercel.app</a></sub>
</td>
<td>

1. Scan the code. A rebuilt Cathay Pacific app opens, with a trip already booked for tonight.
2. Tap the round **Known** button at the bottom right.
3. Tap the mic bar and talk, or tap one of the shortcuts under the mascot.

Try saying:

- "Mei is autistic and uses a wheelchair. Queues and sudden noise are hard for her."
- "Find a quiet toilet near our gate."
- "Take us to the Sensory Corner."
- "Have they boarded yet?"

Allow the microphone when the browser asks. Without one, tap the keyboard button and type.

</td>
</tr>
</table>

## The story, in the deck's own screens

On every solution slide the phone on the right plays a real turn: someone talks, Known thinks, picks a skill, shows one card, and answers in one line.

### Meet Mei

Our case is Mei Lau. She is eight, she is autistic and she uses a wheelchair: one need you can see, and one you cannot. She is flying from Hong Kong with her mum and dad.

<p align="center"><img src="docs/deck/02.jpg" alt="Case study: Mei Lau, aged 8" width="80%"></p>

### 1. Booking

| Today | With Known |
|---|---|
| <img src="docs/deck/03.jpg" alt="Problem: to get help, Mei's parent or guardian has to phone Cathay"> | <img src="docs/deck/05.jpg" alt="Solution: a parent or guardian says it once, in their own words"> |
| The app tells a parent or guardian to call seven days before the flight, and has no option for autism. Mum waits on hold and explains her daughter, again. | **Listen and plan.** Mum says it once, in her own words. Known hears three needs and turns them into tasks with the codes staff already use. |

Known is one assistant with seven skills and one memory, and the family stays in charge of that memory. They see every line in their own words, can change or forget any of it, and staff see only the brief card the family approves. Known keeps what helps, never the diagnosis.

<p align="center">
<img src="docs/deck/04.jpg" alt="Meet Known: you say it once, it does the rest" width="49%">
<img src="docs/deck/06.jpg" alt="What I remember: the family sees and controls everything Known keeps" width="49%">
</p>

### 2. Wheelchair help

| Today | With Known |
|---|---|
| <img src="docs/deck/07.jpg" alt="Problem: families do not know where or when wheelchair help will arrive"> | <img src="docs/deck/08.jpg" alt="Solution: Known arranges help with a place and a time"> |
| Families often do not know where or when their wheelchair help will arrive. | **Arrange help.** Known books it and gives a place, a time and a name. Ground staff get one brief card, so help is there when Mei arrives. |

### 3. Calm places

| Today | With Known |
|---|---|
| <img src="docs/deck/09.jpg" alt="Problem: a crowded concourse, and no map shows where it is loud"> | <img src="docs/deck/10.jpg" alt="Solution: Known reads the terminal zone by zone"> |
| A terminal changes by the minute. A gate starts boarding, a café fills up, and no map shows a family where it is loud. | Known reads the terminal zone by zone: flight times first, then people counters, Wi-Fi counts and sound meters. Counts and levels only. No faces, no recordings. |

<p align="center">
<img src="docs/deck/11.jpg" alt="Calm places: the quiet toilet, a minute away, on the 3D map" width="49%">
<img src="docs/deck/12.jpg" alt="Calm route: the quiet, step-free way to the Sensory Corner" width="49%">
</p>

**Calm places** finds the quiet toilet near the gate. **Calm route** takes the family the quiet, step-free way, clear of the queue at Gate 26. Both are drawn on the team's 3D map of Hong Kong airport.

### 4. Gate change

| Today | With Known |
|---|---|
| <img src="docs/deck/13.jpg" alt="Problem: a gate change is a loud announcement"> | <img src="docs/deck/14.jpg" alt="Solution: Known speaks first, with a silent alert and a quiet route"> |
| A gate change is a loud announcement, and sudden noise is one of the hardest things for autistic travellers. | **Gate watch** speaks first, with a silent alert and a new quiet route to Gate 41. Then **Calm mode** shows Mei what happens next, in three pictures. |

### 5. At home

| Today | With Known |
|---|---|
| <img src="docs/deck/15.jpg" alt="Problem: at home, grandma can only see the flight status"> | <img src="docs/deck/16.jpg" alt="Solution: grandma asks Known whether they have boarded"> |
| Grandma can only see the flight status. She does not know whether Mei has been met. | **Keep family posted.** Grandma asks, "Have they boarded yet?" The same assistant, on her phone, shows the journey so far. |

### What this gives Cathay

One assistant, seven skills, the whole journey. The team proposed one supervised pilot: one station first, thirty to fifty real cases, and a go or no-go within twelve weeks. Each milestone has to earn the next.

<p align="center">
<img src="docs/deck/17.jpg" alt="Impact: one assistant, seven skills, one supervised pilot" width="49%">
<img src="docs/deck/18.jpg" alt="Roadmap: five milestones, each one earning the next" width="49%">
</p>

<p align="center"><img src="docs/deck/19.jpg" alt="Closing slide" width="80%"></p>

## How the demo works

- **App:** the Cathay Pacific screens rebuilt as five working tabs, with Known as a floating button on every one. It is built with Vite and plain JavaScript, with an Express server for the AI calls running as one Vercel function.
- **Voice in:** the browser records 16 kHz audio. One Gemini call writes down what was said, marks the phrases that matter, picks the skill and writes Known's line.
- **Voice out:** Gemini text to speech, with the words on screen keeping time with the voice.
- **Mascot and cards:** GSAP animation on SVG, shared between the deck and the app.
- **Map:** a three.js model of Hong Kong airport with a walking graph of the terminal.

## What is real and what is scripted

The voice, the understanding of what was said, the choice of skill, and the plan and memory cards are real Gemini calls. The other skill cards show the deck's scripted content about Mei, whatever is asked. Nothing is sent to Cathay, and payment and real sign-in are not implemented. The flight, times, gates and names are illustrative.

Known is a hackathon concept. It is not a Cathay Pacific product, and this repository is not affiliated with or endorsed by Cathay Pacific.

## Team E497 · All Aboard

Uh Suh Yeon · Shin Hyunsung · Kang Seungwan · Shin Seung Min · Kim Hyunjun

## What is in this repository

| Path | What it is |
|---|---|
| `docs/deck/` | The 19 deck frames used above |
| `handouts/E497_Known_presentation.html` | The full deck as one offline HTML file; use the right arrow to advance |
| `handouts/E497_Known_one_pager.pdf` | The one-pager |
| `handouts/Known 5-minute script.md` | The speaker script, one block per click |
| `docs/known-mascot.svg`, `docs/known-qr.png` | The mascot, and the QR code for the live app |

The offline deck includes GSAP, used under its [standard license](https://gsap.com/standard-license).
