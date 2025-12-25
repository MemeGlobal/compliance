# Knowledge Base Updates — extracted from `compliance.yml` and Publisher Questionnaire

This file contains **paste-ready Confluence table rows** (Option B) extracted from `compliance.yml` and the Publisher Questionnaire, using tags from `controlled_tag_taxonomy.md`.

## Confluence table header

| ID | Statement | Tags | Status | Source | Notes |
| --- | --- | --- | --- | --- | --- |

## Rows

| 1 | Built-in playback for article content is provided in all plans. | tts, application | implemented | compliance.yml — requirement 1.01 |  |
| 2 | The embedded player provides standard transport controls (play, pause, stop, fast forward). | tts, user-experience, user-interface | implemented | compliance.yml — requirement 1.02 |  |
| 3 | Users are not redirected to a new page or external player. | tts, user-experience | implemented | compliance.yml — requirement 1.02; compliance.yml — requirement 1.03 |  |
| 4 | Multi-language playback is supported. | tts, compatibility | implemented | compliance.yml — requirement 1.04 |  |
| 5 | Translating a story counts as a credit. | billing, tts | implemented | compliance.yml — requirement 1.04 |  |
| 6 | The player is compatible across mobile platforms. | tts, mobile, compatibility | implemented | compliance.yml — requirement 1.05 |  |
| 7 | High-quality voices are available. | tts, user-experience | implemented | compliance.yml — requirement 1.06 |  |
| 8 | Cloned and GenAI voices start at the Publisher plan tier. | billing, tts | implemented | compliance.yml — requirement 1.06 |  |

| 9 | The player conforms to WCAG 2.1 AA. | accessibility, user-interface, wcag | implemented | compliance.yml — requirement 2.01 |  |
| 10 | The player conforms to Section 508. | accessibility, user-interface, section-508 | implemented | compliance.yml — requirement 2.01 |  |
| 11 | The player has been independently verified via VPAT v2.4 (Oct 19, 2023). | accessibility, vpat | implemented | compliance.yml — requirement 2.01 |  |
| 12 | The player supports screen readers (JAWS and VoiceOver). | accessibility, screen-reader-support, user-interface | implemented | compliance.yml — requirement 2.01; 2.03 |  |
| 13 | The player supports full keyboard navigation. | accessibility, keyboard-navigation, user-interface | implemented | compliance.yml — requirement 2.01; 2.02 |  |
| 14 | The player provides visible focus indicators. | accessibility, user-interface, focus-indicators | implemented | compliance.yml — requirement 2.01; 2.02 |  |
| 15 | The player provides high-contrast elements. | accessibility, user-interface, high-contrast | implemented | compliance.yml — requirement 2.01 |  |
| 16 | The player provides ARIA-labeled controls. | accessibility, user-interface, aria | implemented | compliance.yml — requirement 2.01; 2.03 |  |
| 17 | Accessibility is periodically retested with aXe and Lighthouse. | accessibility, accessibility-testing | implemented | compliance.yml — requirement 2.01 | Tool names appear in source evidence; tags remain taxonomy-controlled. |
| 18 | The player supports keyboard operation using Tab, Enter, and Space. | accessibility, keyboard-navigation, user-interface | implemented | compliance.yml — requirement 2.02 |  |
| 19 | The player provides proper Name/Role/Value via WAI-ARIA. | accessibility, aria, user-interface | implemented | compliance.yml — requirement 2.03 |  |
| 20 | End users can change playback speed. | accessibility, user-experience, user-interface | implemented | compliance.yml — requirement 2.04 |  |
| 21 | End users cannot change voice pitch. | tts, user-experience, user-interface | not-implemented | compliance.yml — requirement 2.04 | Evidence says voice pitch is not configurable by end users. |
| 22 | Voice pitch is configurable by the client/admin. | tts, user-experience | implemented | compliance.yml — requirement 2.04 |  |
| 23 | Background playback is supported. | tts, user-experience, mobile | implemented | compliance.yml — requirement 2.05 |  |

| 24 | The platform integrates wherever a small JavaScript snippet can be added. | integration, script-embed, application | implemented | compliance.yml — requirement 3.01 |  |
| 25 | For CrownPeak, integration requires the ability to inject code in the global header/footer or a template include. | integration, cms, script-embed | implemented | compliance.yml — requirement 3.01 |  |
| 26 | The player script loads asynchronously. | performance, async-loading, frontend | implemented | compliance.yml — requirement 3.02 |  |
| 27 | The player script is less than 50 KB gzipped. | performance, frontend | implemented | compliance.yml — requirement 3.02 |  |
| 28 | The player script does not block rendering. | performance, async-loading, frontend | implemented | compliance.yml — requirement 3.02 |  |
| 29 | The player script does not impact Core Web Vitals. | performance, frontend | implemented | compliance.yml — requirement 3.02 |  |
| 30 | Audio processing is handled on cloud infrastructure. | cloud, infrastructure, tts | implemented | compliance.yml — requirement 3.02 |  |
| 31 | The player element is hidden if the script fails to load. | user-experience, graceful-degradation, frontend | implemented | compliance.yml — requirement 3.03 |  |
| 32 | The player element is hidden if the Web Audio API is unsupported. | compatibility, graceful-degradation, frontend | implemented | compliance.yml — requirement 3.03 |  |
| 33 | The page remains stable and readable when TTS fails to load. | user-experience, graceful-degradation, frontend | implemented | compliance.yml — requirement 3.03 |  |

| 34 | Player controls clearly indicate when audio is available. | user-experience, user-interface, tts | implemented | compliance.yml — requirement 4.01 |  |
| 35 | Users can enable or disable playback for a session. | user-experience, user-interface, tts | implemented | compliance.yml — requirement 4.02 |  |
| 36 | The embedded player is non-intrusive. | user-experience, user-interface, tts | implemented | compliance.yml — requirement 4.03 |  |
| 37 | The embedded player coexists with other page components. | user-experience, user-interface, tts | implemented | compliance.yml — requirement 4.03 |  |
| 38 | The UI is optimized for mobile. | user-experience, user-interface, mobile | implemented | compliance.yml — requirement 4.04 |  |
| 39 | The player provides a “Play Text” action. | user-experience, user-interface, tts | implemented | compliance.yml — requirement 4.05 |  |
| 40 | Text highlighting is synchronized with audio. | user-experience, user-interface, tts | implemented | compliance.yml — requirement 4.05 |  |

| 41 | The platform provides RESTful APIs with JSON over HTTPS. | api, encryption, encryption-in-transit | implemented | compliance.yml — requirement 5.01 |  |
| 42 | SOAP is not supported. | compatibility, api | not-implemented | compliance.yml — requirement 5.01 | Evidence says SOAP is not supported. |
| 43 | Atom is not supported. | compatibility, api | not-implemented | compliance.yml — requirement 5.01 | Evidence says Atom is not supported. |

| 44 | APIs use OAuth2/Bearer tokens for authentication. | api, authentication, oauth2 | implemented | compliance.yml — requirement 5.02 |  |
| 45 | Role-based access control is enforced for APIs. | api, authorization, rbac | implemented | compliance.yml — requirement 5.02 |  |
| 46 | API rate limits are enforced. | api, performance, rate-limiting | implemented | compliance.yml — requirement 5.02 | Evidence says enforced rate limits. |
| 47 | API quota limits are enforced. | api, performance, quotas | implemented | compliance.yml — requirement 5.02 | Evidence says quotas are enforced. |
| 48 | API monitoring with alerts for anomalies is in place. | api, monitoring, detective | implemented | compliance.yml — requirement 5.02 |  |


| 51 | The platform is hosted as a fully managed SaaS. | deployment, cloud | implemented | compliance.yml — requirement 5.04 |  |
| 52 | The platform is hosted in AWS across multiple regions. | deployment, cloud, multi-region | implemented | compliance.yml — requirement 5.04 | Vendor name appears in source evidence; tags remain taxonomy-controlled. |
| 53 | On-premise deployment is not offered. | deployment | out-of-scope | compliance.yml — requirement 5.04 | Evidence says on-premise is not offered. |

| 54 | CI/CD uses immutable version tags. | ci-cd, deployment, immutable-versioning | implemented | compliance.yml — requirement 5.05 |  |
| 55 | Automated rollback typically completes within minutes. | ci-cd, deployment | implemented | compliance.yml — requirement 5.05 |  |

| 56 | Hosted script updates are applied automatically. | deployment, integration, script-embed | implemented | compliance.yml — requirement 5.06 |  |
| 57 | CMS plugins update via standard admin flows. | deployment, cms, integration | implemented | compliance.yml — requirement 5.06 |  |
| 58 | Updates are backward-compatible. | compatibility, backward-compatibility | implemented | compliance.yml — requirement 5.06 |  |
| 59 | Updates are pre-tested. | secure-development, pre-testing | implemented | compliance.yml — requirement 5.06 |  |

| 60 | The platform uses multi-region redundancy. | cloud, disaster-recovery, multi-region | implemented | compliance.yml — requirement 5.07 |  |
| 61 | Load balancing is used. | cloud, scalability, load-balancing | implemented | compliance.yml — requirement 5.07 |  |
| 62 | Auto-scaling is used. | cloud, scalability, autoscaling | implemented | compliance.yml — requirement 5.07 |  |
| 63 | Daily automated backups are performed. | backup, backup-restore, cloud | implemented | compliance.yml — requirement 5.07 |  |
| 64 | Distributed failover is supported. | cloud, disaster-recovery | implemented | compliance.yml — requirement 5.07 |  |
| 66 | IAM isolation is used. | access-control, cloud, preventive | implemented | compliance.yml — requirement 5.07 | Evidence says IAM isolation. |
| 68 | The uptime SLA is 99.9%. | availability | implemented | compliance.yml — requirement 5.07 | Evidence says 99.9% uptime SLA. |

| 69 | Ready-to-use snippets and plugins are available for WordPress, Wix, and Webflow. | integration, cms | implemented | compliance.yml — requirement 5.08 | Vendor/product names appear in source evidence; tags remain taxonomy-controlled. |
| 70 | For CrownPeak/AEM, integration is performed via a single JavaScript snippet in the global template. | integration, cms, script-embed | implemented | compliance.yml — requirement 5.08 |  |

| 71 | The admin dashboard provides usage metrics. | analytics, dashboard | implemented | compliance.yml — requirement 6.01 |  |
| 72 | The admin dashboard provides analytics. | analytics, dashboard | implemented | compliance.yml — requirement 6.01 |  |
| 73 | Integration with Google Analytics is supported. | analytics, integration | implemented | compliance.yml — requirement 6.02 | Vendor name appears in source evidence; tags remain taxonomy-controlled. |

| 75 | Sensitive data is encrypted in transit using TLS 1.2+. | encryption, encryption-in-transit, network | implemented | compliance.yml — requirement 7.01 |  |
| 76 | No local device caching is used. | privacy, data-retention, endpoint | implemented | compliance.yml — requirement 7.01 | Evidence says no local device caching. |
| 77 | Database access is restricted via IAM and VPC policies. | access-control, database, cloud, preventive | implemented | compliance.yml — requirement 7.01 |  |

| 78 | TLS 1.2+ is enforced across clients, APIs, and servers. | encryption, encryption-in-transit, network | implemented | compliance.yml — requirement 5.03; compliance.yml — requirement 7.02 |  |
| 79 | Legacy protocols are disabled. | encryption, encryption-in-transit | implemented | compliance.yml — requirement 5.03; compliance.yml — requirement 7.02 |  |

| 80 | Only HTTPS (443) is exposed externally. | network, preventive | implemented | compliance.yml — requirement 7.03 |  |
| 81 | Security groups and NACLs block non-essential ports. | network, preventive | implemented | compliance.yml — requirement 7.03 |  |

| 82 | The platform uses a multi-tier architecture with segregated subnets for web/API, application, and database. | infrastructure, network, preventive | implemented | compliance.yml — requirement 7.04 |  |
| 83 | An AWS Load Balancer and WAF protect the platform. | network, preventive | implemented | compliance.yml — requirement 7.04 | Vendor/tool names appear in source evidence; tags remain taxonomy-controlled. |

| 84 | Okta 2.0 SSO compatibility and MFA for the admin dashboard are not currently supported as described. | authentication, identity, sso, mfa | not-implemented | compliance.yml — requirement 7.05 |  |

| 85 | The platform supports two user roles: Account Owner and Standard User. | authorization, rbac, application | implemented | compliance.yml — requirement 7.06 |  |
| 86 | Content-level access restrictions are supported. | access-control, authorization, application | implemented | compliance.yml — requirement 7.06 |  |

| 87 | AWS-native controls (IAM, WAF, CloudTrail, GuardDuty) are used for intrusion detection and continuous monitoring. | monitoring, cloud, detective | implemented | compliance.yml — requirement 7.07 | Vendor/tool names appear in source evidence; tags remain taxonomy-controlled. |
| 88 | Least-privilege access is used. | access-control, preventive | implemented | compliance.yml — requirement 7.07 |  |
| 89 | Routine audits are performed. | access-review, detective | implemented | compliance.yml — requirement 7.07 | Evidence says routine audits. |

| 90 | Authentication is performed via secure API tokens or SSO (SAML 2.0). | authentication, identity, api, sso, saml | implemented | compliance.yml — requirement 7.08 |  |
| 91 | All access is logged and audited. | logging, audit-logging, detective | implemented | compliance.yml — requirement 7.08 |  |
| 92 | Data is stored in encrypted databases within private VPC subnets. | encryption, encryption-at-rest, database, cloud | implemented | compliance.yml — requirement 7.08 |  |
| 93 | Mutual TLS is used between microservices. | encryption, encryption-in-transit, infrastructure, network | implemented | compliance.yml — requirement 7.08 |  |
| 94 | CI/CD includes vulnerability scanning prior to deployment. | ci-cd, vulnerability-management, secure-development | implemented | compliance.yml — requirement 7.08 |  |
| 95 | CI/CD includes dependency checks prior to deployment. | ci-cd, vulnerability-management, secure-development | implemented | compliance.yml — requirement 7.08 | Evidence says dependency checks. |

| 96 | The platform is designed for elastic concurrency. | scalability, concurrency | implemented | compliance.yml — requirement 8.01 |  |
| 97 | Consumer traffic is served via CDN and stateless autoscaling services. | scalability, cdn, autoscaling | implemented | compliance.yml — requirement 8.01 |  |
| 98 | Author and admin traffic runs on separate autoscaling pools. | scalability, autoscaling | implemented | compliance.yml — requirement 8.01 |  |
| 99 | Burst traffic is handled without customer action. | scalability | implemented | compliance.yml — requirement 8.01 |  |

| 100 | CDN edge caching is used for player JS, CSS, and audio streams. | performance, cdn, caching | implemented | compliance.yml — requirement 8.02 |  |
| 101 | Versioned, immutable assets are used. | performance, caching | implemented | compliance.yml — requirement 8.02 |  |
| 102 | ETag and content hashing are used. | performance, caching | implemented | compliance.yml — requirement 8.02 |  |
| 103 | API short-TTL caching is used for read-heavy endpoints. | performance, api, caching | implemented | compliance.yml — requirement 8.02 |  |
| 104 | Static assets use long TTL. | performance, caching | implemented | compliance.yml — requirement 8.02 |  |
| 105 | Sensitive responses are set to no-store. | privacy, data-retention | implemented | compliance.yml — requirement 8.02 | Evidence says sensitive responses set no-store. |

| 106 | Runtime tiers are stateless clusters behind load balancers. | scalability, load-balancing | implemented | compliance.yml — requirement 8.03 |  |
| 107 | Data stores use managed services with replicas. | scalability, storage | implemented | compliance.yml — requirement 8.03 |  |
| 108 | Streaming and analytics pipelines are partitioned for horizontal scale. | scalability, analytics | implemented | compliance.yml — requirement 8.03 |  |

| 109 | Multi-AZ clusters behind L7 load balancers are used. | availability, multi-az, load-balancing | implemented | compliance.yml — requirement 8.04 |  |
| 110 | Autoscaling on CPU, QPS, and latency is used. | scalability, autoscaling | implemented | compliance.yml — requirement 8.04 |  |
| 111 | Multi-AZ database replicas are used. | availability, database, multi-az | implemented | compliance.yml — requirement 8.04 |  |
| 112 | Cross-region durable object storage is used. | availability, storage, multi-region | implemented | compliance.yml — requirement 8.04 |  |
| 113 | Asynchronous queues are used for spikes. | scalability | implemented | compliance.yml — requirement 8.04 |  |

| 114 | There is no fixed per-server limit because the player is served from CDN. | scalability, cdn | implemented | compliance.yml — requirement 8.05 |  |
| 115 | Coverage scales to any number of pages. | scalability | implemented | compliance.yml — requirement 8.05 |  |

| 116 | The platform scales horizontally with dynamic instance counts across autoscaling groups and regions. | scalability, autoscaling, multi-region | implemented | compliance.yml — requirement 8.06 |  |
| 117 | Capacity is expanded based on demand and SLOs. | scalability | implemented | compliance.yml — requirement 8.06 |  |

| 118 | The player and integrations are HTML5-compliant. | compatibility, html5, frontend | implemented | compliance.yml — requirement 9.01 |  |
| 119 | Compatibility covers the current and two prior versions of major browsers. | compatibility, browser-support, browser | implemented | compliance.yml — requirement 9.02 |  |
| 120 | Web-based delivery supports laptops, PCs, tablets, and smartphones. | compatibility, endpoint | implemented | compliance.yml — requirement 9.03 |  |
| 121 | The admin UX supports concurrent multi-tab and multi-page workflows. | user-experience, dashboard | implemented | compliance.yml — requirement 9.04 |  |
| 122 | The platform supports at least 50 simultaneous active listeners. | scalability, concurrency | implemented | compliance.yml — requirement 9.05 |  |
| 123 | Concurrency is defined as simultaneous active listeners. | scalability | implemented | compliance.yml — requirement 9.05 |  |
| 124 | The system is engineered for low-latency interactions. | performance, low-latency | implemented | compliance.yml — requirement 9.06 |  |

| 125 | Trinity headquarters are located in Israel. | infrastructure | implemented | Publisher Questionnaire — Question 1 |  |
| 126 | AWS (US/EU) is used for cloud storage. | cloud, storage | implemented | Publisher Questionnaire — Question 1 |  |
| 127 | BunnyWay d.o.o (EU) is used for CDN services. | cdn, cloud | implemented | Publisher Questionnaire — Question 1 |  |
| 128 | IP addresses are processed and stored. | personal-data, privacy, storage | implemented | Publisher Questionnaire — Question 2; Question 7 |  |
| 129 | User-agent information is processed and stored. | personal-data, privacy, storage | implemented | Publisher Questionnaire — Question 2; Question 7 |  |
| 130 | User actions in the player are processed and stored. | personal-data, privacy, analytics, storage | implemented | Publisher Questionnaire — Question 2; Question 7 |  |
| 131 | Approximate location at country/state/city level is processed. | personal-data, privacy | implemented | Publisher Questionnaire — Question 2 |  |
| 132 | Consent string is processed. | personal-data, privacy | implemented | Publisher Questionnaire — Question 2 |  |
| 133 | UUID (Trinity's unique identifier assigned to a cookie) is processed. | personal-data, privacy | implemented | Publisher Questionnaire — Question 2 |  |
| 134 | Cookies ID for targeted ads generated by providers such as id5 (as approved through publisher's CMP) are processed. | personal-data, privacy | implemented | Publisher Questionnaire — Question 2 |  |
| 135 | Special categories of data are not processed. | privacy | not-implemented | Publisher Questionnaire — Question 2 |  |
| 136 | Data processed for the purpose of targeted ads (CCBA) are processed as an independent Controller/Third Party and not a Processor/Service Provider. | privacy | implemented | Publisher Questionnaire — Question 2 |  |
| 137 | Publisher data is shared with sub-processors (service providers). | privacy | implemented | Publisher Questionnaire — Question 3 |  |
| 138 | Personal data applicable to monetization is shared with demand partners. | privacy | implemented | Publisher Questionnaire — Question 3 |  |
| 139 | Publisher data is not used for internal commercial purposes other than placement of targeted ads. | privacy | implemented | Publisher Questionnaire — Question 4 |  |
| 140 | Placement of targeted ads is considered as a sale and share under the CCPA and similar US state laws definitions. | privacy | implemented | Publisher Questionnaire — Question 4 |  |
| 141 | Privacy Policies are adopted. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 142 | CCPA Notice is adopted. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 143 | Users Rights Policy is adopted. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 144 | Internal Information Security Policy is adopted. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 145 | Employees' and consultants' data protection undertakings are in place. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 146 | Data Processing Agreement with vendors/service providers and customers is in place. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 147 | Vendor registration and compliance with the IAB TCF program with regards to ads related activities is maintained. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 148 | When processing personal data for the operation of the player and collecting data to provide the publisher with analytics, processing is performed as processor on behalf of the publisher. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 149 | When contextual ads are placed, processing is performed as processor on behalf of the publisher. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 150 | Under the GDPR, both parties are considered controllers with respect to the consent string. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 151 | Under the GDPR, both parties are considered controllers in situations where personalized ads are placed. | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 152 | Under the CCPA, when personalized ads are involved, the publisher is considered as a "business" and the Trinity as a "third party." | privacy | implemented | Publisher Questionnaire — Question 5 |  |
| 153 | Trinity is registered as a Vendor under the IAB TCF. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 154 | IAB TCF signals transmitted through the publisher's CMP are honored. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 155 | Cookies are dropped in accordance with the signal per purpose as settled by the IAB TCF and based on the applicable territory's mechanism. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 156 | Cookies are avoided from loading in accordance with the signal per purpose as settled by the IAB TCF and based on the applicable territory's mechanism. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 157 | Cookies are deleted in accordance with the signal per purpose as settled by the IAB TCF and based on the applicable territory's mechanism. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 158 | Data is collected and shared in accordance with the signal per purpose as settled by the IAB TCF and based on the applicable territory's mechanism. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 159 | Data collection and sharing is avoided in accordance with the signal per purpose as settled by the IAB TCF and based on the applicable territory's mechanism. | privacy | implemented | Publisher Questionnaire — Question 6 |  |
| 160 | Personal data is stored in AWS. | cloud, storage, privacy | implemented | Publisher Questionnaire — Question 7 |  |
| 161 | Data transfer is subject to AWS Standard Contractual Clauses (SCCs) as part of their standard agreements. | privacy | implemented | Publisher Questionnaire — Question 7 |  |
| 162 | AWS is DPF certified. | privacy | implemented | Publisher Questionnaire — Question 7 |  |
| 163 | Personal data is accessed from headquarters in Israel based on adequacy status. | privacy | implemented | Publisher Questionnaire — Question 7 |  |
| 165 | Access to data is restricted consistent with the concept of segregation of duties. | access-control | implemented | Publisher Questionnaire — Question 8 |  |
| 169 | Identified vulnerabilities are remediated in a timely, risk-based manner. | vulnerability-management | implemented | Publisher Questionnaire — Question 8 |  |
| 170 | All manufacturers and developer recommended security updates and patches to operating systems are implemented in a timely manner. | vulnerability-management | implemented | Publisher Questionnaire — Question 8 |  |
| 171 | All manufacturers and developer recommended security updates and patches to third-party software are implemented in a timely manner. | vulnerability-management | implemented | Publisher Questionnaire — Question 8 |  |
| 172 | Penetration testing is conducted on a periodic basis. | vulnerability-management | implemented | Publisher Questionnaire — Question 8 |  |
| 173 | A third party is engaged to perform penetration testing on a periodic basis, usually each 12-18 months. | vulnerability-management | implemented | Publisher Questionnaire — Question 12 |  |
| 174 | Antivirus and malware protection software are implemented with up-to-date definitions. | infrastructure | implemented | Publisher Questionnaire — Question 8 |  |
| 175 | Complex password requirements are enforced. | authentication | implemented | Publisher Questionnaire — Question 8 |  |
| 178 | Secure workstation protection policies are implemented, including locking the system after a defined number of incorrect authentication attempts. | access-control | implemented | Publisher Questionnaire — Question 8 |  |
| 179 | Secure workstation protection policies are implemented, including password-protected screensavers that are activated after a defined period of inactivity. | access-control | implemented | Publisher Questionnaire — Question 8 |  |
| 182 | Access logs are stored for applicable systems. | logging, audit-logging | implemented | Publisher Questionnaire — Question 8 |  |
| 183 | Publisher data is accessed by personnel, provided that access permissions policy is applied based on the concept of need to know. | access-control, privacy | implemented | Publisher Questionnaire — Question 9 |  |
| 184 | Publisher data is accessed by personnel, provided that access permissions policy is applied based on the concept of segregation of duties. | access-control, privacy | implemented | Publisher Questionnaire — Question 9 |  |
| 185 | Segregation is applied for data processed on behalf of each customer. | privacy | implemented | Publisher Questionnaire — Question 9 |  |
| 186 | Data is stored with AWS managed services. | cloud, storage, backup | implemented | Publisher Questionnaire — Question 10; Question 17 |  |
| 187 | Data is subject to AWS disaster recovery. | disaster-recovery, backup, cloud | implemented | Publisher Questionnaire — Question 10; Question 17 |  |
| 188 | Answers and feedback to data security and privacy questionnaires are provided on behalf of clients. | privacy | implemented | Publisher Questionnaire — Question 11 |  |
| 189 | No data breach or data incident involving Personal Information has ever been experienced. | incident-response, privacy | not-implemented | Publisher Questionnaire — Question 13 |  |
| 190 | A structured incident response procedure ensures immediate reporting and escalation of potential incidents. | incident-response | implemented | Publisher Questionnaire — Question 14 |  |
| 191 | Incident response is supported by extensive monitoring. | incident-response, monitoring | implemented | Publisher Questionnaire — Question 14 |  |
| 192 | Incident response process includes prompt containment. | incident-response | implemented | Publisher Questionnaire — Question 14 |  |
| 193 | Incident response process includes investigation of relevant logs. | incident-response, logging | implemented | Publisher Questionnaire — Question 14 |  |
| 194 | Incident response process includes explicit preservation of all evidence. | incident-response | implemented | Publisher Questionnaire — Question 14 |  |
| 195 | If personal data is involved in an incident, legal and privacy counsel are involved to advise on notification obligations. | incident-response, privacy | implemented | Publisher Questionnaire — Question 14 |  |
| 196 | After each incident, processes are reviewed and updated to reduce future risk. | incident-response | implemented | Publisher Questionnaire — Question 14 |  |
| 197 | No inquiries, investigations or legal proceedings regarding data privacy or data protection practices have been submitted to or taken against Trinity. | privacy | not-implemented | Publisher Questionnaire — Question 15 |  |
| 198 | Training programs on data privacy and security are conducted on a periodic basis. | privacy | implemented | Publisher Questionnaire — Question 16 |  |
| 199 | Background screening is made in accordance with applicable laws. | privacy | implemented | Publisher Questionnaire — Question 16 |  |
| 200 | Employees and contractors are subject to confidentiality and compliance with company's policies as part of employment/services agreement. | privacy | implemented | Publisher Questionnaire — Question 16 |  |
| 201 | Cyber insurance is maintained (MADANES insurance). | privacy | implemented | Publisher Questionnaire — Question 18 |  |
| 202 | Trinity has never been Privacy Shield certified. | privacy | not-implemented | Publisher Questionnaire — Question 19 |  |
| 203 | Trinity is not an active participant in the EU-U.S. Data Privacy Framework, the UK Extension, or the Swiss-U.S. Data Privacy Framework. | privacy | not-implemented | Publisher Questionnaire — Question 19 |  |
| 204 | Data is stored in AWS which is DPF certified. | privacy, cloud | implemented | Publisher Questionnaire — Question 19 |  |
| 205 | Data is transferred to the US (AWS) based on the SCCs and DPF, which entitles data subjects with the core rights under the GDPR. | privacy | implemented | Publisher Questionnaire — Question 20.2 |  |
| 206 | Data is transferred to Israel based on adequacy, and the Israeli privacy laws and regulations further provides data subjects with the core rights under the GDPR. | privacy | implemented | Publisher Questionnaire — Question 20.2 |  |
| 207 | Public authorities in both the US and Israel may request access to data in accordance with applicable laws and regulations. | privacy | implemented | Publisher Questionnaire — Question 20.3 |  |
| 208 | In the US, access by public authorities is generally governed by legal processes, such as subpoenas, court orders, or national security requests, and may be subject to judicial oversight. | privacy | implemented | Publisher Questionnaire — Question 20.3 |  |
| 209 | In Israel, access by public authorities is regulated by law, including requirements for due process and, in some cases, court approval. | privacy | implemented | Publisher Questionnaire — Question 20.3 |  |
| 210 | Data subjects may have certain legal remedies available, such as the right to challenge or seek review of disclosure requests, depending on the specific circumstances and applicable law. | privacy | implemented | Publisher Questionnaire — Question 20.3 |  |
| 211 | Trinity has never received a request from public authorities for access to data. | privacy | not-implemented | Publisher Questionnaire — Question 20.4 |  |
| 212 | Given the types of personal data processed and the short retention periods of personal data, the likelihood of receiving such a request is assessed to be low. | privacy | implemented | Publisher Questionnaire — Question 20.4 |  |
| 213 | An independent supervisory authority for data protection matters exists in Israel (Israeli Protection of Privacy Authority). | privacy | implemented | Publisher Questionnaire — Question 20.5 |  |
| 214 | In the US, in some states the AGs regulate privacy matters. | privacy | implemented | Publisher Questionnaire — Question 20.5 |  |
| 215 | The laws of the jurisdiction do not impose obligations that conflict with the data importer's rights and obligations under the standard contractual clauses. | privacy | implemented | Publisher Questionnaire — Question 20.6 |  |
| 216 | Trinity has never been asked to provide personal data to a public authority for reasons of national security, public safety or prevention or investigation of criminal offenses. | privacy | not-implemented | Publisher Questionnaire — Question 20.7 |  |
| 217 | There is no reason to believe that any potentially problematic law(s) will be applied, in practice, in relation to Publisher Data processed. | privacy | implemented | Publisher Questionnaire — Question 20.8 |  |
| 218 | Publisher's database is not accessed. | database, privacy | not-implemented | Publisher Questionnaire — Question 20.9 |  |
| 219 | Websites branded with Publisher marks are not hosted or operated. | privacy | not-implemented | Publisher Questionnaire — Question 21 |  |
| 220 | A script embedded by Publisher to their website loads the player inside an iFrame. | application, script-embed | implemented | Publisher Questionnaire — Question 22.1 |  |
| 221 | Information is collected through cookies/http/javascript, depending on the users preferences according to the CMP signals transferred by Publisher. | privacy | implemented | Publisher Questionnaire — Question 22.2 |  |
| 222 | Analytics and demand partners can collect information about users. | privacy, analytics | implemented | Publisher Questionnaire — Question 22.3 |  |
| 223 | Analytics and demand partners can set cookies directly. | privacy | implemented | Publisher Questionnaire — Question 22.3 |  |
| 224 | IP addresses are collected about users. | personal-data, privacy | implemented | Publisher Questionnaire — Question 22.4 |  |
| 225 | User-agent information is collected about users. | personal-data, privacy | implemented | Publisher Questionnaire — Question 22.4 |  |
| 226 | User actions in the player are collected about users. | personal-data, privacy, analytics | implemented | Publisher Questionnaire — Question 22.4 |  |
| 227 | Approximate location at country/state/city level is collected about users. | personal-data, privacy | implemented | Publisher Questionnaire — Question 22.4 |  |
| 228 | Consent string is collected about users. | personal-data, privacy | implemented | Publisher Questionnaire — Question 22.4 |  |
| 229 | UUID (Trinity's unique identifier assigned to a cookie) is collected about users. | personal-data, privacy | implemented | Publisher Questionnaire — Question 22.4 |  |
| 230 | Cookies ID for targeted ads generated by providers such as id5 (as approved through publisher's CMP) are collected about users. | personal-data, privacy | implemented | Publisher Questionnaire — Question 22.4 |  |
| 231 | The only information Publisher receives is aggregated data regarding number of clicks and revenue, unless otherwise required by Publisher in its role as a data controller. | privacy, analytics | implemented | Publisher Questionnaire — Question 22.5 |  |
| 232 | The cookie banner is Publisher's. | privacy | implemented | Publisher Questionnaire — Question 22.6 |  |
| 233 | The privacy policy is Publisher's. | privacy | implemented | Publisher Questionnaire — Question 22.6 |  |




|| 234 | Pseudonymized, anonymized, aggregate, or de-identified personal data is not re-identified. | privacy, personal-data | implemented | DPA - Section 5.c |  |
|| 235 | The personal data processed (random UUID, IP address, user-agent, and user actions in the player) cannot be used to identify a specific natural person. | privacy, personal-data | implemented | DPA - Section 5.c |  |
|| 236 | A written information security and privacy program with documented policies and training is maintained. | privacy | implemented | DPA - Annex II.1.a |  |
|| 237 | Ongoing training and awareness materials on the Information Security Program are provided to all personnel that may have access to customer data, including on the topics of phishing and social engineering. | privacy | implemented | DPA - Annex II.1.b |  |
|| 238 | A documented risk assessment program is implemented and periodic risk assessments are performed. | privacy | implemented | DPA - Annex II.1.c |  |
|| 239 | Commercially-reasonable background checks are performed on personnel with access to customer data in compliance with applicable laws. | privacy | implemented | DPA - Annex II.1.d |  |
|| 240 | Personnel with access to customer data who have criminal history involving offenses related to theft, fraud, burglary, bribery, property damage, violence, sexual misconduct, harassment, or securities laws violations are excluded. | privacy | implemented | DPA - Annex II.1.d |  |
|| 241 | Access to systems is restricted to only those personnel that require such access for legitimate work-related purposes, consistent with the concepts of least privilege and need-to-know. | access-control | implemented | Publisher Questionnaire — Question 8; DPA - Annex II.2.a.ii |  |
|| 242 | Access requests are required to be approved by a different individual than the requester, consistent with the concept of segregation of duties. | access-control | implemented | DPA - Annex II.2.a.iii |  |
|| 243 | Access privileges to customer data are immediately terminated for any personnel that no longer need such access, and reviews of access lists are conducted to ensure that access privileges have been appropriately provisioned and terminated. | access-control | implemented | DPA - Annex II.2.a.iv |  |
|| 244 | Appropriate network security measures are maintained, including firewalls to segregate internal networks from the internet, risk-based network segmentation, and intrusion prevention or detection systems to alert to suspicious network activity. | network, infrastructure | implemented | Publisher Questionnaire — Question 8; DPA - Annex II.2.b |  |
|| 245 | Customer data is logically isolated from data from any other source. | privacy | implemented | DPA - Annex II.2.c |  |
|| 246 | Periodic authenticated vulnerability scanning is performed on all systems storing, processing, or transmitting customer data to identify all potential vulnerabilities on such systems. | vulnerability-management | implemented | Publisher Questionnaire — Question 8; DPA - Annex II.2.d.i |  |
|| 247 | All remote network and system access to systems is protected by multi-factor authentication. | access-control, network, mfa | implemented | Publisher Questionnaire — Question 8; DPA - Annex II.2.g.ii |  |
|| 248 | Authentication credentials stored on systems are encrypted or hashed with a salt. | encryption, credentials | implemented | Publisher Questionnaire — Question 8; DPA - Annex II.2.h |  |
|| 249 | All customer data is encrypted in transit. | encryption, encryption-in-transit, personal-data | implemented | Publisher Questionnaire — Question 8; DPA - Annex II.2.j.i |  |
|| 250 | To the extent that customer data includes data considered to be sensitive under applicable law, such data is encrypted at rest using industry-standard encryption algorithms, and in accordance with industry standards for secure key and protocol negotiation and key management. | encryption, encryption-at-rest | implemented | compliance.yml — requirement 5.07; compliance.yml — requirement 7.01; Publisher Questionnaire — Question 8; DPA - Annex II.2.j.ii |  |
|| 251 | Infrastructure is managed as Infrastructure as Code (IaC) using CloudFormation and serverless, which provides documented baseline security configuration standards and monitoring for unauthorized changes. | infrastructure, cloud | implemented | DPA - Annex II.2.k.i |  |
|| 252 | Audit logs with CloudTrail are enabled on all sensitive data stores (databases and S3) to capture detailed information such as event source, date, user, timestamp, source addresses, destination addresses, and other useful elements. | logging, audit-logging, cloud | implemented | DPA - Annex II.2.l.i |  |
|| 253 | Extensive monitoring and alerting is maintained on all systems, including centralized log aggregation and analysis for anomalous and suspicious activity to assist in the identification of possible security incidents. | monitoring, logging | implemented | compliance.yml — requirement 5.07; DPA - Annex II.2.l.ii |  |
|| 254 | All internal services are accessible exclusively via VPN protected by two-factor authentication (2FA). | network, vpn, mfa | implemented | DPA - Annex II.2.m |  |
|| 255 | As part of the deployment process, changes are reviewed and tested automatically, as well as peer reviewed. | ci-cd, secure-development | implemented | DPA - Annex II.2.m |  |
|| 256 | Scripts are scanned against common virus providers to detect any potential threats before release. | secure-development, vulnerability-management | implemented | DPA - Annex II.2.m |  |
|| 257 | Strict permissions are enforced for uploading files intended for public serving. | access-control, secure-development | implemented | DPA - Annex II.2.m |  |
|| 258 | Access to facilities is restricted to personnel who are authorized to have such access. | access-control | implemented | DPA - Annex II.3.a |  |
|| 259 | Restricted areas of facilities, such as server rooms, are subject to risk-appropriate access controls, such as by requiring key cards and/or PINs for entry. | access-control | implemented | DPA - Annex II.3.a |  |
|| 260 | Audit trails of access to restricted areas of facilities are regularly reviewed. | access-control, audit-logging | implemented | DPA - Annex II.3.a |  |
||| 261 | Sensitive Information is not retained longer than necessary to fulfill the purposes for which it was collected or as required by applicable law. | privacy, data-retention | implemented | DPA - Section II(A)(6) |  |
||| 262 | Sensitive data is deleted upon customer request. | privacy, data-retention | implemented | DPA - Section II(A)(6) |  |
||| 263 | Deletion of sensitive information includes all backups thereof. | privacy, data-retention, backup | implemented | DPA - PRC Addendum Article 4.4 |  |
