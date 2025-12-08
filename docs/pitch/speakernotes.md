# slide 1

Quantum computing will break classical RSA/ECC encryption within 5–10 years— not a theoretical concern but a documented timeline (NSM-10 directive, NIST roadmap). This research fills a critical gap: organizations lack empirical evidence to make PQC deployment decisions.  Doing research on sector-specific performance benchmarks (latency, memory, throughput), validate side-channel mitigations (masking, constant-time), and deliver governance roadmaps aligned with CSF 2.0 and NIST standards. The result is actionable transition strategies for finance (<30ms latency), healthcare (10+ year data validity), and IoT (resource-constrained devices). This research will help operational readiness.

# slide 2

Agenda

# Slide 3

The quantum threat is real and imminent: cryptographically-relevant quantum computers will break RSA/ECC within 5–10 years, forcing organizations to transition immediately. However, this transition isn't one-size-fits-all. Finance organizations face strict latency requirements—Ahmed et al. (2025) validates that Kyber achieves 13.5 ms and Dilithium 26.5 ms average, both under the critical 30 ms threshold for real-time transactions. Healthcare sectors face a different constraint: data must remain secure and integrity-verifiable for 10+ years, making SPHINCS the preferred choice for long-term archival signatures. IoT deployments are memory and power-constrained, requiring lightweight implementations. Yet despite these sector-specific needs, no unified governance roadmap exists in industry today—organizations lack guidance on compliant, risk-managed PQC transitions aligned with CSF 2.0 and NIST standards. This research fills that critical gap by delivering empirical evidence, sector-specific algorithm recommendations, and governance frameworks that enable organizations to make confident PQC deployment decisions.

# Slide 4

This chart shows the government's plan to transition from old encryption to quantum-safe encryption by 2030.computer's passwords and secrets are currently protected by encryption that works with:
RSA (most common)
ECC (newer but still vulnerable)
The Problem: Quantum computers (when they exist) can break these in hours instead of thousands of years.
The Solution: Switch to Post-Quantum Cryptography (PQC) – new math-based encryption that quantum computers can't break.

# Slide 5

NIST's PQC standardization journey spans eight years of rigorous cryptographic research. In December 2016, NIST issued a global call for post-quantum algorithms, inviting experts worldwide to submit candidates that could withstand quantum computer attacks. By 2022, after extensive evaluation including security analysis, performance testing, and side-channel resistance assessment, NIST selected the three finalists: Kyber (key encapsulation), Dilithium (digital signatures), and SPHINCS (stateless hash-based signatures)—these are the cryptographic "winners" that cannot be broken by known quantum algorithms. By late 2024, NIST published the final standards officially, enabling government agencies and private organizations to begin PQC deployment with confidence. This Phase 1 completion signals the end of the research phase and the start of the migration phase.

# Slide 6

The U.S. government's PQC transition is coordinated across five key agencies with clear deadlines and accountability. NSA mandated in May 2022 that all systems must switch to PQC, with specific targets: by 2033, web, cloud, operating systems, devices, and networking equipment must use quantum-safe encryption. OMB oversees all federal agencies: by October 2022, agencies inventoried their cryptosystems; by November 2022, OMB published transition guidance; 
and within one year of NIST standards (late 2024), every agency must have a formal PQC transition plan. CISA executes the transition: by 2024, releasing tools and support; by 2030, all critical infrastructure must be using PQC. NCD coordinates progress: reporting in October 2023 and annually thereafter, and securing ongoing funding for PQC projects. This multi-agency approach ensures no organization gets left behind—with inventory, planning, tooling, and execution phases clearly defined. Organizations aligned with this roadmap gain compliance readiness and competitive advantage.


# Slide 7

My research directly addresses three critical gaps exposed by the government's 2030 transition deadline. First: organizations don't know if PQC algorithms (Kyber, Dilithium, SPHINCS) actually perform fast enough—I provide empirical latency and throughput benchmarks across sectors. Second: side-channel attacks remain a vulnerability even with quantum-safe algorithms—my evidence table validates masking and constant-time mitigations actually reduce attack success rates. Third: governance chaos—different agencies have different deadlines, and most organizations lack a compliant transition framework—I deliver a CSF 2.0-aligned roadmap that works. Without this research, organizations default to expensive trial-and-error. With it, they deploy PQC with confidence, meeting the 2030 mandate without sacrificing performance, security, or compliance.


# Slide 8

This evidence table is the backbone of my research. Three independent studies validate my three research questions: Ahmed et al. (2025) benchmarks Kyber and Dilithium at sub-30ms latency for finance and recommends SPHINCS for long-term healthcare archival—answering RQ-D1 on performance. Boyens (2023)—note I've updated this from "Epure" for accuracy—demonstrates that masking and constant-time code effectively reduce side-channel leakage in real pilots, validating RQ-C2 mitigation strategies. NIST (2024) provides the governance blueprint: phased rollout with parallel stacks and rollback procedures, directly supporting RQ-G1 organizational readiness. Together, these three sources prove PQC is not just theoretically quantum-safe—it's performant, resistant to attack, and governable at enterprise scale. This is the evidence organizations need to make the 2030 transition with confidence.


# Slide 9

My methodology is a four-stage pipeline: data collection (quantitative meta-analysis of peer-reviewed PQC studies + qualitative 15–20 interviews with security leaders), instrumentation (extraction protocols, PRISMA rubric for systematic bias mitigation), analysis (coding and integration via joint-display matrices), and output (performance benchmarks and governance roadmaps). Three SMART metrics operationalize accountability: Source Coverage Ratio (≥80% industry + peer-reviewed sources, mitigating bias per 800-171r3), Side-Channel Effectiveness (<10% residual leakage post-mitigation validating RQ-C2), and Governance Adoption Rate (>60% of interviews confirming phased PQC rollout alignment with NIST). These metrics are reproducible—anyone can run the Docker command next slide and verify results identically. This mixed-methods design synthesizes hard performance data (Ahmed: <30ms latency in finance, ~15ms in IoT) with real-world governance experience (Boyens: masking effectiveness in pilots, NIST: phased precedent), ensuring research is both empirically rigorous and operationally actionable.


# Slide 10

This slide anchors my PQC research to two foundational federal standards verified against official PDFs. 
First: CSF 2.0 PR.PS (Platform Security, Appendix A, p. 25) mandates that "hardware, software, firmware, operating systems, applications, and services are managed consistent with the organization's risk strategy to protect confidentiality, integrity, and availability"—my research operationalizes this by benchmarking PQC implementation security practices across sectors and demonstrating continuous secure software monitoring via performance logs and vulnerability tracking. 
Second: SP 800-207 Zero Trust Architecture (Section 3.3.1, p. 16) requires "all resource authentication and authorization are dynamic and strictly enforced before access is allowed" with "continual monitoring and possible reauthentication"—my PQC auth middleware implements this by deploying session-based MFA with audit logging on every API request and real-time anomaly detection for continuous reauthentication. 
Together, these standards prove PQC isn't just quantum-safe—it's a compliance enabler for modern zero-trust architectures. Quote these exact outcomes during delivery for unimpeachable standards grounding.


# Slide 11

Exact Screenshot from CSF2.0 and SO 800-207 as evidence


# Slide 12

This slide operationalizes three critical safeguards distilled from Week 7 risk analysis and Week 8 governance documentation. 
First: Privacy & Confidentiality (Week 7 ETHICS.md)—I de-identify all interview data using pseudonyms with removal of identifiers, encrypt sensitive data at rest/transit using AES-256, enforce least-privilege access with quarterly reviews, and ensure secure erasure post-retention (5-year retention, then purged). Mitigates re-identification and parameter leakage risks. Second: Data Handling & Versioning (Week 8 DMP.md)—all code versioned via Git with checksums, Jupyter transformation logs tracked, encrypted S3 backups maintained. Sensitive artifacts (interviews, test logs) never shared publicly; only aggregated results published. Ensures audit-ready traceability. Third: Supplier Risk & C-SCRM (Week 8 cSRM_note.md)—open-source PQC libraries (Kyber/Dilithium/SPHINCS) tracked via SBOM (Software Bill of Materials) with checksums, proactive vulnerability monitoring in CI/CD pipeline per NIST SP 800-161r1. All three safeguards map to AU-2 (Audit Events, SP 800-53 Rev. 5) and 800-171r3 controls for organization-defined event logging and accountability. Point to docs/DMP.md and docs/cSRM_note.md for full implementation details.



# Slide 13

This slide demonstrates the traceability framework from Week 11—the backbone of my research governance. I start with a Risk→Requirement→Metric→Evidence chain: I have identified a risk (insufficient published metrics for PQC variants), traced it to a requirement (800-171r3 03.02.01: establish baseline of security-relevant data sources), operationalized it as a metric (Source Coverage Ratio), and pointed to the evidence artifact (docs/sourcecount.csv). This chain ensures every metric is auditable and tied to a concrete risk. The three SMART metrics on the slide—Source Coverage Ratio (unique PQC sources / total sources), Reference Freshness (average publication year, goal >75%  post-2023), and Privacy Incident Rate (leaked test runs / total test runs, goal zero tolerance)—are then tracked in specific data sources: sourcecount.csv, sourcelog.csv, and testoutput.log respectively. All three metrics are weekly updated and reproducible via the Docker command I'll show on the next slide. The full requirement text (03.02.01) stays in Week 7–11 documentation; the slide shows only the ID and metric formula for clarity. This operationalizes accountability: every metric has a purpose, every metric has a source, and every metric is verifiable.

# Slide 14

This slide shows how the CSF 2.0 outcomes PR.DS and PR.PS translate from today’s reality to a target post-quantum state using the SP 1301 governance lens. Current PR.DS is manual RSA/ECC key management with de facto monitoring, while the target is automated key management with Kyber, Dilithium, and SPHINCS plus real-time visibility into cryptographic events and side-channel anomalies. Current PR.PS is legacy crypto libraries, inconsistent version tracking, and ad-hoc patching; the target is SBOM-tracked PQC libraries, continuous vulnerability scanning in CI/CD, and proactive patching aligned to NIST SP 800-161r1. Together, these shifts move organizations from Tier 2 “Risk Informed” to Tier 3 “Repeatable” maturity, grounded in the CSF 2.0 PR.DS outcome text on data being managed consistent with organizational risk strategy.

# Slide 15

This slide demonstrates how my entire analysis pipeline is reproducible and transparent. From Week 9, I've containerized the entire environment using Docker: a single command—docker build -t pqcdev . && docker run --rm -v  $(pwd):/work pqcdev—executes the complete analysis. The first step builds a Docker image named "pqcdev" that includes Python 3.11, pandas, and all analysis scripts, eliminating local dependency conflicts. The second step runs the container, mounts the project directory as /work inside, executes the analysis pipeline, and cleans up after itself with the --rm flag. This generates two critical output files: docs/latencybyalgorithm.txt (average execution time in milliseconds by PQC algorithm, evidence for RQ-D1 performance metrics across sectors) and docs/attackratebysector.txt (attack success rate by organizational sector, evidence for RQ-C2 side-channel risk quantification). 
Anyone can run this exact command and produce identical results regardless of their local Python or library versions. This guarantees transparency and scientific rigor in my capstone research.


# Slide 16

This research delivers three layers of impact that extend far beyond academia. 
First, research impact: I've provided empirical evidence for PQC deployment across Finance, Healthcare, and IoT—three critical sectors that currently lack consensus on algorithm selection, performance baselines, and governance alignment. This fills a documented gap and delivers a CSF 2.0-aligned migration 
roadmap. 
Second, organizational value: my findings offer sector-specific algorithm recommendations (Kyber sub-30ms for Finance; SPHINCS for Healthcare archival), a risk-managed transition playbook (phased rollout, parallel crypto stacks, rollback procedures), a standards compliance framework (CSF 2.0 Current→Target Profile integration), and a metrics-driven governance model (Risk→Requirement→Metric→Evidence traceability). Third, scalability: this reproducible methodology—accessible via the GitHub repository—enables adoption by CISA and NSA for quantum readiness initiatives, private organizations managing their PQC transitions, and government agencies aligning with NIST standards. My next steps are ambitious but achievable: expand the qualitative cohort – more interviews. Review more research papers, publish findings in peer-reviewed venues (IEEE, ACM, NIST Journal), and contribute through blogs , articles related to PQC.The full repository at github.com/ibhandari072021/PostQuantumCryptography contains all artifacts and the reproducible pipeline.

# Slide 17

Github repo. Docs/pitch and Readme.md updated

# Slide 18

References

# slide 19

Thank you.