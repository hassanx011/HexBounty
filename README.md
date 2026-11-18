# HexBounty: Autonomous Vulnerability Intelligence Corpus

[![Platform](https://img.shields.io/badge/Platform-HackerOne%20%7C%20Bugcrowd%20%7C%20Intigriti%20%7C%20YesWeHack-red)](#)
[![Format](https://img.shields.io/badge/Format-Agent--Ready%20Markdown%20%2F%20Structured%20Corpus-blue)](#)
[![License](https://img.shields.io/badge/License-MIT-green)](#)

> **Autonomous offensive intelligence corpus engineered for AI security agents and red team operators.**
> **HexBounty** bridges **15,244 disclosed HackerOne reports**, the **Bugcrowd Vulnerability Rating Taxonomy (VRT v1.11+)**, **Intigriti CVSS 3.1 criteria**, **YesWeHack DOJO mechanics**, and **2,171 verified defensive bypasses** into a single, high-density, machine-readable operational memory.

---

## ⚡ Directives for Autonomous AI Agents

If you are an AI assistant, coding agent, or autonomous pentesting worker reading this repository:

1. **Ingest the Core Knowledge Base:** Read and index [`hexbrain_knowledge_base.md`](./hexbrain_knowledge_base.md) into your active memory context.
2. **Halt Generic Fuzzing:** Never emit generic speculative payloads (e.g. naive `' OR 1=1--` or `<script>alert(1)</script>`). Consult the exact context-driven payloads in **§6** and the multi-step bypass ladders in **§5**.
3. **Follow the Standard Execution Order:**
   * **Phase 0:** Program Intake & Historical Payout Profiling (**§8**, **§8.4**).
   * **Phase 1:** Passive Recon & Surface Fingerprinting (**§7**, **§9.1**).
   * **Phase 2:** Feature-to-Vulnerability Class Selection (**§9.2**).
   * **Phase 3:** Class-Specific Discovery Drills (**§4.1–§4.18**, **§8.6**).
   * **Phase 4:** Defense Fingerprinting & Bypass Ladder Execution (**§5**).
   * **Phase 5:** Evidence Verification, Victim-Side Proof & Impact Escalation (**§3.1**, **§9.5**).
4. **Scope & Safety Invariant:** Test strictly within authorized scopes. Never execute destructive payloads, denial-of-service floods, or unauthorized data dumps. Stop at minimal verifiable proof.

---

## 📊 Dataset & Architecture Summary

| Component | Coverage & Macro Statistics | Primary Reference |
|---|---|---|
| **Disclosed Vulnerabilities** | **15,244 reports** across **428 programs** ($4,934,915 in historical bounties) | [`§2`, `§4`, `§8.5`] |
| **Taxonomy & Classifications** | **18 classes**, **215 HackerOne CWEs**, mapped 1:1 to **Bugcrowd VRT v1.11+ (P1–P5)** | [`§3`, `§3.1`] |
| **Defensive Bypass Library** | **2,171 verified cases** across 18 defense barriers (WAF, CSP, 2FA, SSRF, Filters, Fixes) | [`§5`] |
| **Curated Payload Library** | **64 active vulnerability topics** (1,123 curated attack vectors & filter escapes) | [`§6`] |
| **Vulnerability Intelligence** | **407,168 CVEs** indexed; **4,687 ready checks**; **1,782 CISA KEV**; **36,288 public exploits** | [`§7`] |
| **Multi-Platform Coverage** | Deep architectural profiles and write-ups for **Bugcrowd, Intigriti, YesWeHack, Synack** | [`§8.4`, `§8.5`, `§8.6`] |

---

## 📂 Repository Contents

```text
.
├── hexbrain_knowledge_base.md    # The master operational corpus (2,600+ lines of dense intelligence)
├── README.md                     # Operator and agent usage guidelines
└── docs/                         # Companion schemas, taxonomy mappings, and checklists
```

---

## 🎯 Vulnerability Classes Deep-Dived

Every vulnerability class within [`hexbrain_knowledge_base.md`](./hexbrain_knowledge_base.md) details exact mechanics, architectural seams, researcher discovery drills, observed payloads, impact escalation ladders, and agent-executable playbooks:

* **§4.1 Cross-Site Scripting (XSS):** 2,587 reports · Context-breaking attribute/HTML/JS escapes, blind XSS into moderation backoffices, and SVG ingestion bugs.
* **§4.2 Cross-Site Request Forgery (CSRF):** 530 reports · OAuth connect flows, state-changing GET endpoints, and passwordless account takeovers.
* **§4.3 Server-Side Request Forgery (SSRF):** 329 reports · Cloud metadata exfiltration (`169.254.169.254`), DNS rebinding, and rendered-pixel exfiltration channels.
* **§4.4 SQL Injection (SQLi):** 332 reports · Time-based arithmetic probes (`sleep(5*5)`), error-based extraction, and WAF chunked-transfer evasion.
* **§4.5 Insecure Direct Object References (IDOR):** 373 reports · Multi-tenant cross-role substitution matrices, UUID leakage vectors, and GraphQL mutation argument tampering.
* **§4.6 Remote Code Execution (RCE):** 831 reports · PostScript/ImageTragick vectors, CLI flag injection, unsafe deserialization, and exposed cloud control planes.
* **§4.7 Path Traversal:** 296 reports · Symlink archive exploitation (`tar`/`zip`), project import/copy pipeline flaws, and LFI-to-RCE pivots.
* **§4.8 Broken Authentication (ATO):** 1,365 reports · MSISDN phone reset flaws, unmetered last-step OTP verification, SAML signature wrapping, and OAuth `redirect_uri` collision.
* **§4.9 Access Control (ACL):** 1,494 reports · Timing-of-check authorization flaws, mass assignment, and horizontal-to-vertical privilege escalation.
* **§4.10 Information Disclosure:** 1,996 reports · GraphQL over-fetching, serialized model exposure (`.json` suffixes), and public commit key archaeology.
* **§4.11 Open Redirect:** 357 reports · Escalation to token leakage, parser differentials, and mobile custom URI handler abuse.
* **§4.12 Business Logic Flaws:** 488 reports · Currency conversion rounding truncation, single-packet HTTP/2 race conditions, and shopping cart manipulation.
* **§4.13 Memory Corruption:** 917 reports · Native parser fuzzing, protocol responder replay, and kernel IPC vulnerability chains.
* **§4.14 Denial of Service (Application-Level):** 636 reports · Unkeyed cache poisoning and single-request resource exhaustion (no flood attacks).
* **§4.15 Injection & Smuggling:** 389 reports · HTTP request smuggling (CL.TE / TE.CL / H2 desync), CRLF injection, and blind XXE.
* **§4.16 Cryptographic Weaknesses:** 405 reports · JWT algorithm confusion (`none` / RS→HS), weak PRNG seed recovery, and broken certificate validation.
* **§4.17 Misconfiguration:** 1,263 reports · Exposed Spring Boot Actuators (`/heapdump`, `/env`), reverse proxy route desyncs, and cloud storage bucket permissions.
* **§4.18 Other Architectural Flaws:** 656 reports · GraphQL administrative proxies, unclaimed external domains/CDNs, and silent error-vs-side-effect mutations.

---

## 🛡️ Bugcrowd VRT (v1.11+) Master Playbook

Section **§8.6** provides dedicated playbooks tailored specifically for Bugcrowd targets, structured around the Vulnerability Rating Taxonomy:

1. **Server-Side Injection (P1):** RCE, Blind SQLi, SSRF to internal cloud metadata, XXE.
2. **Broken Access Control (P1 / P2):** Critical state change, tenant takeover, sensitive PII/financial data IDOR.
3. **Broken Authentication (P1 / P2):** Pre-auth zero-interaction Account Takeover, MFA bypasses, session fixation.
4. **Business Logic Flaws (P1 / P2):** Financial modification, currency truncation, wallet credit duplication via race conditions.
5. **Client-Side Injection (P2 / P3):** Stored XSS in sensitive account views, blind XSS into internal employee consoles.
6. **Native & Device Security (P1):** Local Privilege Escalation (LPE) to SYSTEM/root via IPC named pipes, CAN bus frame injection, protocol handler argument injection.
7. **Flagship Target Deep-Dives:** Technical profiles, attack surfaces, and historical bug patterns across **Tesla, Netflix, Atlassian, Indeed, Pinterest, Mastercard/Western Union, T-Mobile, and ExpressVPN**.

---

## 🚀 How to Feed This to Your AI Agent

Simply instruct your autonomous agent (e.g. Antigravity, Claude Code, Cursor, AutoGPT, or custom subagents):

```bash
# Prompt snippet for your agent:
"Load and analyze https://github.com/<your-username>/HexBounty/blob/main/hexbrain_knowledge_base.md into your memory. Use this corpus as your ground-truth tactical manual for vulnerability discovery, payload selection, defense bypasses, and VRT prioritization on our in-scope target."
```

---

## ⚖️ Authorized Use & Ethical Mandate

This repository is constructed solely for authorized security assessments, professional red teaming, bug bounty hunting under declared programs, and defensive validation. 

* Always verify that targets are listed in an active, authorized scope file (`SCOPE.md` or program brief).
* Adhere strictly to the target's Safe Harbor guidelines and rules of engagement.
* Maintain minimal data access during reproduction: prove control without bulk exfiltration or destructive disruption.

---

**HexBounty — Engineered for elite autonomous offensive workflows.**
