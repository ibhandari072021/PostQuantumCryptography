One key supplier/tool/data dependency for this project is the open-source implementation libraries of the post-quantum cryptography (PQC) algorithms Kyber, Dilithium, and SPHINCS+. These libraries are critical for performance testing and side-channel attack experiments. The specific risk to manage is dependency vulnerability, including timely updates, patch management, and ensuring the provenance of the source code to avoid tampering or unintentional inclusion of insecure code.




2.3.3. Level 2 — Mission and Business Process

Exact Text from page no 243 (NIST SP 800-161r1-upd1)
“Level 2 addresses how the enterprise mission and business processes assess, respond to, and monitor cybersecurity risks throughout the supply chain. Level 2 activities are performed in accordance with the C-SCRM strategy and policies provided by Level 1.22 22 For more information, see Section 2.2 in [SP80039]. In this level, process specific C-SCRM strategies, policies, and implementation plans dictate how the enterprise’s CSCRM goals and requirements are met within each mission and business process. Here, specific C-SCRM program requirements are defined and managed and include cost, schedule, performance, security, and a variety of critical non-functional requirements. These nonfunctional requirements include concepts such as reliability, dependability, safety, security, and quality.
Level 2 roles include representatives of each mission and business process, such as program managers, research and development, and acquisitions/procurement. Level 2 C-SCRM activities address C-SCRM within the context of the enterprise’s mission and business process. Specific strategies, policies, and procedures should be developed to tailor the C-SCRM implementation to fit the specific requirements of each mission and business process. In order to further develop the high-level Enterprise Strategy and Implementation Plan, different mission areas or business lines within the enterprise may need to generate their own tailored mission and business-level strategy and implementation plan, and they should ensure that C-SCRM execution occurs within the constraints defined by higher-level C-SCRM strategies and in conformance C-SCRM policies. To facilitate the development and execution of Level 2 Strategy and Implementation plans, enterprises may benefit from forming a committee with representation from each mission and business process. Coordination and collaboration between the mission and business processes can help drive risk awareness, identify cybersecurity risks throughout the supply chain, and support the development of an enterprise and C-SCRM architecture. A C-SCRM PMO may also assist in the implementation of C-SCRM at Level 2 through the provision of services (e.g., policy templates, C-SCRM subject matter expert [SME] support) ….. “

Mitigations to Implement

1.	Verify third-party software versions: Ensure that all library or tool versions are documented with checksums stored securely in the project’s SBOM (Software Bill of Materials). This helps detect tampering or unapproved changes before use.
2.	Maintain detailed supplier/source documentation: Record the source, licensing, and update histories of all dependencies in a configuration management file (dependency_tracking.md), making sure that updates and patches are tracked and vulnerabilities are managed proactively.
Evidence Location in Repository:

•	SBOM file: SBOM.txt in  cSRM\SBOM.txt
•	Dependency documentation: cSRM\dependency_tracking.md
This implementation aligns with NIST guidance by managing third-party dependencies at the mission and business process level to mitigate risks from vulnerabilities or tampering, ensuring trusted and secure development environments.
