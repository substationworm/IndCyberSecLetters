![](IndCyberSecLetters-Header.png "IndCyberSec. Letters")

# 📰 Issue 05: The State of ICS/OT Cybersecurity in 2024 According to the SANS Institute

The [SANS 2024 Industrial Control Systems/Operational Technology (ICS/OT) Survey: The State of ICS/OT Cybersecurity](https://www.sans.org/white-papers/sans-2024-state-ics-ot-cybersecurity/), authored by [Jason D. Christopher](https://www.linkedin.com/in/jdchristopher/), was published on October 9, 2024. Based on responses from 530 professionals in the critical infrastructure sector, the report consolidates statistical data, trends, and insights into cyber threats, providing a valuable resource for asset owners and operators responsible for ICS/OT security.

Additionally, this issue highlights notes on open-source intelligence (OSINT) that connect to key findings from the SANS Institute report. This edition of the [Ind.Cyber.Sec Letters](https://github.com/substationworm/IndCyberSecLetters/tree/main) is structured around the main conclusions of the survey, organized as follows:

- [Respondent Profiles](#-respondent-profiles).
- [Challenges, Threats, and Risks](#-challenges-threats-and-risks).
- [Cyber Defense](#-cyber-defense).
- [Cloud Services and Artificial Intelligence](#-cloud-services-and-artificial-intelligence).
- [Notes on OSINT](#-notes-on-osint).

## 📊 Respondent Profiles

- 36% of survey participants reported being responsible for the security of both information technology (IT) and OT infrastructures.
- The division between IT and OT is also reflected in team distribution: 34% of respondents focus exclusively on ICS/OT security, while 24% concentrate primarily on IT security.
- Approximately 50% of ICS security professionals have five years or less of experience in the field. This highlights the importance of workplace mentoring to foster knowledge transfer between experienced professionals and newcomers.
    - 👨‍🎓 Notably, 48.7% of these professionals lack cybersecurity certifications, which could undermine the effectiveness of implemented protection measures, resulting in less resilient ICS environments.
    - Conversely, 24.1% of respondents report having between six and ten years of experience.

## 💀 Challenges, Threats, and Risks

- 🚨 One of the primary challenges reported by respondents (65%) is the integration of legacy ICS/OT systems with modern IT environments.
- 🚨 Half of the respondents indicated a lack of understanding among IT teams regarding the specific operational nuances of ICS/OT environments.
- 🚨 66% of participants identified "individuals" (employees and contractors) as the primary risk to OT assets. However, only 25% allocate resources to training, recruitment, and retention of human resources.
- 🚨 Approximately 28% of respondents do not have an incident response plan (IRP) specific to ICS assets.
- 💸 Only 11.7% of respondents reported ransomware incidents in the past 12 months. Of these cases:
    - 38.1% affected IT networks only.
    - 28.6% impacted OT/ICS networks exclusively.
    - 21.4% involved both IT and OT/ICS networks.
- ⚔️ The primary initial attack vectors in OT/ICS systems were as follows:
    - 🗡️ Compromise in IT that allowed threats to move into IT/OT networks (45.8%). <a name="compromised-it-systems"></a>
    - 🗡️ External remote services (23.7%).
    - 🗡️ Internet-accessible devices (23.7%).
    - 🗡️ Compromised removable media (20.3%).
    - 🗡️ Supply chain compromise (20.3%).
- ⚰️ 22% of organizations have ICS/OT technologies configured as dual-homed with IT systems or directly integrated into enterprise networks.

## 🏰 Cyber Defense

- 72% of organizations ensure their ICS adhere to established frameworks:
    - 🏅[45%] [National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF)](https://www.nist.gov/cyberframework).
    - 🏅 [International Society of Automation (ISA)/IEC 62443](https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards).
    - 🏅 [North American Electric Reliability Corporation (NERC) - Critical Infrastructure Protection (CIP)](https://www.nerc.com/pa/Stand/Pages/ReliabilityStandards.aspx).
- Defensible architecture, with a focus on perimeter defenses, is the top priority for financial resource allocation (33.1%), followed by initiatives targeting ICS/OT visibility and monitoring (22.9%), incident response (21.4%), secure remote access (12.9%), and vulnerability-based risk management (9.1%).
    - 🚀 Incident detection typically occurs relatively quickly, often within 24 hours.
    - 🚔 Incident response requires greater attention from organizations, as advanced detection capabilities may have limited utility without an effective response plan.
    - 🚔 The more frequently an IRP is tested, the better teams are prepared to manage real-world incidents. Among the 75% of respondents who conducted quarterly tests simulating ICS network outages, 72% expressed confidence in their ability to operate systems manually during such events.
    - 🧱 "Network protections, including boundary protection," is identified as the highest priority for defensible architecture by 55.6% of respondents, with 23.2% and 15.1% ranking it as their second and third priorities, respectively. This aligns with the attribution of [IT system compromises](#compromised-it-systems) as the primary initial attack vector in 2024.
- From a strategic priorities perspective, the security of industrial processes is the primary concern for 36.4% of organizations, followed by the confidentiality of intellectual property (22.4%) and the prevention of financial losses (13.6%).
- The five main technologies used for ICS security in 2024, according to the [survey](https://www.sans.org/white-papers/sans-2024-state-ics-ot-cybersecurity/), are:
    - 1️⃣ Access controls (81.3%).
    - 2️⃣ Backup and recovery processes and tools (74.4%).
    - 3️⃣ Endpoint detection and response (EDR), including traditional antivirus (73.3%).
    - 4️⃣ Segmentation between control systems and higher risk networks (66.3%).
    - 5️⃣ Secure remote access with multifactor authentication (64.8%).
- 🛡️ 62.7% of organizations have a security operations center (SOC), with 29.4% notably having a SOC responsible for both IT and OT environments.
    - 👍 70% of organizations collect and correlate data from ICS asset servers running commercial operating systems such as Windows, Unix, or Linux.
    - 👍 63.9% collect and correlate data from ICS network devices, including firewalls, switches, routers, gateways, and others.
    - 👍56% of organizations utilize ICS-specific threat intelligence, primarily sourced from vendors (79%).
    - 👎 Conversely, 27.7% of organizations lack a SOC, and, alarmingly, 12% have no capability to monitor their ICS/OT networks.
- 🕹️ 62.1% of organizations have a formal policy for remote access to ICS/OT systems, while 22% operate with an informal program, and 15.9% lack such a policy or are unaware of its existence. Key capabilities developed to protect remote access include:
    - 1️⃣ Enforcement of multifactor authentication.
    - 2️⃣ Use of a jump box to establish secure pathways
    - 3️⃣ Logging of remote sessions.
    - 4️⃣ Ability to terminate suspicious or anomalous remote access.
    - 5️⃣ Regular review of all users with remote access privileges.
- 📋 74.9% of respondents reported that an assessment of ICS/OT cybersecurity was conducted within the past 12 months.
- 👀 51.7% indicated continuous monitoring for vulnerabilities, while 46.6% reported the use of passive network monitoring.

## 🤖 Cloud Services and Artificial Intelligence

- The use of artificial intelligence (AI) is still emerging, with only 19% of organizations employing this technology in both IT and OT networks. Additionally, 19% of respondents are in the testing phases, while 27% limit the application of AI exclusively to IT networks.
- ☁️ 39% of organizations use cloud-based services, while 45% avoid them due to concerns about security and reliability.
    - In the energy sector, in particular, there is a notable absence of cloud solutions, with only 18% of organizations adopting this technology. This situation is primarily attributed to regulatory uncertainties associated with standards such as NERC-CIP.
    - 31.6% of organizations implement remote control of engineering operations through cloud-integrated human-machine interface (HMI) systems.
    - As of 2024, the use of cloud services is predominantly limited to configuration monitoring or operational telemetry analysis, a practice reported by 55.8% of respondents.

## 🌐 Notes on OSINT

> [!CAUTION]
> 66% of respondents identified "individuals" (employees and contractors) as the primary risk to ICS/OT systems.
    - 🕵️ Social media intelligence (SOCMINT).
        - 🗃️ Sharing sensitive information on platforms such as LinkedIn or Reddit can lead to the compromise of ICS/OT assets (**oversharing**).
        - 🗃️ Information disclosed by individuals on social media can be weaponized against them through social engineering techniques.
    - 🪪 Open-source or scraped usernames and email addresses can be leveraged for mass phishing, spearphishing campaigns, or other techniques, such as password spraying.
        - 🔎 Analyzing email formats and domains can enable adversaries to infer employee, contractor, or vendor contact details based on full names.
        - 🔎 Weak passwords and password reuse, when combined with harvested email addresses, may facilitate unauthorized access to IT/OT systems. This risk has been highlighted in [Issue 04: Weak Passwords and Poor Security Practices Persist After Six Years of NordPass Research](https://github.com/substationworm/IndCyberSecLetters/blob/main/2024/Issue04/Issue04.md).
        - 🔎 Threat actors can determine whether an email address has been involved in data breaches or if associated passwords have been compromised, using tools like [haveibeenpwned.com](https://haveibeenpwned.com/), for example.

> [!CAUTION]
> 22% of organizations operate with informal programs for remote access to ICS/OT systems, while 15.9% either lack such policies or are unaware of their existence.
    - 🔓 Internet-exposed ICS/OT assets accessible via specialized search engines, such as [Shodan.io](https://www.shodan.io/), can reveal user account details or facilitate unauthorized access, particularly in environments with poor security practices.
    - 🐛 The identification of equipment associated with an organization's IT/OT infrastructure enables malicious actors to search for known vulnerabilities tied to specific vendors or products. For instance, as of the publication date of this issue, the [ICS Advisory Project (ICS[AP])](https://www.icsadvisoryproject.com/) lists 3,087 Cybersecurity & Infrastructure Security Agency (CISA) ICS advisories, covering 582 vendors and 2,381 products.

## 📚 References

- Christopher, J. D. (2024). *SANS 2024 State of ICS/OT Cybersecurity*. SANS Institute. [Link](https://www.sans.org/white-papers/sans-2024-state-ics-ot-cybersecurity/)

**🔖 Nomenclature**

- AI: Artificial intelligence.
- EDR: Endpoint detection and response.
- HMI: Human-machine interface.
- ICS: Industrial control system.
- IRP: Incident response plan.
- IT: Information technology.
- OSINT: Open-source intelligence.
- OT: Operational technology.
- SOC: Security operations center.
- SOCMINT: Social media intelligence.

---

*Ind.Cyber.Sec Letters* . Issue 05 . 2024-12-18

[Prof. Dr. Luiz F. Freitas-Gutierres](https://www.linkedin.com/in/lffreitas-gutierres/)