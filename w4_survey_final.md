# Gallup Wave 4 — Final Survey Items (Returning Respondents)

March 4, 2026

Clean version with all decisions applied. No flags — ready for Qualtrics build.
Display logic in brackets. Age piping: [schoolwork/work] and [school/work].

---

## PARENT SURVEY

### Intro

REPEAT_TEXT. This survey is intended to follow another survey you completed a few months ago. It will help us understand your thoughts about artificial intelligence (AI).

During the survey, you might notice a few questions that look familiar from the last survey, but that's on purpose. We are interested in what's changed since the last time you filled this survey out.

---

### Well-being

**P1.** Please imagine a ladder with steps numbered from zero at the bottom to ten at the top. The top represents the **best possible life** for you and the bottom represents the **worst possible life** for you. On which step of the ladder would you say you personally feel you stood **during the past 30 days**? (P2)
- 0 to 10

---

### AI Screening

[Intro: The next questions are about having conversations with AI chatbots like ChatGPT, Claude, or Snapchat My AI. We don't mean Siri, autocorrect, or Google search AI summary.]

**P2.** Have you **ever** used AI chatbots? (AI_USE_EVER_P)
- Yes
- No

**P3.** [IF AI_USE_EVER_P = Yes] In the **past 30 days**, have you used AI chatbots? (AI_USE_YN_P)
- Yes
- No

---

### AI Use Context Screening [NEW]

[IF AI_USE_EVER_P = Yes]

[Intro: Many people use AI to be more productive or get things done. We want to understand how **you** use AI. Please select **all** of the following that you have used AI for.]

**P4.** Which of the following have you used AI chatbots for? **Select all that apply.** (W4_P_AIUSE_PROD)
- Drafting or editing a professional email
- Preparing for a meeting or presentation
- Summarizing documents, articles, or reports
- Writing a report, proposal, or memo
- Brainstorming ideas for a project
- Analyzing or making sense of data
- Coding or solving technical problems
- Researching a work-related topic
- Learning a new skill for work
- Other work use (please specify): [text box]
- I have **never** used AI for work or anything productive

[Programmer: Create embedded data variable W4_P_AI_PATH based on responses:
- PATH_A = AI_USE_EVER_P = Yes AND selected at least one productive use (not the "never" option)
- PATH_B = AI_USE_EVER_P = Yes AND selected ONLY "I have never used AI for work or anything productive"
- PATH_C = AI_USE_EVER_P = No]

---

### Meaning & Agency [NEW]

[Programmer: Show version (a), (b), or (c) based on W4_P_AI_PATH. Randomize within each subconstruct block.]

Scale for all items: Strongly disagree / Disagree / Slightly disagree / Slightly agree / Agree / Strongly agree

---

#### PATH A — Uses AI for work

[Intro: The next questions are about how, if at all, using AI chatbots has **affected your experience of doing work**.]

#### Process agency
[Randomize P5a–P6a, P18a–P20a]

**P5a.** When I use AI, I feel like I have **less say** in how my work gets done. (W4_P_A1a) [negative]

**P6a.** When I use AI, it feels like **I'm not the one producing** the work. (W4_P_A2a) [negative]

**P18a.** When I use AI, I still feel **in control** of how my work gets done. (W4_P_A8a) [positive rewrite of P5a]

**P19a.** When I use AI, the final product still feels like **it's mine**. (W4_P_A9a) [positive rewrite of P6a]

**P20a.** When I use AI, I feel like the work still reflects **my own thinking and approach**. (W4_P_A10a) [TENTATIVE]

#### Outcome agency
[Randomize P7a–P8a, P21a]

**P7a.** AI helps me achieve work goals I **couldn't reach on my own**. (W4_P_A3a)

**P8a.** AI makes me feel like I can **take on bigger challenges** at work. (W4_P_A4a)

**P21a.** AI helps me produce **higher-quality** work than I could on my own. (W4_P_A11a) [TENTATIVE]

#### Meaning
[Randomize P9a–P11a]

**P9a.** Because of AI, my work feels **less meaningful** than it used to. (W4_P_A5a)

**P10a.** AI does parts of my work that I actually **care about doing myself**. (W4_P_A6a)

**P11a.** I take **less pride** in my work when AI helps with it. (W4_P_A7a)

---

#### PATH B — Uses AI only for personal reasons

[Intro: You mentioned you haven't used AI for work. The next questions are about how, if at all, using AI chatbots has **affected your experience of everyday tasks and personal projects**.]

#### Process agency
[Randomize P5b–P6b, P18b–P20b]

**P5b.** When I use AI, I feel like I have **less control** over how things in my personal life get done. (W4_P_A1b) [negative]

**P6b.** When I use AI for personal tasks, it feels like **I'm not the one doing things myself**. (W4_P_A2b) [negative]

**P18b.** When I use AI, I still feel **in control** of how things in my personal life get done. (W4_P_A8b) [positive rewrite of P5b]

**P19b.** When I use AI for personal tasks, the result still feels like **it's mine**. (W4_P_A9b) [positive rewrite of P6b]

**P20b.** When I use AI, I feel like what I do still reflects **my own thinking and approach**. (W4_P_A10b) [TENTATIVE]

#### Outcome agency
[Randomize P7b–P8b, P21b]

**P7b.** AI helps me accomplish personal goals I **couldn't reach on my own**. (W4_P_A3b)

**P8b.** AI makes me feel like I can **take on bigger challenges** in my personal life. (W4_P_A4b)

**P21b.** AI helps me get **better results** in my personal life than I could on my own. (W4_P_A11b) [TENTATIVE]

#### Meaning
[Randomize P9b–P11b]

**P9b.** Because of AI, things I do in my personal life feel **less meaningful** than they used to. (W4_P_A5b)

**P10b.** AI handles personal tasks that I actually **care about doing myself**. (W4_P_A6b)

**P11b.** I take **less pride** in what I accomplish when AI helps with it. (W4_P_A7b)

---

#### PATH C — Has never used AI

> NOTE FOR ANGELA: Same framing decision as child survey — see note there. Neutral "If I used AI..." chosen over causal "I don't use AI because..."

[Intro: You mentioned you haven't used AI chatbots. We're interested in **what you think using AI would be like**.]

#### Process agency
[Randomize P5c–P6c, P18c–P20c]

**P5c.** If I used AI, I think I would have **less say** in how my work gets done. (W4_P_A1c) [negative]

**P6c.** If I used AI, I think it would feel like **I'm not the one producing** the work. (W4_P_A2c) [negative]

**P18c.** If I used AI, I think I would still feel **in control** of how my work gets done. (W4_P_A8c) [positive rewrite of P5c]

**P19c.** If I used AI, I think the final product would still feel like **it's mine**. (W4_P_A9c) [positive rewrite of P6c]

**P20c.** If I used AI, I think the work would still reflect **my own thinking and approach**. (W4_P_A10c) [TENTATIVE]

#### Outcome agency
[Randomize P7c–P8c, P21c]

**P7c.** If I used AI, I think it could help me achieve work goals I **can't reach on my own**. (W4_P_A3c)

**P8c.** If I used AI, I think I could **take on bigger challenges** at work. (W4_P_A4c)

**P21c.** If I used AI, I think it could help me produce **higher-quality** work than I can on my own. (W4_P_A11c) [TENTATIVE]

#### Meaning
[Randomize P9c–P11c]

**P9c.** If I used AI, I think my work would feel **less meaningful**. (W4_P_A5c)

**P10c.** If I used AI, I think it would do parts of my work that I actually **care about doing myself**. (W4_P_A6c)

**P11c.** If I used AI, I think I would take **less pride** in my work. (W4_P_A7c)

---

#### Dependency [PATH A and PATH B only]

**P12.** [IF PATH_A] If **all AI tools suddenly disappeared**, how well could you do your typical work? (W4_P_D1)
- Much worse than before I started using AI
- Somewhat worse
- About the same
- Somewhat better
- Much better than before I started using AI

**P12b.** [IF PATH_B] If **all AI tools suddenly disappeared**, how well could you handle your typical everyday tasks? (W4_P_D1b)
- Much worse than before I started using AI
- Somewhat worse
- About the same
- Somewhat better
- Much better than before I started using AI

**P13.** [IF PATH_A] Compared to **6 months ago**, my ability to do work **without AI** has... (W4_P_D2)
- Gotten much worse
- Gotten somewhat worse
- Stayed about the same
- Gotten somewhat better
- Gotten much better

**P13b.** [IF PATH_B] Compared to **6 months ago**, my ability to handle everyday tasks **without AI** has... (W4_P_D2b)
- Gotten much worse
- Gotten somewhat worse
- Stayed about the same
- Gotten somewhat better
- Gotten much better

---

#### Identity and motivation

**P14.** How much do you **enjoy** your work? (W4_P_ID1)
- Not at all / A little / Somewhat / Quite a bit / A great deal

**P15.** How important is your work to **who you are as a person**? (W4_P_ID2)
- Not at all important / Slightly important / Moderately important / Very important / Extremely important

**P16.** How much do you **pride yourself** on your work? (W4_P_ID3)
- Not at all / A little / Somewhat / Quite a bit / A great deal

**P17.** How much of your work requires you to **come up with your own ideas or approaches**? (W4_P_CREAT)
- None of it / A little / Some / Most / All of it

---

### Polarization [NEW] [IF parent is age 18–28]

**P18.** Do you think AI chatbots will make **political disagreements** in America better or worse? (W4_POL1_P)
- Much worse
- Somewhat worse
- No effect
- Somewhat better
- Much better
- I don't know

---

## CHILD / GEN Z SURVEY

### A. Well-being & Social

**1.** Please imagine a ladder with steps numbered from zero at the bottom to ten at the top. The top of the ladder represents the **best possible life** for you and the bottom of the ladder represents the **worst possible life** for you. On which step of the ladder would you say you personally feel you stood **during the past 30 days**? (Q1)
- 0 to 10

---

**2.** Please think of a close friend as someone you can talk with about things that are most important to you, including sensitive issues. Overall, about how many **close friends** would you say you have? (Q5)
- 0
- 1
- 2–5
- 6–10
- More than 10

---

### B. AI Screening

[Intro: The next questions are about having conversations with AI chatbots like ChatGPT, Claude, or Snapchat My AI. We don't mean Siri, autocorrect, or Google search AI summary.]

**3.** Have you **ever** used AI chatbots? (AI_USE_EVER)
- Yes
- No

**3a.** [IF AI_USE_EVER = Yes] In the **past 30 days**, have you used AI chatbots? (AI_USE_YN)
- Yes
- No

---

### C. AI Usage Frequency

[IF AI_USE_YN = Yes]

[Intro: As a reminder, the next questions are about having conversations with AI chatbots like ChatGPT, Claude, or Snapchat My AI. We don't mean Siri, autocorrect, or Google search AI summary.]

All items use the same 8-point frequency scale:
- Never
- Once
- Two or three times
- Once a week
- Several times per week
- Once a day
- Several times a day
- Almost constantly

**4.** During the past 30 days, about how often did you **ask an AI chatbot something instead of just Googling it**? (Q6A)

**5.** During the past 30 days, about how often did you use AI chatbots to **create an image or video**? (Q7A)

**6.** During the past 30 days, about how often did you use AI chatbots to **help you with your work**? (Q8A)

**7.** During the past 30 days, about how often did you use AI chatbots to **help you with writing**? (Q9A)

**8.** During the past 30 days, about how often did you use AI chatbots to **help you with math**? (Q10A)

**9.** During the past 30 days, about how often did you use AI chatbots **as if they were a friend**? For example, to talk about your day or just have a personal conversation. (Q11A)

**10.** During the past 30 days, about how often did you use AI chatbots **as if they were a boyfriend/girlfriend**? (Q12A)

**11.** During the past 30 days, about how often did you use AI chatbots to get **advice about something personal** to you, such as advice about relationships or life decisions? (Q13A)

**12.** During the past 30 days, about how often did you use AI chatbots for your work **when you were specifically told not to**? (Q14A)

---

### D. AI Adoption & Payment [NEW]

**13.** [IF AI_USE_EVER = Yes] When did you **first start** using AI chatbots? (W4_ADOPT)
- I don't remember
- Before 2023
- 2023
- 2024
- 2025
- 2026

**14.** [IF AI_USE_EVER = Yes] Do you **pay** for an AI chatbot subscription (e.g., ChatGPT Plus)? (W4_PAID)
- Yes
- No

---

### E. AI Influence on Behavior

[IF AI_USE_YN = Yes]

[Intro: The next questions are about how much, if at all, **AI chatbots have influenced your life** during the past 30 days. By AI chatbots, we mean AI like ChatGPT, Claude, or Snapchat My AI. We don't mean Siri, autocorrect, or Google search AI summary. Please select the response that best describes you.]

[Randomize 15–17]

**15.** Because of AI chatbots, I **talked to my friends** during the past 30 days... (Q15)
- Much less often than I used to
- A little less often than I used to
- The same amount as I used to
- A little more often than I used to
- Much more often than I used to

**16.** Because of AI chatbots, I **used social media** during the past 30 days... (Q16)
- [Same scale as 15]

**17.** Because of AI chatbots, I **used Google search** during the past 30 days... (Q17)
- [Same scale as 15]

---

[Randomize 18–19]

**18.** Because of AI chatbots, during the past 30 days I think I was... (Q18)
- Much less **curious** than I used to be
- A little less curious than I used to be
- Just as curious as I used to be
- A little more curious than I used to be
- Much more curious than I used to be

**19.** Because of AI chatbots, during the past 30 days I think I was... (Q19)
- Much less **lazy** than I used to be
- A little less lazy than I used to be
- Just as lazy as I used to be
- A little more lazy than I used to be
- Much more lazy than I used to be

---

[Randomize 20–21]

**20.** Because of AI chatbots, were you more or less **confident** when you talked to people during the past 30 days? (Q20)
- Much less confident
- A little less confident
- Neither more nor less confident
- A little more confident
- Much more confident

**21.** Because of AI chatbots, were you more or less **interested in talking to people** during the past 30 days? (Q21)
- Much less interested
- A little less interested
- Neither more nor less interested
- A little more interested
- Much more interested

---

### F. Peer AI Use

**22.** How many of your friends interact with AI chatbots **as if they were a friend**? For example, to talk about their day or just have a personal conversation. Please give your best guess. (Q22)
- None
- Some
- About half
- Most
- All

---

### G. AI Use Strategies [NEW]

[IF AI_USE_YN = Yes]

[Intro: The next questions are about **how you use AI chatbots** to get things done — not for advice or personal reasons. People use AI in many different ways. There are no right or wrong answers — we want to know what **you** actually do.]

[Randomize 23–28]

All items use the same 5-point frequency scale:
- Never / Rarely / Sometimes / Often / Always

#### Coach
**23.** Before asking AI for help, I try to **work through the task on my own first**. (W4_S1 — try-first)

**24.** I ask AI **follow-up questions** to make sure I really understand what it told me. (W4_S2 — Socratic engagement)

**25.** Before I use what AI gives me, I **check whether it's correct**. (W4_S3 — critical evaluation)

#### Crutch
**26.** I tend to **use what AI gives me without making changes**. (W4_S4 — passive consumption)

**27.** I use AI to **avoid tasks I find difficult or challenging**. (W4_S5 — difficulty avoidance)

**28.** I find it **hard to get started** on tasks without asking AI first. (W4_S6 — initiation dependency)

> APPENDIX / RESERVE: "When AI suggests something different from what I was thinking, I usually **go with AI's version**." (judgment deferral — cut for length but available if needed)

#### Cut from prior version (rationale in comms.md)
> - ~~I use AI to learn things I'd have trouble learning on my own~~ (learning orientation — motivation not strategy, overlaps with outcome agency)
> - ~~I keep asking AI to revise what it gives me until I get what I want~~ (iterative refinement — ambiguous coach/crutch)
> - ~~I ask AI for feedback on my ideas or writing the way I'd ask a coach or teacher~~ (input-seeking — social desirability, overlaps with Socratic item)

---

### H. AI Use Context Screening [NEW]

[IF AI_USE_EVER = Yes]

[Intro: Many people use AI to be more productive or get things done. We want to understand how **you** use AI. Please select **all** of the following that you have used AI for.]

**29.** Which of the following have you used AI chatbots for? **Select all that apply.** (W4_AIUSE_PROD)
- Drafting or editing a professional email
- Preparing for a meeting or presentation
- Summarizing documents, articles, or reports
- Writing a paper, report, or assignment
- Brainstorming ideas for a project
- Analyzing or making sense of data
- Coding or solving technical problems
- Researching a [school/work]-related topic
- Learning a new skill for [school/work]
- Solving a homework or class assignment [IF age < 18]
- Studying or reviewing material for an exam [IF age < 18]
- Other [school/work] use (please specify): [text box]
- I have **never** used AI for [school/work] or anything productive

[Programmer: Create embedded data variable W4_AI_PATH based on responses:
- PATH_A = AI_USE_EVER = Yes AND selected at least one productive use (not the "never" option)
- PATH_B = AI_USE_EVER = Yes AND selected ONLY "I have never used AI for school/work or anything productive"
- PATH_C = AI_USE_EVER = No]

---

### I. Agency & Meaning [NEW]

[Programmer: Display "schoolwork" if age < 18; "work" if age >= 18. Randomize within each subconstruct block. Show version (a), (b), or (c) based on W4_AI_PATH.]

Scale for all items: Strongly disagree / Disagree / Slightly disagree / Slightly agree / Agree / Strongly agree

---

#### PATH A — Uses AI for [schoolwork/work]

[Intro: The next questions are about how, if at all, using AI chatbots has **affected your experience of doing [schoolwork/work]**.]

#### Process agency
[Randomize 30a–31a, 37a–39a]
> NOTE: 30a–31a are negatively worded; 37a–38a are positive rewrites for directional balance; 39a is a tentative extra item.

**30a.** When I use AI, I feel like I have **less say** in how my [schoolwork/work] gets done. (W4_A1a) [negative]

**31a.** When I use AI, it feels like **I'm not the one producing** the [schoolwork/work]. (W4_A2a) [negative]

**37a.** When I use AI, I still feel **in control** of how my [schoolwork/work] gets done. (W4_A8a) [positive rewrite of 30a]

**38a.** When I use AI, the final product still feels like **it's mine**. (W4_A9a) [positive rewrite of 31a]

**39a.** When I use AI, I feel like the work still reflects **my own thinking and approach**. (W4_A10a) [TENTATIVE]

#### Outcome agency
[Randomize 32a–33a, 40a]

**32a.** AI helps me achieve [school/work] goals I **couldn't reach on my own**. (W4_A3a)

**33a.** AI makes me feel like I can **take on bigger challenges** at [school/work]. (W4_A4a)
> NOTE: Not in the original outcome agency scale. Added for W4.

**40a.** AI helps me produce **higher-quality** [schoolwork/work] than I could on my own. (W4_A11a) [TENTATIVE]

#### Meaning
[Randomize 34a–36a]

**34a.** Because of AI, my [schoolwork/work] feels **less meaningful** than it used to. (W4_A5a)

**35a.** AI does parts of my [schoolwork/work] that I actually **care about doing myself**. (W4_A6a)

**36a.** I take **less pride** in my [schoolwork/work] when AI helps with it. (W4_A7a)

---

#### PATH B — Uses AI only for personal reasons

[Intro: You mentioned you haven't used AI for [schoolwork/work]. The next questions are about how, if at all, using AI chatbots has **affected your experience of everyday tasks and personal projects**.]

#### Process agency
[Randomize 30b–31b, 37b–39b]

**30b.** When I use AI, I feel like I have **less control** over how things in my personal life get done. (W4_A1b) [negative]

**31b.** When I use AI for personal tasks, it feels like **I'm not the one doing things myself**. (W4_A2b) [negative]

**37b.** When I use AI, I still feel **in control** of how things in my personal life get done. (W4_A8b) [positive rewrite of 30b]

**38b.** When I use AI for personal tasks, the result still feels like **it's mine**. (W4_A9b) [positive rewrite of 31b]

**39b.** When I use AI, I feel like what I do still reflects **my own thinking and approach**. (W4_A10b) [TENTATIVE]

#### Outcome agency
[Randomize 32b–33b, 40b]

**32b.** AI helps me accomplish personal goals I **couldn't reach on my own**. (W4_A3b)

**33b.** AI makes me feel like I can **take on bigger challenges** in my personal life. (W4_A4b)

**40b.** AI helps me get **better results** in my personal life than I could on my own. (W4_A11b) [TENTATIVE]

#### Meaning
[Randomize 34b–36b]

**34b.** Because of AI, things I do in my personal life feel **less meaningful** than they used to. (W4_A5b)

**35b.** AI handles personal tasks that I actually **care about doing myself**. (W4_A6b)

**36b.** I take **less pride** in what I accomplish when AI helps with it. (W4_A7b)

---

#### PATH C — Has never used AI

> NOTE FOR ANGELA: We chose neutral/hypothetical framing ("If I used AI, I think...") over causal framing ("I don't use AI because..."). Rationale: causal conflates beliefs about AI with reasons for non-use — someone might not use AI due to access, inertia, or workplace policy, not because they hold strong beliefs about meaning. Neutral isolates the belief cleanly and lets us correlate beliefs with reasons for non-use separately. Tradeoff: neutral may produce more midpoint responses since it's more detached; causal forces engagement but at the cost of validity.

[Intro: You mentioned you haven't used AI chatbots. We're interested in **what you think using AI would be like**.]

#### Process agency
[Randomize 30c–31c, 37c–39c]

**30c.** If I used AI, I think I would have **less say** in how my [schoolwork/work] gets done. (W4_A1c) [negative]

**31c.** If I used AI, I think it would feel like **I'm not the one producing** the [schoolwork/work]. (W4_A2c) [negative]

**37c.** If I used AI, I think I would still feel **in control** of how my [schoolwork/work] gets done. (W4_A8c) [positive rewrite of 30c]

**38c.** If I used AI, I think the final product would still feel like **it's mine**. (W4_A9c) [positive rewrite of 31c]

**39c.** If I used AI, I think the work would still reflect **my own thinking and approach**. (W4_A10c) [TENTATIVE]

#### Outcome agency
[Randomize 32c–33c, 40c]

**32c.** If I used AI, I think it could help me achieve [school/work] goals I **can't reach on my own**. (W4_A3c)

**33c.** If I used AI, I think I could **take on bigger challenges** at [school/work]. (W4_A4c)

**40c.** If I used AI, I think it could help me produce **higher-quality** [schoolwork/work] than I can on my own. (W4_A11c) [TENTATIVE]

#### Meaning
[Randomize 34c–36c]

**34c.** If I used AI, I think my [schoolwork/work] would feel **less meaningful**. (W4_A5c)

**35c.** If I used AI, I think it would do parts of my [schoolwork/work] that I actually **care about doing myself**. (W4_A6c)

**36c.** If I used AI, I think I would take **less pride** in my [schoolwork/work]. (W4_A7c)

---

#### Dependency/self-efficacy [PATH A and PATH B only]

**42a.** [IF PATH_A] If **all AI tools suddenly disappeared**, how well could you do your typical [schoolwork/work]? (W4_D1)
- Much worse than before I started using AI
- Somewhat worse
- About the same
- Somewhat better
- Much better than before I started using AI

**42b.** [IF PATH_B] If **all AI tools suddenly disappeared**, how well could you handle your typical everyday tasks? (W4_D1b)
- Much worse than before I started using AI
- Somewhat worse
- About the same
- Somewhat better
- Much better than before I started using AI

**43a.** [IF PATH_A] Compared to **6 months ago**, my ability to do [schoolwork/work] **without AI** has... (W4_D2)
- Gotten much worse
- Gotten somewhat worse
- Stayed about the same
- Gotten somewhat better
- Gotten much better

**43b.** [IF PATH_B] Compared to **6 months ago**, my ability to handle everyday tasks **without AI** has... (W4_D2b)
- Gotten much worse
- Gotten somewhat worse
- Stayed about the same
- Gotten somewhat better
- Gotten much better

---

### J. Identity & Motivation [NEW]

**44.** How much do you **enjoy** [schoolwork/work]? (W4_ID1)
- Not at all / A little / Somewhat / Quite a bit / A great deal

**45.** How important is your [schoolwork/work] to **who you are as a person**? (W4_ID2)
- Not at all important / Slightly important / Moderately important / Very important / Extremely important

**46.** How much do you **pride yourself** on your [schoolwork/work]? (W4_ID3)
- Not at all / A little / Somewhat / Quite a bit / A great deal

---

### K. Creativity [NEW] [IF age 18–28 only]

**47.** How much of your work requires you to **come up with your own ideas or approaches**? (W4_CREAT)
- None of it / A little / Some / Most / All of it

---

### L. Social Anxiety

[Intro: For these next three statements, please select the answer that best describes how each situation **makes you feel**.]
[Randomize 48–50]

**48.** **Going to a party** makes me feel... (Q33)
- Very nervous
- Somewhat nervous
- Neither nervous nor relaxed
- Somewhat relaxed
- Very relaxed

**49.** **Being the center of attention** makes me feel... (Q34)
- [Same scale as 48]

**50.** **Talking with people I don't know very well** makes me feel... (Q35)
- [Same scale as 48]

---

### M. Loneliness

[Randomize 51–53]

**51.** During the past 30 days, how **lonely** did you feel? (Q39)
- Not at all lonely
- Slightly lonely
- Moderately lonely
- Very lonely
- Extremely lonely

**52.** During the past 30 days, how often did you feel like you **didn't have any friends**? (Q40)
- Never / Rarely / Sometimes / Often / Always

**53.** During the past 30 days, how often did you feel **left out**? (Q41)
- Never / Rarely / Sometimes / Often / Always

---

### N. Pavani Item [NEW — IF age < 18]

**54.** Which do you think would be more valuable for students your age: AI tools that give individual students personalized help, or AI tools that help students work together? (W4_PAV1)
- AI tools that give individual students personalized help
- AI tools that help students work together
- Both would be equally valuable
- Neither would be valuable

---

### O. Polarization [NEW — IF age 18–28]

**55.** Do you think AI chatbots will make **political disagreements** in America better or worse? (W4_POL1)
- Much worse
- Somewhat worse
- No effect
- Somewhat better
- Much better
- I don't know

---

### P. Policy & Life Events [NEW]

**56.** Does your school or employer have a **policy** about AI chatbot use? (W4_POL_INST)
- They **ban** AI use
- They **discourage** AI use
- They don't have a policy
- They **encourage** AI use
- They **require** AI use

**57.** [IF 56 != "They don't have a policy"] In the last 12 months, has this **policy changed**? (W4_POL_CHG)
- No
- Yes

**57a.** [IF 57 = Yes] Approximately **when** did the policy change? (e.g., June 2025) (W4_POL_CHG_DATE)
- [Short text box]

**57b.** [IF 57 = Yes] Briefly, **what changed**? (W4_POL_CHG_DESC)
- [Short text box]

---

**58.** In the last 12 months, have you experienced a **breakup**? (W4_LIFE1)
- No
- Yes

**58a.** [IF 58 = Yes] Please provide the approximate date (e.g., June 2025): (W4_LIFE1_DATE)
- [Short text box]

**59.** In the last 12 months, have you **relocated** to a new city or neighborhood? (W4_LIFE2)
- No
- Yes

**59a.** [IF 59 = Yes] Please provide the approximate date (e.g., June 2025): (W4_LIFE2_DATE)
- [Short text box]

---

### Q. Invitation [NEW]

**60.** We're developing an **AI coach to help people become better writers**. This app is not yet open to the public. Would you be interested in trying it? (W4_INVITE)
*Note: This is a real invitation. If you say yes, we'll reach out with instructions — there's no cost or obligation.*
- Yes, I'd like to try the AI writing coach
- No thanks, I'm not interested right now

---

### R. Demographics

**61.** What is your **total annual household income**, before taxes? (D1_GENZ)
- Less than $12,000
- $12,000 to $23,999
- $24,000 to $35,999
- $36,000 to $47,999
- $48,000 to $59,999
- $60,000 to $89,999
- $90,000 to $119,999
- $120,000 to $179,999
- $180,000 to $239,999
- $240,000 and over

**62.** Which of the following best describes your own feelings about your **household's income** these days? (D2)
- Living very well on present income
- Living comfortably on present income
- Getting by on present income
- Finding it difficult on present income

**63.** Are you currently **enrolled in higher education**? (ENROLL)
- Yes
- No

**64.** [IF ENROLL = Yes] Which of the following are you currently enrolled in? **Select all that apply.** (ENROLL_LEVEL)
- Associate degree program
- Bachelor's degree program
- Graduate degree program
- Certificate from a college program
- Certification from an industry program
- Other educational program (please specify): [text box]

**65.** What is the **highest level of school** you have completed or the highest degree you have received? (EDU)
- Less than a high school diploma
- High school graduate (diploma or GED)
- Technical, trade, vocational, or business school after high school
- Some college but no degree
- Two-year associate degree
- Four-year bachelor's degree
- Some postgraduate schooling, no degree
- Postgraduate or professional degree (MA, MS, PhD, MD, JD)

---

### [Qualtrics pilot only]

**66.** How **old** are you? (DEMO_AGE)
- [Dropdown: 18–100]

**67.** What is your **gender**? (DEMO_GENDER)
- Male
- Female
- Non-binary
- Prefer to self-describe: [text box]
- Prefer not to say

**68.** Which of the following best describes your **race or ethnicity**? Select all that apply. (DEMO_RACE)
- White
- Black or African American
- Hispanic or Latino/a
- Asian
- American Indian or Alaska Native
- Native Hawaiian or Pacific Islander
- Other (please specify): [text box]

---

# ITEM COUNT SUMMARY

| Section | Items | Scale |
|---------|-------|-------|
| **Parent survey** | P1–P18 (screening + 3-path agency/meaning + deps + identity) | Mixed |
| **Child/GenZ: Well-being & Social** | 1–2 | Ladder + categorical |
| **AI Screening** | 3, 3a | Ever + past 30 days |
| **AI Usage Frequency** | 4–12 (9 items) | 8-point frequency |
| **Adoption & Payment** | 13–14 | Categorical + Y/N |
| **AI Influence on Behavior** | 15–21 (7 items) | 5-point comparative |
| **Peer AI Use** | 22 | 5-point categorical |
| **AI Use Strategies [NEW]** | 23–28 (6 items: 3 coach + 3 crutch) | 5-point frequency |
| **AI Use Context Screening [NEW]** | 29 (1 checklist) | Select all |
| **Agency & Meaning [NEW]** | 30–41 a/b/c (process neg/pos, outcome, meaning) | 6-point agreement |
| **Dependency [NEW]** | 42–43 a/b variants (2 items) | 5-point comparative |
| **Identity & Motivation [NEW]** | 44–46 (3 items) | 5-point |
| **Creativity [NEW]** | 47 (1 item, 18+ only) | 5-point |
| **Social Anxiety** | 48–50 (3 items) | 5-point |
| **Loneliness** | 51–53 (3 items) | 5-point |
| **Pavani [NEW]** | 54 (1 item, <18 only) | 4-option |
| **Polarization [NEW]** | 55 (1 item, 18+ only) | 5-point |
| **Policy & Life Events [NEW]** | 56–59 + sub-items | Mixed |
| **Invitation [NEW]** | 60 | Y/N |
| **Demographics** | 61–65 | Mixed |
| **Pilot demos** | 66–68 | Mixed |
| **TOTAL (child/GenZ)** | ~68 items (each respondent sees one agency path) | — |
