# OpenVAS (Greenbone) – Vulnerability Assessment

## Role in VAPT
OpenVAS is used for automated vulnerability discovery across network services and operating systems.


## Skills Demonstrated
- Vulnerability Assessment & Penetration Testing (VAPT)
- CVE Analysis & CVSS Risk Scoring
- Vulnerability Validation
- Risk-Based Remediation & Reporting


## Assessment Approach

### Scan Configuration
- Targeted scans per zone
- Safe checks enabled
- Authenticated scans avoided to reflect black-box testing


## Vulnerability Analysis
- Each finding is mapped to a CVE
- CVSS scores are reviewed, not blindly trusted
- High and Critical findings are manually validated


## False Positive Reduction
- Services verified via Nmap and manual checks
- Non-exploitable findings documented as informational


## Output Handling
- Reports are summarized
- Only validated findings are included in final report
- Raw scanner output is never submitted as-is


## Professional Note
OpenVAS is a discovery tool, not a decision-maker.
Manual validation is mandatory before exploitation.
