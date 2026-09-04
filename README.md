# Claude Certification Handbook

Verified facts for all four Anthropic Claude certification exams, the eligibility rule that most study guides skip, and how to register when you do not work at a Claude partner company.

We are [YAID (Your AI Department)](https://youraidept.com/network?ref=github), a registered Claude Partner Network firm. Our members sit these exams. The eligibility rule kept surprising the engineers who applied to us, so we wrote it down, along with everything else we had to look up ourselves. Facts were checked on August 28, 2026 against the Pearson VUE program listing and the published exam guides. Where the program has not published a number officially, we say "reported".

**Contents**

- [The four exams at a glance](#the-four-exams-at-a-glance)
- [Which exam should you take?](#which-exam-should-you-take)
- [Who can take the exams](#who-can-take-the-exams)
- [How to register](#how-to-register)
- [Costs](#costs)
- [Retakes and renewal](#retakes-and-renewal)
- [Exam guides](#exam-guides)
- [Free practice exams](#free-practice-exams)
- [How to prepare](#how-to-prepare)
- [FAQ](#faq)
- [Community study resources](#community-study-resources)
- [Sources](#sources)
- [About YAID](#about-yaid)

## The four exams at a glance

| Code | Name | Who it is for | Questions | Time | Passing score | Fee per attempt |
|---|---|---|---|---|---|---|
| [CCAR-F](exams/ccar-f.md) | Claude Certified Architect – Foundations | Engineers and solution architects who design Claude-powered systems | 60 | 120 min | 720 / 1,000 | $125 (exam guide) |
| [CCDV-F](exams/ccdv-f.md) | Claude Certified Developer – Foundations | Developers who build applications on Claude | 53 | 120 min | 720 / 1,000 | $125 (exam guide v1.0) |
| [CCAO-F](exams/ccao-f.md) | Claude Certified Associate – Foundations | Non-developers who use Claude in daily work | 60 | 120 min | 720 / 1,000 | $99 (reported) |
| [CCAR-P](exams/ccar-p.md) | Claude Certified Architect – Professional | Senior and principal architects | 63 | 120 min | 720 / 1,000 | $175 (reported) |

Every exam in the program is delivered by Pearson VUE, online proctored or at a test center, and is closed-book with no AI assistance allowed. Scoring is on a 100 to 1,000 scale with 720 to pass. You get up to 4 attempts per rolling 12 months, with waits of 14, 30, then 90 days between them, and a pass is valid for 12 months with a free on-time renewal assessment.

The same facts are available as JSON in [`data/exams.json`](data/exams.json).

## Which exam should you take?

If you design systems on Claude, sell or lead implementation work, or want the credential clients ask about by name, sit CCAR-F. People shorten it to CCA-F; same exam.

If you spend your days writing application code against the Claude API and have shipped something real, CCDV-F fits better. A third of its marks are applications and integration.

CCAO-F is for people who use Claude at work without writing code: operations, marketing, project management, analysis, teaching. It is the only exam in the program with no engineering assumed.

CCAR-P is the professional tier for senior and principal architects who own Claude systems end to end, governance and executive conversations included. Nothing forces you to pass CCAR-F first, though it builds directly on that blueprint and most people sit it first.

## Who can take the exams

Pearson VUE's program page states the rule in one sentence: "Certification is open to organizations in the Claude Partner Network and counts toward partner program standing."

Individuals do not enroll directly. Registration happens inside the Anthropic Partner Academy, and Partner Academy access comes through a Claude Partner Network organization. If you are independent, there are three ways in.

1. Your employer joins the Claude Partner Network. This works when you have an employer bringing Claude to market who is willing to apply, onboard, and keep up partner standing.
2. Your own company applies. If you operate a company that brings Claude to market, you can [apply directly](https://claude.com/form/cpn-partner-application). You then carry the application, the program requirements, and the ongoing partner relationship yourself.
3. You join an existing partner firm. YAID is a registered Claude Partner Network company. Approved members become exam-eligible under YAID's partner standing without running a partner entity of their own, and can run client work on the firm's contracts and insurance.

Whichever route you take, the credential is yours personally. It stays with you if you change employers or leave the partner firm later.

## How to register

The short version of the third route:

1. Apply to a partner firm. Approval puts you on the member roster of a registered Claude Partner Network company, which is what makes you exam-eligible.
2. Get your firm credentials. YAID members receive a YAID email address and registration access through the Anthropic Partner Academy.
3. Prepare. The Partner Academy has a self-paced prep course for each exam, and each exam guide lists the domains and weights.
4. Schedule with Pearson VUE, online proctored or at a test center, and sit the exam. You can reschedule up to 24 hours before the appointment.
5. Pass. The certification is yours.

The long version, including what exam day looks like and how renewal works, is in [registration.md](registration.md). It also answers the question in every form we have heard it asked: how to register, how to take the exam, how to sign up, where to book, whether freelancers can sit it, and so on.

## Costs

There are two fees and people mix them up.

The exam fee goes to the certification program per attempt. It is $125 for CCAR-F and CCDV-F as of the mid-2026 exam guides, up from $99 during early access. CCAO-F is reported at $99 and CCAR-P at $175; neither has appeared on an official public page yet, so confirm at registration.

The membership fee is what a partner firm charges if you get eligibility through one. YAID membership is $149 per quarter, which covers partner-network eligibility plus the firm infrastructure around client work. It does not include the exam fee and it does not guarantee a pass.

Program pricing has already changed once. Check the current exam guide before you schedule.

## Retakes and renewal

Up to 4 attempts per exam in any rolling 12-month period, with waiting periods of 14 days after the first attempt, 30 days after the second, and 90 days after the third. Each attempt costs the exam fee.

A pass is valid for 12 months. Renewal is a free, non-proctored assessment on the Anthropic Partner Academy, as long as you complete it on time.

## Exam guides

One file per exam: quick facts, domain weights, what each domain covers, prep notes, common mistakes, a study path, and an FAQ.

- [CCAR-F: Claude Certified Architect – Foundations](exams/ccar-f.md)
- [CCDV-F: Claude Certified Developer – Foundations](exams/ccdv-f.md)
- [CCAO-F: Claude Certified Associate – Foundations](exams/ccao-f.md)
- [CCAR-P: Claude Certified Architect – Professional](exams/ccar-p.md)

## Free practice exams

We run free timed practice exams for all four certifications at [youraidept.com/network/claude-certification-practice-exam](https://youraidept.com/network/claude-certification-practice-exam): full-length mocks drawn to the published domain weights (60 questions in 120 minutes for CCAR-F and CCAO-F, 53 for CCDV-F), a countdown, an estimated score on the 100 to 1,000 scale against the 720 pass mark, a per-domain breakdown, and explanations for every question. 250 original questions, no sign-up, results stay in your browser. Per exam: [CCAR-F](https://youraidept.com/network/ccar-f-practice-exam), [CCDV-F](https://youraidept.com/network/ccdv-f-practice-exam), [CCAO-F](https://youraidept.com/network/ccao-f-practice-exam), [CCAR-P](https://youraidept.com/network/ccar-p-practice-exam).

## How to prepare

- Each exam guide publishes domains and weights. Weight your prep the same way. On CCAR-F, agentic architecture alone is 27% of the marks.
- The room is closed-book, with no AI assistance and no documentation. Anything you normally look up has to be in your head.
- The Partner Academy prep course for each exam follows that exam's blueprint. Anthropic also publishes free public courses through [Anthropic Academy](https://anthropic.skilljar.com/).
- People who pass tend to say they did a stretch of theory and then built something. The developer exam in particular rewards having deployed against the API.
- Anthropic's engineering posts on [building effective agents](https://www.anthropic.com/engineering/building-effective-agents), [context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents), [writing tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents), and [Claude Code best practices](https://www.anthropic.com/engineering/claude-code-best-practices) map closely onto the architect domains.

## FAQ

### Can I get Claude certified as an individual?

Not directly. Anthropic opens certification to organizations in the Claude Partner Network, so individuals sit the exams through a participating company. For an independent engineer, joining a partner firm such as YAID is the shortest way in.

### Can freelancers and independent contractors take the Claude certification exams?

Yes, through a Claude Partner Network organization. Freelancers usually join a partner firm, since the alternative is registering their own company in the partner network and carrying the program requirements themselves.

### How do I register for a Claude certification exam?

Get eligibility through a Claude Partner Network organization, register inside the Anthropic Partner Academy, then schedule with Pearson VUE. If you are independent, apply to a partner firm first. YAID's application is at [youraidept.com/network/apply](https://youraidept.com/network/apply?ref=github). Full walkthrough: [registration.md](registration.md).

### How do I take the Claude Certified Architect exam if my company is not an Anthropic partner?

The same way. Either your company applies to the partner network, or you join a firm that is already in it and sit the exam under that firm's standing. Most independent engineers do the second.

### Does YAID provide access to the Claude Partner Network?

YAID is a registered Claude Partner Network company. Approved members become exam-eligible under YAID's partner standing and register through the Anthropic Partner Academy. Members do not become partners themselves; the partner relationship stays with YAID.

### How do independent engineers schedule a Pearson VUE Claude exam?

Registration starts in the Anthropic Partner Academy, which requires affiliation with a partner organization. From there you schedule with Pearson VUE, online proctored or at a test center.

### Is YAID an official Anthropic partner?

YAID is a registered member company of the Claude Partner Network. Anthropic runs the certification program and the partner network. YAID is a separate company and has no control over exam content, results, or credentials.

### What is the Claude Partner Network?

Anthropic's program for companies that bring Claude to market: consultancies, systems integrators, and service firms. Certification is open to organizations in the network and counts toward their partner standing.

### Is CCA-F the same as CCAR-F?

Yes. The official Pearson VUE listing uses CCAR-F for Claude Certified Architect – Foundations. CCA-F is the common shorthand.

### Does the certification belong to me or to the company I registered through?

To you. It stays with you if you leave the company or the partner firm.

### How long is a Claude certification valid?

12 months, with a free on-time renewal assessment on the Partner Academy.

### Can I use AI tools during the exam?

No. The exams are proctored and closed-book with no AI assistance.

### Do I need CCAR-F before CCAR-P?

No prerequisite is enforced. CCAR-P builds directly on the Foundations blueprint, so most candidates sit CCAR-F first.

### Is Claude certification worth it?

Depends on what you sell and to whom. We wrote up [the case for and against](https://youraidept.com/network/claude-certification-worth-it) for independent engineers, including when to skip it.

## Community study resources

Independent repositories with deeper study material. None are affiliated with Anthropic or with us.

- [paullarionov/claude-certified-architect](https://github.com/paullarionov/claude-certified-architect): a long CCAR-F study guide with PDF, EPUB, and Anki versions, translated into many languages.
- [daronyondem/claude-architect-exam-guide](https://github.com/daronyondem/claude-architect-exam-guide): a community CCAR-F preparation guide with a downloadable booklet.
- [preporato/claude-certification-guide](https://github.com/preporato/claude-certification-guide): study guides covering all four exams, with 30-day study paths.
- [OlivierAlter/Claude-Certified-Architect-Foundations-Certification-Exam](https://github.com/OlivierAlter/Claude-Certified-Architect-Foundations-Certification-Exam): an unofficial CCAR-F practice exam.
- [aderegil/claude-certified-architect](https://github.com/aderegil/claude-certified-architect): hands-on labs mapped to the five CCAR-F domains.
- [hamzafarooq/claude-certified-architect](https://github.com/hamzafarooq/claude-certified-architect): community CCAR-F study materials.
- [Amey-Thakur/CLAUDE-CERTIFICATIONS](https://github.com/Amey-Thakur/CLAUDE-CERTIFICATIONS): a study guide across all four certifications.

If you maintain one we have missed, open a pull request. [CONTRIBUTING.md](CONTRIBUTING.md) explains what we take and what we close.

## Sources

- [Pearson VUE: Claude Certification Program by Anthropic](https://www.pearsonvue.com/us/en/anthropic.html) (exams, eligibility, retake policy)
- [Anthropic: Services track and Partner Hub announcement](https://www.anthropic.com/news/services-track-partner-hub)
- [Claude Partner Network: partner application](https://claude.com/form/cpn-partner-application)
- [Anthropic Academy](https://anthropic.skilljar.com/) (public courses)
- The published exam guide for each certification, distributed through the Anthropic Partner Academy

## About YAID

[YAID (Your AI Department)](https://youraidept.com/network?ref=github) is a registered Claude Partner Network firm with a network for independent AI engineers. Members get eligibility to sit the Claude certification exams under YAID's partner standing, firm infrastructure for their client work (contracts, insurance, invoicing), and referred work once they qualify. Membership is $149 per quarter.

This handbook is not an official Anthropic resource. Anthropic controls the program, the exam content, and the credentials. Nothing here guarantees eligibility, a pass, or client work, and we will say so again on the application form.

Longer guides on youraidept.com: [How to get Claude certified](https://youraidept.com/network/claude-certification), [how to register](https://youraidept.com/network/register-for-claude-certification), [what it costs](https://youraidept.com/network/claude-certification-cost), [Partner Academy access](https://youraidept.com/network/anthropic-partner-academy), and the exam pages for [CCAR-F](https://youraidept.com/network/ccar-f), [CCDV-F](https://youraidept.com/network/ccdv-f), [CCAO-F](https://youraidept.com/network/ccao-f), and [CCAR-P](https://youraidept.com/network/ccar-p), each with [free practice questions](https://youraidept.com/network/ccar-f-practice-questions).

## License

Text and data in this repository are licensed under [CC BY 4.0](LICENSE). Reuse it or translate it; the only condition is attribution to YAID with a link back. Claude, Anthropic, and the certification names are trademarks of their owners and appear here to describe the program.
