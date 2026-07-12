# Story Bank — Master STAR+R Stories

This file accumulates your best interview stories over time. Each evaluation (Block F) adds new stories here. Instead of memorizing 100 answers, maintain 5-10 deep stories that you can bend to answer almost any behavioral question.

## How it works

1. Every time `/career-ops oferta` generates Block F (Interview Plan), new STAR+R stories get appended here
2. Before your next interview, review this file — your stories are already organized by theme
3. The "Big Three" questions can be answered with stories from this bank:
   - "Tell me about yourself" → combine 2-3 stories into a narrative
   - "Tell me about your most impactful project" → pick your highest-impact story
   - "Tell me about a conflict you resolved" → find a story with a Reflection

## Stories

<!-- Stories will be added here as you evaluate offers -->

---

### [Cloud Migration] BMO AWS Serverless-First Migration
**Source:** Report #090 — Teradata — Sr Principal Architect, Elastic Compute
**S (Situation):** BMO ran 40+ critical applications on VMware vSphere on-prem and needed a cloud-native migration without business disruption.
**T (Task):** Architect and deliver an end-to-end AWS migration with HA/DR built in, using CDK for repeatable infrastructure.
**A (Action):** Designed serverless-first deployment model — Lambda + ECS Fargate + CDK. Built multi-AZ HA architecture. Authored DR runbooks and validated them in pre-production. Managed VMware virtualised workload decommission in lockstep.
**R (Result):** Zero-downtime go-live; HA/DR validated before production cutover; CDK templates reused for future deployments.
**Reflection:** Serverless-first must be a day-one architectural decision, not a retrofit. The IaC templates encode the pattern and prevent drift. DR runbooks that were never rehearsed are not runbooks — validate before you need them.

---

### [Platform Automation] modeas — Shell-to-Python Migration at Charles Schwab
**Source:** Report #090 — Teradata — Sr Principal Architect, Elastic Compute
**S (Situation):** Charles Schwab's deployment system was built on a legacy shell-based programme — hard to maintain, slow, and error-prone at scale.
**T (Task):** Migrate the deployment platform to Python to improve maintainability and performance; deliver a platform that could handle the release cadence of a major brokerage.
**A (Action):** Rebuilt modeas from shell to Python — designed for maintainability first (clean module separation, testable, observable), then optimised for throughput. Treated it as an internal product: versioned, tested, with its own observability and self-service provisioning.
**R (Result):** 200+ builds/deployments per hour; 10,000+ ops hours eliminated annually; deployment cadence improved by 600%. Platform is maintainable by the team without specialist knowledge.
**Reflection:** Automation platforms need product-level thinking — version control, testing, observability. And the first question is always maintainability, not throughput. A fast system nobody can debug is a liability.

---

### [FinOps] BMO AWS Cost Optimisation Programme
**Source:** Report #090 — Teradata — Sr Principal Architect, Elastic Compute
**S (Situation):** BMO's AWS bill grew unchecked after the cloud migration; there was no cost attribution or rightsizing discipline.
**T (Task):** Own cloud cost transparency and waste elimination for the BMO AWS estate.
**A (Action):** Identified obsolete and unused resources; rightsized workloads to actual demand; implemented tagging taxonomy for cost attribution by team and workload.
**R (Result):** Measurable reduction in cloud waste; improved infrastructure cost efficiency; engineering teams started making cost-conscious deployment decisions.
**Reflection:** FinOps requires cultural change, not just tooling. Engineers need to see the cost of their deployment choices in real time — make it visible and they will optimise it naturally.
<!-- Format:
### [Theme] Story Title
**Source:** Report #NNN — Company — Role
**S (Situation):** ...

---

### [Incident Management] ADP SRE — MTTR Reduction via Blameless Culture + Automation
**Source:** Report #052 — Jefferies — VP Platform Reliability Engineer
**S (Situation):** ADP SRE had no structured postmortem culture; incidents were handled reactively, with firefighting as the default response mode.
**T (Task):** Build an incident management framework that would reduce MTTR and create lasting learning from failures across a 35-person team.
**A (Action):** Instituted blameless postmortem cadence; automated remediation via Ansible + Dynatrace alerting; defined MTTR SLOs and made them visible to engineering and leadership.
**R (Result):** MTTR reduced by 40%+; change success rate improved measurably; team shifted from reactive to predictive operations.
**Reflection:** Blameless culture requires top-down sponsorship first — the cultural change was harder than the tooling. Start by running the first postmortem yourself and modelling the behaviour you want.

---

### [Observability] ADP Full-Stack Observability Stack Build
**Source:** Report #052 — Jefferies — VP Platform Reliability Engineer
**S (Situation):** ADP platforms lacked unified observability; incidents were first detected via customer reports rather than internal alerting.
**T (Task):** Architect full-stack observability for a 35-person SRE organisation operating mission-critical HCM platforms.
**A (Action):** Deployed Prometheus + Grafana + Dynatrace; built alerting rules across network, app, and infrastructure layers; integrated with on-call tooling.
**R (Result):** Real-time RCA capability enabled; proactive bottleneck identification before business impact.
**Reflection:** Start with SLIs before choosing tools — otherwise you build beautiful dashboards nobody acts on. The metric has to correspond to a user-visible reliability threshold.

---

### [Automation / Toil Reduction] Robo Deployment Framework — RBC
**Source:** Report #052 — Jefferies — VP Platform Reliability Engineer
**S (Situation):** RBC had 250+ applications deployed manually; onboarding a new application to CI/CD took 5 weeks.
**T (Task):** Eliminate manual deployment and onboarding friction at enterprise scale across 60+ teams.
**A (Action):** Designed PowerShell-native CI/CD orchestration with self-service pipelines for Windows services, database deployments (SSIS, Oracle, SQL Server), and enterprise app workloads; automated artifact retrieval and approval workflows via Python and Ansible.
**R (Result):** Application onboarding reduced from 5 weeks to 5 hours (98% reduction); 250+ applications migrated.
**Reflection:** Automation is only durable if the people who use it own it. Co-design with the teams, not for them — or you'll spend your time fielding support tickets for your own automation.

---

### [Team Building / Greenfield] Charles Schwab Platform Engineering — Built from Zero
**Source:** Report #052 — Jefferies — VP Platform Reliability Engineer
**S (Situation):** Charles Schwab had no platform engineering function after the TD Ameritrade merger; SRE practices were inconsistent across the combined organisation.
**T (Task):** Stand up an 18-person Platform Engineering team and establish SRE practices from ground zero within one quarter.
**A (Action):** Hired and structured the team, defined reliability reviews, incident governance, and SRE gates for new platform deployments; established runbooks and on-call frameworks.
**R (Result):** 18-person team operational within one quarter; release reliability improved to 99.9%.
**Reflection:** The first 90 days of a greenfield team are about trust, not tooling. Focus on quick wins that prove value before introducing process — otherwise the team sees overhead, not help.
**T (Task):** ...
**A (Action):** ...
**R (Result):** ...
**Reflection:** What I learned / what I'd do differently
**Best for questions about:** [list of question types this story answers]
-->

### [Practice Building] ADP SRE Scale-Up — 4 to 40 Engineers
**Source:** Report #050 — Happiest Minds — Practice Director DevOps
**S:** ADP had a 4-person SRE team with no formal practice structure when Pavan's engagement began.
**T:** Scale to a high-performing, globally distributed SRE organization to meet ADP's enterprise reliability demands.
**A:** Hired, mentored, and structured 35+ engineers across India, Canada, and the US; introduced incident governance, blameless postmortem culture, and on-call frameworks.
**R:** 40-engineer org built in ~18 months; MTTR reduced by 40%+; SRE practices embedded across ADP's global delivery.
**Reflection:** I would have defined career ladders earlier — the absence of growth structure caused attrition in months 6–12.
**Best for questions about:** Team building, leadership, scaling organizations, engineering culture

### [GTM / Pre-Sales] $478K SOW Closure — RBC Capital Markets DevOps
**Source:** Report #050 — Happiest Minds — Practice Director DevOps
**S:** RBC Capital Markets needed a DevOps transformation with no existing vendor relationship in place.
**T:** Win the SOW and deliver the engagement.
**A:** Led technical discovery, shaped the proposal with a 12-member 18-month plan, presented to CTO-level stakeholders at RBC subsidiaries.
**R:** $478K SOW closed; 12-member team mobilized; DevOps transformation delivered successfully.
**Reflection:** Pre-sales credibility comes from delivery track record — always bring proof of prior work, not slide decks.
**Best for questions about:** Business development, pre-sales, stakeholder influence, commercial acumen

### [Frameworks / Accelerators] Robo Deployment Framework — 5 Weeks → 5 Hours
**Source:** Report #050 — Happiest Minds — Practice Director DevOps
**S:** RBC Insurance had 250+ applications, each requiring 5 weeks of manual onboarding to CI/CD pipelines.
**T:** Build a self-service framework that works across heterogeneous stacks (Java, .NET, Oracle, SQL Server).
**A:** Designed a PowerShell-native CI/CD orchestration platform; abstracted deployment logic; built automated approval workflows in Python and Ansible.
**R:** Application onboarding reduced from 5 weeks to 5 hours (98% reduction); enabled migration of 250+ apps to GitHub.
**Reflection:** Reusable frameworks only scale if adoption is managed — I'd invest more in enablement alongside the tooling.
**Best for questions about:** Innovation, automation, efficiency, IP creation, scale

### [Metrics / Delivery] DORA Framework Adoption — RBC Wealth Management
**Source:** Report #050 — Happiest Minds — Practice Director DevOps
**S:** RBC had no shared engineering health metrics; 60+ teams had no common definition of delivery performance.
**T:** Introduce DORA as the north star for DevOps maturity across the organization.
**A:** Defined Deployment Frequency, Lead Time, Change Failure Rate, and MTTR using Azure DevOps; built dashboards; ran quarterly reviews.
**R:** Measurable improvement in delivery performance and production stability; DORA became a shared language across 60+ teams.
**Reflection:** Metrics adoption requires executive sponsorship — without a VP-level champion, teams will track but not act on data.
**Best for questions about:** Metrics, organizational change, delivery performance, measurement

### [Executive Communication] C-Suite Reliability Reporting — ADP
**Source:** Report #050 — Happiest Minds — Practice Director DevOps
**S:** ADP's VP and C-suite had no visibility into engineering reliability; perception was shaped by incident noise.
**T:** Establish SRE as a strategic function visible at the executive level.
**A:** Built a reliability scorecard, translated SLO performance into business impact language, presented quarterly to VP+ stakeholders.
**R:** SRE function gained strategic visibility; error budget concept adopted by product leadership.
**Reflection:** Non-technical executives respond to risk and cost language, not uptime percentages — always translate before presenting.
**Best for questions about:** Stakeholder communication, influencing without authority, executive presence

### [Resilience Engineering] Chaos Engineering Programme at ADP — Keptn
**Source:** Report #095 — Citi — DevOps Application Support Manager, VP
**S:** ADP's SRE team had no proactive fault injection capability; platform reliability was only discovered under production failure conditions.
**T:** Establish a chaos engineering programme to surface fault scenarios before they reached users.
**A:** Deployed Keptn-based chaos testing framework; defined fault scenarios (network partition, pod eviction, latency injection); ran quarterly wargaming sessions with the SRE team; built pre-test runbooks for every fault scenario tested.
**R:** Proactively identified and hardened 12+ failure scenarios; reduced production surprises during high-traffic and incident peaks.
**Reflection:** Chaos engineering only works if there is a known recovery playbook before you inject the fault. Build the runbook first, validate the recovery path, then run the test — not the other way around.
**Best for questions about:** Resilience, chaos engineering, proactive reliability, disaster recovery, SRE maturity

### [Platform Product Management] CPMI + DevOps as a Service — Internal Platform Ownership
**Source:** Report #101 — Northern Trust — Global Head of Platform Engineering
**S (Situation):** Three concurrent banking clients (ADP, Schwab, BMO) had no shared standard for measuring or improving platform engineering maturity; each was at a different level with no common language.
**T (Task):** Create a shared framework and product that clients would adopt voluntarily — not because they were told to.
**A (Action):** Designed the Cloud Platform Maturity Index (CPMI) — a scored maturity model with an adoption playbook, tooling recommendations, and a DevOps as a Service catalogue. Built it as an internal product with its own roadmap and versioning, not as a one-off delivery.
**R (Result):** Adopted across all three clients; measurable improvement in cloud capability, security posture, and automation maturity; CPMI became the shared language for engineering capability conversations with client leadership.
**Reflection:** Internal platforms succeed when they solve the developer's problem first. I made the CPMI scoring immediately actionable — every tier told you what to do next, not just where you stood.
**Best for questions about:** Platform product management, internal tooling, developer experience, influence without authority, roadmap ownership

---

### [AI Platform Operations] BMO GenAI Assistants — AWS Bedrock
**Source:** Report #095 — Citi — DevOps Application Support Manager, VP
**S:** BMO's risk analysis teams spent significant manual effort reviewing and summarising structured risk reports; no AI tooling was in place.
**T:** Design and deploy GenAI assistants to reduce manual analysis effort and accelerate insights delivery within BMO's compliance perimeter.
**A:** Built GenAI assistants using AWS Bedrock; integrated BCRG and LTS risk data pipelines; enabled interactive Q&A over structured risk reports; designed audit trail and explainability layers for compliance.
**R:** Reduced manual analysis effort measurably; risk teams accelerated insights delivery; assistant deployed within regulatory and data governance constraints.
**Reflection:** In banking, the AI is the easy part. The real work is data governance, audit trail, and explainability — design those first or you will not get past the compliance review.
**Best for questions about:** GenAI in production, AI platform operations, regulated AI deployment, banking AI use cases
