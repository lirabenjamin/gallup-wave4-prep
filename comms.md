# Comms — Wave 4 Survey Prep

## 2026-03-05 21:30 — Batch of small fixes

Done:
1. **"CLOSE" → "close"** in item 2 (close friends)
2. **"I don't know"** added to both polarization items (P18 and child item 51)
3. **Parent survey now has the same 3-path split** (P3 = ever used AI, P4 = productive use checklist, P5–P11 a/b/c, P12–P13 dependency a/b)
4. **"Have you ever used AI" question added** for both surveys:
   - Parent: P3 (AI_USE_EVER_P) — new standalone item
   - Child: Q3 (AI_USE_EVER) — now Q3 asks "ever", Q3a asks "past 30 days" (conditional on ever=Yes)

This matters because the old Q3 only asked about the past 30 days. Someone who used AI 3 months ago but not recently would have been routed to Path C (never used). Now AI_USE_EVER properly separates "never tried AI" from "tried it but not recently."

**Still open for your review:**

- **Path C wording**: I used "If I used AI, I think I would..." which captures expectations/beliefs. Your original framing was more "I don't use AI because I think it would make my work less meaningful." Current version is more neutral (measures beliefs without implying those are the *reason* for non-use). Want the causal "because" framing instead?
> i think the neutrla is better, can you have a brief chat discussion with me about this to help me think about it?

---

## 2026-03-05 21:00 — Agency/meaning items split into 3 paths

Done. See 21:30 entry above for latest state. Both child and parent surveys now have 3-path routing.

---

## 2026-03-05 19:30 — Full pilot analysis with focused section

Added to `w4_pilot_analysis.html`:
- **Focused analysis**: Coach/crutch descriptives, correlation heatmap with outcomes, 4 regressions (outcome agency, process agency, meaning, dependency), strategy×outcome item-level heatmap
- **Feedback synthesis**: 10 actionable issues ranked by severity (ladder order backwards, work-AI gating needed, no midpoint on agree scale, "lazy" wording, etc.)
- **Composites + alphas**: Coach, crutch, process/outcome agency, meaning, dependency, identity, etc.
- **Scale-level correlations**: Interactive plotly heatmap at composite level

Key finding: Coach and crutch are orthogonal (r=.00). Coach predicts higher outcome agency, lower meaning loss, and lower dependency. Process×outcome agency negatively correlated (r=-.22) — your tradeoff hypothesis holds. Dependency items have almost no variance (M=3.0, SD=0.48).

---

## 2026-03-05 18:00 — Pilot analysis rendered (N=102)

Fixed column mapping bug (Qualtrics exports `Q##` not `QID##`) and rendered `w4_pilot_analysis.html`. Key findings:
- N=102, all finished, median 8.9 min
- **Age concern**: top ages are 34-51, NOT 18-28 Gen Z. Check Prolific age filter?
- See HTML for distributions, correlations, and feedback comments.

---

## 2026-03-05 — Pilot analysis ready to run

`w4_pilot_analysis.qmd` is ready. When data comes in, just ask me to run it:

```
quarto render w4_pilot_analysis.qmd
```

It downloads data from Qualtrics automatically (SV_3OhwvVEN6i6vWqW), recodes all scales to numeric, and produces: sample summary, means/SDs by construct, distributions for every variable, pairwise correlation heatmap, and all pilot feedback comments.

---

## 2026-03-04 — v3 Survey Created + Manual Steps

**Survey v3:** SV_3OhwvVEN6i6vWqW
**URL:** https://upenn.qualtrics.com/jfe/form/SV_3OhwvVEN6i6vWqW

### Manual steps needed:

1. **Prolific redirect URL** — Add end-of-survey redirect to: `https://app.prolific.com/submissions/complete?cc=C4C2GBFP`
   - In Qualtrics: Survey Options → Survey Termination → Redirect to URL → paste the URL above

2. **Icons** — Qualtrics WAF blocks external image URLs in question text, so icons couldn't be added via API. Add them manually in the Qualtrics editor using images from `img/` folder. See `w4_layout_and_images.md` for which icon goes on each page. Each page has an HTML comment `<!-- ICON: filename.png -->` marking where the icon should go.

---

## 2026-03-04 16:00 — Responses to your edits & open discussion items

### 1. Socratic item (36) — rework suggestion

Angela's right that models explain by default now. The item as written ("I ask AI to explain its reasoning, not just give me the answer") doesn't differentiate coach users because EVERYONE gets explanations whether they asked or not. The real Socratic behavior isn't *receiving* explanations — it's *pushing back* and *testing understanding*. Here are three alternatives:

- **A.** "When AI gives me an answer, I try to understand WHY it's correct before using it." (tests comprehension, not just receipt)
- **B.** "I ask AI follow-up questions to make sure I really understand what it told me." (probing behavior)
- **C.** "I sometimes challenge what AI tells me to see if it holds up." (critical engagement / pushback)

I'd go with **B** — it's clearly behavioral ("I ask follow-up questions"), works with the frequency scale, isn't double-barreled, and captures the core Socratic behavior of not accepting at face value. It's also distinct from item 39 (checking correctness) because 39 is about verification and B is about deepening understanding.
> agree like this one

### 2. Social desirability concern

Yes, this is a real worry for the strategy items. The "coach" items (try first, check correctness, ask follow-ups) are clearly the "right" answers. A few mitigations:

- The frequency scale helps — "Sometimes" is an easy, non-judgmental middle option. Agree/disagree would be worse (who disagrees with "I check if AI is correct"?).
- The two reverse-coded items (35: use without changes; 37 if kept: use without reading) provide a cross-check. People who say "Always" on coach items but "Never" on crutch items are probably inflating.
- You could add an intro normalizer: *"People use AI in many different ways. There are no right or wrong answers — we want to know what YOU actually do."*
> add this

- Ultimately, the real test is whether strategy scores predict outcomes (dependency, agency, meaning). If everyone clusters at the ceiling, the items are uninformative and you'd know.
> yes ill pilot tomorrow and get some sense of hte distros

My honest assessment: you'll get moderate social desirability bias but enough variance to be useful. The frequency scale + reverse items help a lot.

### 3. Polarization wording

I'd go with **"political disagreements"** over "division." Reasons: (1) "disagreements" is concrete and specific — people disagree about stuff; (2) "division" is more loaded/abstract and has become a political talking point itself; (3) for 12-17s, "disagreements" is more intuitive. But it's a close call. Either works if consistent. I'll standardize to "disagreements" in the file unless you say otherwise.
> sure

### 4. Item 49 (dependency) — you're right, I was wrong

Your example is correct. Someone who learned a lot FROM using AI would do better without AI than they did before they ever used it. The "much better" anchor is legitimate and captures AI-as-learning-tool. Withdrawing my flag.
> good!

### 5. Item 35 vs 37 inconsistency

You said "keep the without reading it" in comms but "Keep 35, drop 37" in the items file. These conflict:
- Item 35 = "I tend to use what AI gives me without making changes" (passive use)
- Item 37 = "I use what AI gives me without reading it from beginning to end" (shallow processing)

Which one do you actually want to keep? Or both? If you want just one crutch item, I'd keep 37 (without reading) — it's a more extreme/distinctive behavior and will have more variance. "Without making changes" is ambiguous (maybe the output was already good).
> i like 35 better

### 6. Items for discussion before I commit changes

These need your input before I touch the file:

- **Agency intro framing**: You raised whether to reference "before AI." My take: the items already contain the comparison ("less meaningful *than it used to*", "*compared to* 6 months ago"). Adding a "how has life changed since AI" framing to the intro would double the temporal comparison and might prime people to report change even if there was none. I'd keep the intro neutral: *"The next questions are about how, if at all, using AI chatbots has affected your experience of [schoolwork/work]."* The comparison lives in the items, not the intro.
> good

- **Item 47 ("AI does the parts I care about")**: You said nobody would disagree with "I wish AI would handle the boring parts." Fair — that companion item is ceiling-bound. But item 47 as written is interesting precisely because it can go either way: some people strongly agree (AI took over what I liked), others strongly disagree (AI only handles the tedious stuff). I'd keep 47 as is with no companion.
> yes

- **Meaning measurement (general vs AI-attributed)**: Should items say "Because of AI, my work feels less meaningful" or just "My work feels meaningful"? Your lean is to keep as-is (AI-attributed). I agree — the general version confounds everything (economy, life stage, mood). The AI-attributed version isolates the AI effect, which is what you need for the agency paper. The cost is that people who don't use AI much might not know how to answer. But you're already gating these items on AI use, so that's handled.
> good

- **Item 38 (learning orientation)**: You suggested "I use AI to learn things that would be hard to learn otherwise" or "I use AI to teach me things that would be hard to learn otherwise." Both work with frequency. I'd go with: **"I use AI to learn things I'd have trouble learning on my own."** It's behavioral ("I use AI to learn"), concrete ("things I'd have trouble learning"), and pairs naturally with Never/Rarely/Sometimes/Often/Always.
> yes i like that one.
---

## 2026-03-04 15:00 — Item review file created

BenBen, I created `w4_items_review.md` with all 95 items numbered sequentially. Every item from the Gallup spec (repeat items) and your new W4 items are included. I flagged 12 items that need decisions — see the summary table at the bottom of the file.

Key decisions you need to make:
1. **Strategy scale**: Never/Rarely/Sometimes/Often/Always (frequency) vs. Strongly disagree–Strongly agree? I recommend frequency for behavioral items.
> frequency

2. **Two passive items (35 vs 37)**: You have "I use what AI gives me without making changes" AND "I use what AI gives me without reading it." These overlap. The Socratic item ("I ask AI to explain its reasoning") got dropped. Keep both passive items, or swap one for the Socratic item?
> keep the without reading it. The explanatoin item i think might be a good one but not in that state. Angela didnt like it, she said, becuase nowadays, models always expalin their behavior. can you think of an improvement? also do you worry that were going to get a lot of social desirability

3. **Polarization wording**: "political division" (child survey) vs. "political disagreements" (parent survey). Pick one.
> What do you think is better, my guess is division?

4. **Breakup/relocation for minors**: Restrict to 15+ or 18+?
> Id keep for eveyrone, kids are early these days.

Answer here or in chat — whatever's easier.

---

## 2026-03-04 — Questions for BenBen

1. The bracketed note "[Things go too fast, i wish they were slower, i feel im in a hamster wheel]" under Meaning — do you want me to turn this into an actual survey item capturing pace/overwhelm? If so, is it about AI specifically (e.g., "AI makes my work move faster than I'd like") or about work in general?
> yes make this an item, maybe two for more stats/better measurement? I think all that section is about how you feel life has changed from the before ai times to today... so not sure how to best structure this. but these are some things i feel and i dont htink im alone on this. it sort of captures this feeling of ai acelerating the pace and making me feel worse. i wish i could take my time, and tend to my work like i tend to a garden.

2. "How much do you think of yourself as a writer?" — do you want to keep this? It's only useful if you're moderating the writing coach invitation uptake. If not, I'd cut it.
> I like the identity quesitons, but we are asking questions about your work, so i dont think it makes sense to ask do you think of yourself as a worker. and we have items that sort of say that my work is part of my identity or something like that.

3. Between the two similar identity items — "How important is your work to your identity?" vs. "How much do you pride yourself on your work?" — which one do you want to keep? I recommend the identity one.
> i want to have 2-3 good meaning items. not sure what are the best ones.

4. Open-ended placement: do you want the open-ended advice question BEFORE the strategy items (unprimed, more naturalistic) or AFTER them (richer, more thoughtful responses)?
> I think before so we dont prime them

5. Coach/crutch self-report: do you want the direct "coach vs. crutch" item at all, or are you satisfied with the behavioral items (18-24) capturing the distinction? If you want it, I suggest the neutral version: "Which better describes how you typically use AI chatbots? [To get things done faster / To learn and improve my skills / About equal]"
> i want both questions, and you can have both, so dont force the dichotomy. i want to ask both quesitons and give poeple some sort of definition for each, ill discuss these w angela in a bit, so i might end up cutting them, but i want to have something to discuss.

6. Item 28 — "AI makes me feel powerful" — are you OK replacing this with "AI makes me feel like I can take on bigger challenges"? Or do you want to keep "powerful"?
> I like the bigger challenges -- add a note that that is not in the original outcome agency scale.

7. Should I move the policy item up near the AI frequency block (more natural flow) or keep it at the end with the life events?
> keep at the end.
