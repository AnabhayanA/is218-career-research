# IS218 — Portfolio Plan / living project record

**Website:** https://anabhayana.github.io/is218-career-research/  
**Repository:** https://github.com/AnabhayanA/is218-career-research  
**Last updated:** 2026-11-19  
**Research question:** How can I become a software engineer who builds useful features with AI models and contributes to communities, and what do related employer roles expect?

**Personal career goal:** Become a software engineer working with AI models and developing new product features that solve real problems. I want to use my skills to give back to the communities served by the organizations I work with, and to the broader community. This is an aspiration, not a claim that I have already achieved these outcomes.

## 1. Career research — original employer descriptions

Source check date for all three: **November 19, 2026**. The source pages are employer-hosted job descriptions surfaced in search; the postings may change or close. Publication date and application deadline: **not stated in the retrieved descriptions**. Duties below are paraphrases. These roles are research examples, **not a claim of my eligibility or applications**.

| Role and original employer URL | Location and eligibility from posting | Three responsibilities | Learning gap (interpretation) |
| --- | --- | --- | --- |
| [Catena Clearing — Forward Deployed Engineer](https://jobs.lever.co/catena-clearing/1e1a2e89-8051-440a-b4cf-a3fe803ebce6) | Remote US, occasional travel; US-only/no sponsorship; 2+ years software experience preferred | Customer onboarding and troubleshooting; build/test data ingestion, mapping and webhooks; turn field issues into product feedback and documentation | API/webhook integrations and production data validation |
| [Makai Labs — AI Engineer](https://jobs.ashbyhq.com/makai-labs/a350e730-8d80-4528-9d41-497acbd01223/) | Remote, including NJ; contract; senior student/recent grad/early career, Python and AI project background | Build AI applications/tools; implement LLM/retrieval/agent workflows; benchmark/evaluate and harden prototypes | Evaluating LLM outputs and handling failures |
| [Arizent — Data & AI Engineer](https://jobs.ashbyhq.com/arizent/5f246f2b-8cd1-41ec-916c-9ed37a6b07a5/) | NYC Midtown, hybrid; 1+ years data/analytics/AI engineering, SQL/Python, agents, ETL | Build agents; build ETL pipelines/BigQuery reporting; test agent reliability and troubleshoot data quality | BigQuery/ETL and monitoring production agents |

**What changes relative to a conventional software role?** The Catena posting explicitly joins engineering with customer deployment and operational debugging. Makai expects LLM workflow design and evaluation, while Arizent combines AI agents with business data quality and cross-functional work. This comparison is based on these three postings, not every job with these titles.

**Two directions:** (A) forward deployed/customer-facing delivery and (B) AI application engineering. Both require engineering and communication. A emphasizes client-specific integration and field debugging; B emphasizes building/evaluating AI features and reliable data/LLM workflows. **Provisional choice:** software engineering focused on applied AI and useful product features, because it aligns with my goal of building technology that benefits people. **Next learning step:** make a small Python application feature with API integration, tests, and a written evaluation. **Assumption:** the chosen postings reasonably illustrate these directions; they are not a representative labor-market sample. Keep full personal reflection and circumstances in Canvas, not here.

## 2. Scope and agile planning

**In scope for the future portfolio:** homepage, research/decision record, individual project case studies with code and test links, truthful contributions, professional links when available, mobile-friendly navigation. **Out of scope for this Plan review:** finished professional portfolio, login, database, backend, analytics, fabricated testimonials and unverified outcomes.

**Primary audience:** internship reviewer. **Secondary:** potential collaborator or client. **Reader promise:** For an internship reviewer, make it easy to find concrete work, my contribution, code, verification, and a next action.

### User stories and acceptance criteria

1. As an internship reviewer, I can find an individual project in two navigation steps. **Accept:** homepage has a working project link and clear title.
2. As a reviewer, I can see what was implemented, what is planned and who contributed. **Accept:** each eventual case study labels individual/group/starter/AI-assisted work and limitations.
3. As a reviewer, I can inspect code and tests. **Accept:** linked repositories open; test claims are tied to real command output or CI.
4. As a research reader, I can compare career paths and inspect original sources. **Accept:** three postings show date checked, location, eligibility, duties and learning gaps; comparison links back to them.
5. As a keyboard/mobile visitor, I can navigate and read content. **Accept:** links work with keyboard focus and no horizontal overflow at common mobile widths.

### Prioritized tasks, milestones and ownership

| Priority | Milestone | Task | Owner | Status |
| --- | --- | --- | --- | --- |
| P0 | Plan | Research three employers and compare directions | Me | Drafted; direct page recheck recommended |
| P0 | Plan | Publish research site and project record | Me | Published, user-confirmed |
| P0 | Plan | Get partner feedback in GitHub issue; fix and request retest | Me + actual reviewer | Not done |
| P1 | First portfolio slice | One truthful individual project case study with source and tests | Me | Planned |
| P1 | Quality | Mobile/keyboard/link verification | Me + reviewer | Not run |
| P2 | Later portfolio | Add résumé, professional links and group work with attribution | Me | Pending actual materials |

## 3. Design alternatives and persuasion

**Voice:** curious, practical, clear, community-minded. **Character:** Creator with evidence-first proof.

**New visual direction (November 19):** A newspaper/editorial design inspired by traditional New York Times-style layouts, without copying its logo or brand. The site now uses an original masthead (“The Engineering Journal”), cream paper, strong serif typography, fine divider rules, editorial columns, and restrained red accents. This is a third, more personal direction that combines scanability with a recognizable editorial identity. The website was updated on GitHub, but live deployment, responsive behavior and accessibility still need browser verification.

- **A — Evidence-first grid:** restrained typography, high contrast, project evidence visible early. **Strength:** scanability for reviewers. **Limitation:** can feel generic.
- **B — Creative technical notebook:** expressive visual sections, experiments and process sketches. **Strength:** memorable personality and iteration. **Limitation:** more navigation and accessibility risk.
- **Provisional choice:** A. The homepage has now been redesigned in an editorial newspaper style that preserves A’s emphasis on scanability. A separate lightweight B mockup and peer comparison are not yet complete.
- **Persuasion choices:** link directly to inspectable code/tests; state contributions and limitations explicitly. Neither proves employability by itself.
- **Visual reference:** to be selected and cited; do not present an invented reference as inspected.

## 4. Technical architecture and tradeoffs

```text
Content author (Markdown + HTML)
             |
         GitHub repo
             |
       GitHub Pages (static)
             |
        Visitor browser
       HTML + CSS (+ JS only if needed)
```

**Chosen stack:** semantic HTML and CSS, GitHub Pages, Markdown documentation. **Why:** fast, inexpensive, inspectable, no authentication or persistence requirements. **Alternative:** React/Next.js supports reusable interactive components but adds build tooling and dependencies without a clear need at this stage. **Alternative:** Flask backend would add hosting, security and testing obligations with no benefit for a read-only portfolio. **Tradeoff:** static pages need manual content updates.

## 5. Code architecture and design principles

- `index.html`: semantic page sections, links, research content and navigation.
- `PORTFOLIO_RECORD.md`: decisions, source evidence, milestones and honest verification status.
- Future `styles.css`: layout and visual tokens if styling grows; future `assets/`: optimized images with descriptive alt text.
- **Single Responsibility Principle:** keep research decisions in Markdown and page presentation in HTML/CSS; split files when complexity warrants it.
- **Avoid premature patterns:** no repository/service/factory pattern or database layer needed. If project cards become numerous, use a simple data-driven template rather than duplicating markup. **Dependency inversion:** not useful without swappable services.

## 6. Testing, linting and static analysis plan

| Check | Level | When | Local / CI | Current status |
| --- | --- | --- | --- | --- |
| Original employer links and facts | Manual content review | Each research update | Local/manual | Indexed sources checked; direct page rendering not verified |
| Internal/external links | Integration/smoke | Each content update | Local; CI later | Not run |
| Semantic HTML validity | Static analysis (Nu Validator) | Each change | Local; CI later | Not run |
| CSS linting | Static analysis (Stylelint if CSS separated) | CSS changes | Local; CI later | Not configured |
| Keyboard tab order, focus, mobile widths | End-to-end/manual | Before each review | Browser locally; CI optional | Not run |
| Browser navigation smoke test | End-to-end (Playwright if site grows) | Before later portfolio releases | Local and CI | Not configured |
| Unit tests | Only for future JS logic | When logic exists | Local and CI | Not applicable yet |

**Failure policy:** fix broken links, invalid markup and accessibility blockers before marking the review ready; record known issues instead of claiming checks passed.

## 7. Build order, dependencies and open questions

1. Keep research source evidence accurate and label assumptions.
2. Ask a partner to follow a specific research/project-finding task.
3. Record observed difficulty in a GitHub issue; link a fix commit and request reviewer retest.
4. Build first portfolio slice: one real case study with clear contribution, repository and reproducible tests.
5. Validate mobile/keyboard/links and update this record.
6. Add further case studies and professional materials only when verified.

**Dependencies:** employer pages may change; second distinct AI/programming research site must be published before cross-link can be completed; peer review requires a real partner. **Open questions:** Which portfolio design does a real reader find easier? Which project has the best verified evidence? When will the second research site URL be ready?

## 8. Evidence and feedback

- [Python calculator](https://github.com/AnabhayanA/is218-oop-calculator) — individual project; verify current test results before stating a count.
- [Rock Paper Scissors](https://github.com/AnabhayanA/https-github.com-AnabhayanA-my-rps) — distinguish starter material from implemented work.
- [Iron Flight](https://github.com/AnabhayanA/iron-flight-game) — distinguish planned vs working features.
- Group contributions: not yet documented/verified here.
- Creative Project AI/programming exploration research site: **link pending**. Must be distinct from this site.
- [Feedback issues](https://github.com/AnabhayanA/is218-career-research/issues): reviewer, observed result, change link and retest **pending**. Never invent a peer review.

## Changed / Checked / Next

- **Changed:** Added three employer-backed role summaries, a career comparison, and a practical plan with architecture, stories, tests and milestones.
- **Checked:** Reviewed indexed employer descriptions on November 19, 2026; GitHub publishing confirmed by owner. Automated checks and real peer retest not yet performed.
- **Next:** Verify live site on mobile and keyboard, get actual peer feedback, link a documented change/retest, and cross-link the separate programming research site.

Course instructions: https://kaw393939.github.io/is218-studio/projects/portfolio.html
