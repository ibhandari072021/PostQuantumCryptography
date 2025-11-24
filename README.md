# PostQuantumCryptography
PostQuantumCryptography

ETHICS.md - (summary of A–E + control mapping references)

/docs/privacy_program_plan.md - Privacy program plan

/logs/account_management_audit.log - Account management logs, access approval records, and periodic audit reports 

/docs/access_control_policy.md - Policy details

/logs/policy_review.log - Policy review logs

/docs/audit_review.md- Periodic audit review notes capturing compliance checks, risk analyses, and corrective actions 


# Dependency Verification

Each PQC library version used in this project is pinned and verified via checksum against the official repository.  
Checksums are recorded in SBOM.txt for audit purposes.  

Update Process:  
1. Fetch updated library code or binaries from official source.  
2. Verify checksum matches authorized version.  
3. Update SBOM.txt and document changes in CHANGELOG.md.  
4. Notify governance board via docs/cscrm_note.md of dependency update status.


# Standards Note:
See docs/crosswalk.md for the crosswalk table. This capstone project aligns with CSF Outcomes PR.DS-01, PR.AA-03, PR.PS-04 and Zero Trust tenets “all are resources,” “dynamic/auth enforced,” “continuous info collection.” Audit log files and code comments in each module serve as evidence of compliance.


# SMART Metrics (with pointers):

Source Coverage Ratio: See docs/source_count.csv after each literature review.

Reference Freshness Score: See docs/source_log.csv (auto-calculated annually/quarterly).

Peer Review Validation %: See docs/peerreview_log.txt (updated post-review cycle).

Privacy Incident Rate: Run src/paramleak_check.py; results in logs/test_output.log.

De-ID Enforcement Ratio: See docs/data_deid.log after each new dataset run.

Secure Storage Compliance: Run src/storage_policy_check.py; results in logs/storage_output.log.

# Traceability Matrix:

See docs/traceability_matrix.pdf for the mapping of project risks to controls, metrics, and evidence.

Referenced Requirements/Assessment Statements:

SP 800-171 Requirement IDs: 03.03.01,03.01.02, 03.05.01, 03.02.01, 03.02.03, 03.08.02, 03.13.01, 03.13.02, 03.01.07, 03.04.03

SP 800-171A Assessment Statement ID: A.03.03.01.a