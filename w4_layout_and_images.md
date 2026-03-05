# Gallup Wave 4 — Page Layout & Icons

March 4, 2026

Each page = one screen in Qualtrics. All Likert items displayed **horizontally** (not matrix). Icon at top of each page, small (~80x80px). Icons sourced from Flaticon (see `images.md` for attribution).

**Icon key:**
- Clipboard = intro/logistics
- Single person = about you personally
- 3 people = social/friends
- Chat bubble = AI conversations
- Robot = AI-specific
- Person at laptop = work/strategies with AI
- Briefcase = work context (18+) / Book = school context (<18) [NOTE TO EMILIO: swap briefcase for book on pages marked * for under-18 respondents]
- Globe = AI and society
- Heart = life events

Icons can repeat across similar pages. Keep it simple.

---

## PARENT SURVEY PAGES

### Parent Page 1 — Intro
- REPEAT_TEXT (intro paragraph)
- **Icon:** Clipboard

### Parent Page 2 — Well-being Ladder
- P1 (ladder 0–10)
- **Icon:** Single person

### Parent Page 3 — AI Screening
- AI intro text + P2 (used AI Y/N)
- **Icon:** Chat bubble

### Parent Page 4 — AI & Work Meaning
- P3 (meaningful slider)
- **Icon:** Person at laptop

### Parent Page 5 — Agency & Meaning
- P4–P10 (process agency, outcome agency, meaning — all 6-point agree/disagree, horizontal)
- **Icon:** Person at laptop

### Parent Page 6 — Dependency
- P11 (AI disappeared) + P12 (compared to 6 months ago)
- **Icon:** Briefcase

### Parent Page 7 — Identity & Motivation
- P13 (enjoy work) + P14 (work identity) + P15 (pride) + P16 (creativity)
- **Icon:** Single person

### Parent Page 8 — Polarization [IF age 18–28]
- P17 (political disagreements)
- **Icon:** Globe

---

## CHILD / GEN Z SURVEY PAGES

### Page 1 — Life Satisfaction
- Item 1 (ladder)
- **Icon:** Single person

### Page 2 — Close Friends
- Item 2 (close friends count)
- **Icon:** 3 people

### Page 3 — AI Screening
- AI intro text + Item 3 (used AI Y/N)
- **Icon:** Chat bubble

### Page 4 — AI Frequency: Productivity
- Items 4–8 (Google replacement, images/video, work, writing, math)
- 5 items, all same scale, horizontal Likert
- **Icon:** Chat bubble

### Page 5 — AI Frequency: Social & Personal
- Items 9–12 (friend, boyfriend/girlfriend, personal advice, forbidden use)
- 4 items, all same scale, horizontal Likert
- **Icon:** Chat bubble

### Page 6 — Adoption & Payment
- Items 13–14 (when started, paid subscription)
- **Icon:** Robot

### Page 7 — AI Influence: Social Behavior
- Intro text + Items 15–17 (friends, social media, Google — randomized)
- 3 items, same scale, horizontal Likert
- **Icon:** Robot

### Page 8 — AI Influence: Curiosity & Laziness
- Items 18–19 (curiosity, laziness — randomized)
- 2 items, horizontal Likert
- **Icon:** Robot

### Page 9 — AI Influence: Confidence & Interest
- Items 20–21 (confidence, interest in talking — randomized)
- 2 items, horizontal Likert
- **Icon:** Robot

### Page 10 — Peer AI Use
- Item 22 (friends using AI as friend)
- **Icon:** 3 people

### Page 11 — AI Strategies
- Intro text (normalizer + "how you use AI") + Items 23–29 (7 strategy items, randomized)
- All same scale (Never–Always), horizontal Likert
- **Icon:** Person at laptop

### Page 12 — Agency: Process & Outcome
- Intro text + Items 30–33 (process agency 2 items + outcome agency 2 items, randomized within blocks)
- 4 items, 6-point agree/disagree, horizontal Likert
- **Icon:** Person at laptop

### Page 13 — Meaning
- Items 34–36 (meaningful, parts I care about, pride — randomized)
- 3 items, 6-point agree/disagree, horizontal Likert
- **Icon:** Person at laptop

### Page 14 — Dependency
- Items 37–38 (AI disappeared, skill trajectory)
- 2 items, different scales — each displayed individually with horizontal options
- **Icon:** Briefcase *

### Page 15 — Identity & Motivation
- Items 39–41 (enjoy work, identity, pride) + Item 42 [IF 18+] (creativity)
- 3–4 items, horizontal Likert
- **Icon:** Single person

### Page 16 — Social Anxiety
- Intro text + Items 43–45 (party, center of attention, strangers — randomized)
- 3 items, same scale, horizontal Likert
- **Icon:** 3 people

### Page 17 — Loneliness
- Items 46–48 (lonely, no friends, left out — randomized)
- 3 items, horizontal Likert
- **Icon:** Single person

### Page 18 — Pavani [IF age < 18] / Polarization [IF age 18–28]
- Item 49 (Pavani, for minors) OR Item 50 (polarization, for adults)
- One item per respondent based on age
- **Icon (Pavani):** Book
- **Icon (Polarization):** Globe

### Page 19 — Policy
- Items 51–52b (AI policy, policy change, date, description)
- **Icon:** Briefcase *

### Page 20 — Life Events
- Items 53–54a (breakup, relocation + dates)
- **Icon:** Heart

### Page 21 — Invitation
- Item 55 (writing coach invitation)
- **Icon:** Robot

### Page 22 — Demographics
- Items 56–60 (income, income feelings, enrollment, enrollment level, education)
- **Icon:** Clipboard

### Page 23 — Pilot Demographics [pilot only]
- Items 61–63 (age, gender, race/ethnicity)
- **Icon:** Clipboard

---

# PAGE COUNT SUMMARY

| Survey | Pages | Approx. time |
|--------|-------|-------------|
| Parent | 8 pages | ~4 min |
| Child/GenZ | 23 pages | ~12 min |

# DESIGN NOTES

1. **Likert display**: All Likert items horizontal, NOT matrix. One question per row, options spread left-to-right.
2. **Icons**: Small (~80x80px) at top-left of each page. All from same Flaticon set for visual consistency. See `images.md` for downloads and attribution.
4. **Mobile-friendly**: Horizontal Likert stacks vertically on mobile (Qualtrics handles automatically).
5. **Randomization**: Applied within pages as noted (not across pages).
6. **Age-conditional icons**: Pages marked * use Briefcase for 18+ and Book for <18. Note to Emilio in survey.
