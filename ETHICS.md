Ethics & Constraints Brief

Data & People

This research primarily handles cryptographic algorithm specifications, synthetic data generated for cryptanalysis/testing, and publicly available text artifacts related to cryptographic protocols. No human-sourced text containing PII will be collected; any human-sourced content used will be confined to role-play or public artifact text strictly without PII.

Risks

•	Limited research availability in this area may introduce bias and lead to incorrect experimental results, as findings are largely based on reviewed papers rather than direct experimentation.
•	Reliance on reviewed papers, which may contain errors or outdated information, increases the risk of propagating incorrect assumptions or conclusions in the research.
•	Privacy exposure due to accidental leakage of sensitive cryptographic parameters or related metadata.
•	Re-identification risk through linking experimental data with external sources.
•	Over-collection of unnecessary experimental metadata.
•	Dual-us/misuse risk where cryptographic research might be exploited to weaken systems.
•	Unsafe storage or sharing of sensitive cryptographic test data or keys.


Mitigations

•	Bias and Incorrect Results due to Limited Research:
o	Mitigation: Rely on multiple peer-reviewed papers and authoritative reviews. Cross-verify findings and clearly document sources to mitigate bias and inaccuracies, with transparent citation practices.
•	Inability to Fully Test Due to Lack of Quantum Infrastructure:
o	Mitigation: Use simulation tools and theoretical analysis from reviewed literature to support findings. Clearly state limitations and assumptions, and avoid overgeneralizing results.
•	Privacy exposure from accidental leakage of cryptographic parameters or metadata:
o	Mitigation: Use de-identification techniques such as pseudonymization, remove or mask sensitive metadata, and store cryptographic parameters in encrypted, access-controlled environments.
•	Re-identification through linking experimental data with external sources:
o	Mitigation: Apply robust anonymization methods such as k-anonymity or differential privacy measures where feasible, and restrict external data linkages.
•	Over-collection of experimental metadata:
o	Mitigation: Practice data minimization, collecting only the metadata essential for analysis and reproducibility, and avoid storing auxiliary information unless necessary.
•	Dual-use/misuse of cryptographic research:
o	Mitigation: Follow responsible disclosure guidelines and restrict sharing of detailed cryptographic methodologies unless approved through institutional reviews.
•	Unsafe storage or sharing of cryptographic test data or keys:
o	Mitigation: Encrypt data in storage and during transfer, implement strict access controls, and maintain audit logs.


Boundaries


•	No collection or use of real production credentials, true personally identifiable information (PII), or protected health information (PHI).
•	No unauthorized scraping or data gathering outside the scope of publicly available cryptographic standards, academic papers, and open research datasets.
•	No acquisition or storage of quantum hardware, real quantum states, or proprietary quantum infrastructure components.
•	No sharing or distribution of sensitive cryptographic keys, operational secrets, or detailed proprietary algorithm implementations outside secure, authorized research contexts
•	The project will not attempt to perform live quantum-based cryptographic experiments due to infrastructure constraints; analysis is limited to simulated, synthetic, and literature-based datasets.
•	No engagement in activities that could intentionally weaken or exploit cryptographic protections contrary to ethical research guidelines

Evidence

•	ETHICS.md summarizing ethical considerations, constraints, and mappings to NIST SP 800-53 Rev. 5 controls.
•	Consent scripts/notices saved in /docs/consent_script.md for any use of role-play or public artifact sourced text.
•	Data anonymization and redaction rules, including pseudonymization regex and masking patterns, documented in /docs/redaction_rules.txt.
•	Access logs and audit trail records (detailed user access, modification timestamps, and data handling logs) maintained in /docs/access_log.md.
•	Privacy program plans and assessment reports, including privacy impact and risk assessments relevant to the research, stored in /docs/privacy_program_plan.md and /assessments/privacy_impact_assessment.pdf.
•	Periodic audit review notes capturing compliance checks, risk analyses, and corrective actions documented in /docs/audit_review.md.

Control Mapping to NIST SP 800-53 Rev.5

AC-1 Access Control- Policy and Procedures (Page 18)

Control Text

Develop, document, and disseminate to [Assignment: organization-defined personnel or roles]: 
1. [Selection (one or more): Organization-level; Mission/business process-level; System-level] access control policy that: 
(a) Addresses purpose, scope, roles, responsibilities, management commitment, coordination among organizational entities, and compliance; and 
(b) Is consistent with applicable laws, executive orders, directives, regulations, policies, standards, and guidelines; and 
2. Procedures to facilitate the implementation of the access control policy and the associated access controls; 
b. Designate an [Assignment: organization-defined official] to manage the development, documentation, and dissemination of the access control policy and procedures; and 
c. Review and update the current access control: 

1. Policy [Assignment: organization-defined frequency] and following [Assignment: organization-defined events]; and 
2. Procedures [Assignment: organization-defined frequency] and following [Assignment: organization-defined events]. 


Mitigation Satisfaction

The documented access control policies and procedures in the project provide a clear framework to control access to sensitive cryptographic research data, ensuring compliance with organizational and legal requirements.

Evidence

Policy documents with revision and dissemination logs maintained in /docs/access_control_policy.md and /logs/policy_review.log.



AC-2 Account Management (Page 19)

Control Text

a. Define and document the types of accounts allowed and specifically prohibited for use within the system;
b. Assign account managers;
c. Require [Assignment: organization-defined prerequisites and criteria] for group and role membership;
d. Specify:
1. Authorized users of the system;
2. Group and role membership; and
3. Access authorizations (i.e., privileges) and [Assignment: organization-defined attributes (as required)] for each account;
e. Require approvals by [Assignment: organization-defined personnel or roles] for requests to create accounts;
f. Create, enable, modify, disable, and remove accounts in accordance with [Assignment: organization-defined policy, procedures, prerequisites, and criteria];
g. Monitor the use of accounts;
h. Notify account managers and [Assignment: organization-defined personnel or roles] within:
1. [Assignment: organization-defined time period] when accounts are no longer required;
2. [Assignment: organization-defined time period] when users are terminated or transferred; and
3. [Assignment: organization-defined time period] when system usage or need-to-know changes for an individual;
i. Authorize access to the system based on:
1. A valid access authorization;
2. Intended system usage; and
3. [Assignment: organization-defined attributes (as required)];
j. Review accounts for compliance with account management requirements [Assignment: organization-defined frequency];
k. Establish and implement a process for changing shared or group account authenticators (if deployed) when individuals are removed from the group; and
l. Align account management processes with personnel termination and transfer processes.
Discussion: Examples of system account types include individual, shared, group, system, guest,

Mitigation Satisfaction

The project enforces strict account management policies including review, monitoring, and least privilege access to ensure only authorized personnel can access sensitive research materials.

Evidence

Account management logs, access approval records, and periodic audit reports in /logs/account_management_audit.log.




PT-1 Personally Identifiable Information Processing and Transparency- Policy and Procedures (Page 256)

Control Text

a. Develop, document, and disseminate to [Assignment: organization-defined personnel or roles]:
1. [Selection (one or more): Organization-level; Mission/business process-level; System-level] personally identifiable information processing and transparency policy that:
(a) Addresses purpose, scope, roles, responsibilities, management commitment, coordination among organizational entities, and compliance; and
(b) Is consistent with applicable laws, executive orders, directives, regulations, policies, standards, and guidelines; and
2. Procedures to facilitate the implementation of the personally identifiable information processing and transparency policy and the associated personally identifiable information processing and transparency controls;
b. Designate an [Assignment: organization-defined official] to manage the development, documentation, and dissemination of the personally identifiable information processing and transparency policy and procedures; and
c. Review and update the current personally identifiable information processing and transparency:
1. Policy [Assignment: organization-defined frequency] and following [Assignment: organization-defined events]; and
2. Procedures [Assignment: organization-defined frequency] and following [Assignment: organization-defined events].

Mitigation Satisfaction

Having a formal privacy program plan ensures the study has documented responsibilities, scope, and compliance measures for privacy and data protection consistent with legal and organizational expectations.

Evidence

Privacy program plan document and update records stored in /docs/privacy_program_plan.md and related audit logs.
