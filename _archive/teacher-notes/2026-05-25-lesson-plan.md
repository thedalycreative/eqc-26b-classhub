# Lesson Plan — Mon 25 May 2026

**Class 17 · Week 9 · S2 Step 1 · Intake 26B**
**Topic:** From Wireframe to Working Code — Prototype & Begin Website
**Deck:** `26b-lesson-plan-25may2026.html`

---

## Learning Outcomes

By end of class, students will be able to:

1. Translate a wireframe section into semantic HTML structure.
2. Identify which HTML5 element matches a wireframe region (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).
3. Apply minimal CSS to roughly match wireframe layout (background, padding, basic flex).
4. Save → refresh → confirm changes in a browser independently.
5. Have a live, working `index.html` for their original website project.

---

## Materials Needed

- Projector + your laptop for the deck and live demo
- VS Code open with a clean starter folder (`index.html`, `styles.css`)
- One student wireframe (or your own demo wireframe) projected alongside the editor
- Class Hub tab open: cheat sheets folder, `how-to-organise.html`
- QR code image `26b.png` in the same folder as the deck
- (Optional) Bin Chicken Bistro zip on hand as a "what good looks like" reference

---

## Timing (105 min)

| Time | Block | What's happening |
|------|-------|------------------|
| 0:00 – 0:10 | **Settle + Attendance** | Deck Slide 1 (QR). Quick recap: "On Wednesday we wireframed. Today we code." |
| 0:10 – 0:15 | **Schedule + Today** | Deck Slides 2 & 3. Set expectations: this is a build day, not a lecture. |
| 0:15 – 0:20 | **The Big Idea** | Deck Slide 4 (Bridge). Walk the wireframe→tag mapping. Land the line: *"Every rectangle has a tag."* |
| 0:20 – 0:40 | **Live Demo** | Deck Slide 5. Mirror your editor + a wireframe. Build ONE section (header) in front of them. Talk out loud. Make a typo on purpose, show how to find it. |
| 0:40 – 1:40 | **Build Time** | Deck Slide 6. Students code. Circulate at 30 min and 50 min marks. |
| 1:40 – 1:55 | **Show & Tell** | Deck Slide 7. 30 seconds per student — flip their screen, point at the wireframe, point at the page. |
| 1:55 – 2:00 | **Wrap** | What to bring Wednesday. Anyone stuck → hub for help. |

> **Buffer:** if demo runs long, cut Show & Tell down to 5 students max. The build time is the most valuable block — protect it.

---

## The Activity — Wireframe → Code Translation

**Format:** Individual build, guided.
**Length:** 60 min build + 15 min demo round.
**Output:** A working `index.html` with at least ONE section rendered.

### Student steps (also on Slide 6)

1. Open your wireframe and your project folder in VS Code side-by-side.
2. Pick ONE section to start with. **Recommend the header** — it's the fastest win.
3. Write the HTML skeleton first. Semantic tags only. No styles.
4. Save. Open in browser. Confirm something shows up.
5. Add basic CSS to roughly match the wireframe — background, padding, layout.
6. Repeat for the next section.

### Rules of play

- HTML first, CSS second.
- Save + refresh every 2 minutes.
- Don't AI-generate yet — type it. Muscle memory matters this week.
- Ugly is fine. Working > pretty.
- Ask your neighbour before asking Tim.

---

## Live Demo Plan

**Pick ONE student's wireframe to demo with (ask permission first)**, OR use the Bin Chicken Bistro example.

Demo arc (~20 min, must stay tight):

1. **Point at the wireframe.** Out loud: "What is this rectangle?" → name it.
2. **Type the tag.** Just the opening + closing. Save. Refresh. Show it's empty.
3. **Add content.** Logo text, nav links. Save. Refresh.
4. **Make it look right.** ~5 lines of CSS — background, padding, `display: flex`.
5. **Make a deliberate mistake** (forget a closing tag). Show students how the browser reacts. Find it, fix it.

> The goal isn't to finish a section. The goal is for them to **see the rhythm**: type → save → refresh → adjust.

---

## Circulation Cues (during build time)

When you walk around, watch for:

| Sign | What to do |
|------|------------|
| Blank file after 10 min | Sit with them. Get one tag typed. Leave. |
| All `<div>` tags | "Which one of these is your header?" Don't fix — ask. |
| Working on colours before structure | "Is the structure done?" Redirect to HTML first. |
| Stuck on CSS | Open dev tools (F12) together. Inspect the element. |
| Way ahead — second section already done | Push them: "Can you do nav with flexbox?" |

---

## Differentiation

- **Struggling:** Pair them with the Bin Chicken Bistro example. Have them retype the header section to build confidence.
- **On pace:** Standard activity flow.
- **Ahead:** Challenge — make the header **responsive** with a media query, or add hover states to the nav links.
- **Way behind from earlier weeks:** Use the `how-to-organise.html` and starter template; their goal today is just a visible page, not a section.

---

## Success Criteria (for marking / self-check)

A student has "succeeded" today if:

- [ ] `index.html` opens in a browser without error
- [ ] At least one full section from their wireframe is visible
- [ ] Tags used are **semantic** (header / main / section / footer) — not all divs
- [ ] CSS is in `styles.css`, linked from `<head>`
- [ ] They can point at the screen and the wireframe and explain the match

---

## Teacher Notes / Things to Watch

- The wireframe→code leap is the moment students often go quiet. Don't let silence = stuck. Walk over at 10 min if no typing.
- **Don't fix their code.** Ask the question that lets them fix it. ("What does the browser console say?")
- AI temptation will be huge — set the expectation early: today is typing day. AI returns Wednesday.
- Save the last 15 min for show-and-tell — peer pressure is the best motivator and they get to see their classmates' approaches.

---

## Hub Updates After Class

Once class is done, update `index.html`:

- Move Week 8 status from `current open` to `completed`
- Change Week 9 from `upcoming` to `current open`
- Move the `Now` status pill from Week 8 to Week 9
- Update the header progress text: `Week 8 of 12` → `Week 9 of 12`
- Add a `.badge.file` to Class 17 tile pointing to `26b-lesson-plan-25may2026.html`

---

## Homework / Bring Wednesday

- Continue building at home if motivated (optional, not required).
- **Bring:** your wireframe + at least your one-section site working locally.
- Wednesday's class: continue building. AI tools allowed for the FIRST time as a coding aid.
