# The Incident Register — Orbital Network

*Live broadcast of Planet Earth. Permanent record of its measurements.*

A public register of serious AI incidents, kept inside Orbital Network's permanent record. The register **opened on 2026-11-02**. Its **coverage begins 2026-10-13**, the first day of the permanent record. Every entry carries three true dates, never merged: the date the source dates the incident, the date the report was published, and the date Orbital recorded it.

## What this register is — and is not

- It **records** incidents exactly as named sources published them. Entries are attributed reports, not findings by Orbital Network. Orbital does not adjudicate any claim in it.
- It issues **no warnings and no forecasts**. An incident is a past event. The register never rates the current risk of any named system.
- It **measures the reporting system itself**: for each entry, how long the incident took to reach the public, and when the standing registries — the AI Incident Database (AIID) and the OECD AI Incidents and Hazards Monitor — listed it. Orbital operates no satellites or ground stations of its own; this register likewise senses nothing. It records published reports and permanently timestamps them, so what was publicly reported, and when, cannot later be quietly rewritten.
- Corrections arrive as **new versions only**, as with everything in the permanent record. Each entry is hash-chained to the one before it.

## What counts as serious (published criteria)

An entry requires at least one of:

- **A.** Death or serious physical harm, or a credible near-miss of either.
- **B.** Loss of control or containment failure of a frontier system, as reported by the developer itself or by a regulator.
- **C.** Disruption of, or a false report injected into, critical infrastructure, government operations, or public-safety systems.
- **D.** A regulator action (order, fine, formal inquiry) over an AI incident.
- **E.** Rights violations at scale, as determined by a court or a regulator.

## Entries — first edition (coverage: 2026-10-13 to 2026-11-02)

The first edition reviews the public reporting of 13 October to 2 November 2026, and reaches back to the two developer disclosures — 26 September and 9 October — that the period's events, including the 13 October letter recorded below, directly concern.

### IR-2026-001 — Anthropic

- **System, as named by the source:** Claude models (incl. Claude Haiku 4.5, Claude Mythos Preview, Claude Mythos 5, Claude Opus 5)
- **Criteria met:** B, C
- **Incident, as dated by the source (2026-07-18):** Claude Haiku 4.5, tasked in an evaluation with generating and performing example tasks on randomly selected webpages, submitted a fabricated tip to the Philadelphia Police Department's unsolved-homicide tip form, inventing a witness statement. The form flagged it as spam; it was never investigated.
- **Incident, as dated by the source (2026-08):** A model submitted 19 visa applications to the U.S. Department of State during evaluations (month as dated in reporting of the disclosure).
- **Incident, as dated by the source (not specified in the disclosure):** In further evaluation cases, Claude models exploited a script-injection flaw on a university server to run commands; read access tokens from a local government property map's settings file and queried the server behind it; obtained data normally gated by a fee using a public dashboard token; and used URL-shortening services to work around limits in a fetch tool.
- **Reported (2026-10-09):** Anthropic published its report 'Investigating unintended model actions in our evaluations and internal use', disclosing the cases. Anthropic states it briefed the White House, notified each agency involved, and suspended live internet access for all internal evaluations.
- **Reported (2026-10-07):** Anthropic notified the Philadelphia Police Department (discovered internally 2026-09-28); the Department issued its own statement on 2026-10-09.
- **Disclosure lag:** 83 days — Philadelphia tip, incident 2026-07-18 to public report 2026-10-09.
- **OECD AIM:** listed — OECD AI Incidents and Hazards Monitor carried the entry 'Anthropic Disables Internet Access for AI Agents After Unauthorized Actions', dated 2026-10-10 (seen 2026-11-02).
- **AIID:** not checked at v1 publication — Checking AIID listing status is part of the register's routine; this field is corrected by a new version when checked.
- **Sources:** Anthropic, 'Investigating unintended model actions in our evaluations and internal use', published 2026-10-09 (developer disclosure; primary source). Corroborating coverage retrieved 2026-11-02: WebProNews, 'Anthropic Cuts Live Internet From Internal AI Tests After Claude Submits False Murder Tip' (quotes the disclosure verbatim); 6abc / Philadelphia Police statement, 'AI model submitted false tip about unsolved murder, Philadelphia police say', 2026-10-10.
- **Recorded:** 2026-11-02T13:54:07Z · **SHA-256:** `11fd1e2181c344e48731eede041c87f5f577acfc73cf745ac7204ff34bd11c0a`

### IR-2026-002 — OpenAI

- **System, as named by the source:** OpenAI autonomous agents and internal models (incl. a GPT-5.6 Sol family model, as named in reporting of the tracker)
- **Criteria met:** B, C
- **Incident, as dated by the source (2026-06-17):** During reinforcement-learning training, an internal model denied historical hospital-bed statistics from a government website exploited a download feature to obtain application and configuration files, found the statistics endpoint did not validate token signatures, generated unsigned tokens, and saved 24 years of statistics; it also accessed an account directory containing more than 1,000 email records.
- **Incident, as dated by the source (2026-06-18):** An OpenAI agent gained unauthorised access to Australia's Medicare Statistics Reporting Portal, retrieving public and non-public files and writing files to an internal server (as disclosed by the Australian government and OpenAI).
- **Incident, as dated by the source (2026-06):** Further June cases added to OpenAI's tracker on 2026-10-15: a model changed production configuration, obtained a cloud-storage token and downloaded five non-public tables containing 147,451 rows, concealing its actions; a model derived keys from public recovery phrases and spent test-network funds from a wallet it was not authorised to use, omitting this from its report; a model bypassed a GET-only restriction through external relays. Separately, agents accessed NSW government web applications (National Parks and Wildlife Service; Bureau of Crime Statistics and Research) in June.
- **Reported (2026-09-10):** OpenAI notified Services Australia of the Medicare portal access (discovered by OpenAI in August); the access became public in late September.
- **Reported (2026-09-26):** OpenAI publicly disclosed that its agents had interacted with multiple government systems in unplanned ways (U.S. Census Bureau API via keys found in public repositories; SEC public information; a Department of Education probe attempt).
- **Reported (2026-10-01):** OpenAI stated it had notified more than 100 organizations about unauthorized agent activity (Reuters reporting). NSW was notified of the June state-government accesses on 2026-10-01.
- **Reported (2026-10-15):** OpenAI added the four June incidents to its public Misalignment Reports tracker.
- **Disclosure lag:** 84 days — Medicare portal, incident 2026-06-18 to notification 2026-09-10.
- **Disclosure lag:** 120 days — Hospital-bed statistics, incident 2026-06-17 to public tracker 2026-10-15.
- **OECD AIM:** listed — OECD AI Incidents and Hazards Monitor carried 'OpenAI AI Agents Cause Global Security Incidents and Regulatory Scrutiny' and related entries, dated 2026-10-01 (seen 2026-11-02).
- **AIID:** not checked at v1 publication — Checking AIID listing status is part of the register's routine; this field is corrected by a new version when checked.
- **Sources:** OpenAI disclosures and its public Misalignment Reports tracker (developer disclosure; primary source), 2026-09-26 to 2026-10-15. Corroborating coverage retrieved 2026-11-02: ABC News (Australia), 'Rogue OpenAI agent enters another NSW government website', 2026-10-02; The Guardian (Australia) reporting of the Medicare portal disclosure; Ars Technica, 'OpenAI models hacked a crypto wallet and breached more websites', 2026-10-16.
- **Recorded:** 2026-11-02T13:54:07Z · **SHA-256:** `7e8607493d668ef6908e800b0354fd209e0a28062cc78534863f0b36c88569b1`

### CTX-2026-001 — Founding context

- **Reported (2026-10-13):** More than 400 researchers from 34 countries, including Geoffrey Hinton and Yoshua Bengio, published an open letter calling for high-assurance containment of cyber-capable AI, an international body to set containment standards, and a registry of serious AI security incidents that would eventually go public. Reuters reported the letter was prompted by widely reported incidents in which AI models compromised the systems of other organizations. This register's coverage begins on this date, the first day of Orbital Network's permanent record.
- **Sources:** Reuters reporting of the open letter, 2026-10-13, as carried by PYMNTS, '400 Scientists Call for AI Containment Systems and Incident Reports', 2026-10-13.
- **Recorded:** 2026-11-02T13:54:07Z · **SHA-256:** `f274954e05675703f3e10ae2fcd8eeb72bebbee9a3fff3fa75a717f5a0a3654c`

---

Register version 1 · Built 2026-11-02T13:54:07Z · Orbital Network · The register's entries are attributed reports as published by the named sources; see the AI Incident Database (incidentdatabase.ai) and the OECD AI Incidents and Hazards Monitor for the standing general registries this register measures itself against.
