# OWASP Top 10 2021

![OWASP Top 10 2021](images/owasp_top10_2021.png)

1. A01:2021-Broken Access Control
2. A02:2021-Cryptographic Failures
3. A03:2021-Injection
4. A04:2021-Insecure Design
5. A05:2021-Security Misconfiguration
6. A06:2021-Vulnerable and Outdated Components
7. A07:2021-Identification and Authentication Failures
8. A08:2021-Software and Data Integrity Failures
9. A09:2021-Security Logging and Monitoring Failures
10. A10:2021-Server-Side Request Forgery

## Let Me Explain

1. Access control vulnerabilities include privilege escalation, malicious URL modification, access control bypass, CORS misconfiguration, and tampering with primary keys.
   1. Except for public resources, deny by default.
   2. Implement access control mechanisms once and re-use them throughout the application, including minimizing CORS usage.
   3. Model access controls should enforce record ownership rather than accepting that the user can create, read, update, or delete any record.
   4. CORS misconfiguration allows API access from unauthorized/untrusted origins.
   5. Metadata manipulation, such as replaying or tampering with a JSON Web Token (JWT) access control token, or a cookie or hidden field manipulated to elevate privileges or abusing JWT invalidation.
   6. Elevation of privilege. Acting as a user without being logged in or acting as an admin when logged in as a user.
   7. Permitting viewing or editing someone else's account, simply providing it's unique identifier.
   8. Bypassing access control checks by modifying the URL, internal application state, or the HTML page, or simply using a custom API attack tool.
   9. https://owasp.org/Top10/A01_2021-Broken_Access_Control/
2. This includes security failures when data is in transit or at rest, such as the implementation of weak cryptographic algorithms, poor or lax key generation, a failure to implement encryption or to verify certificates, and the transmission of data in cleartext.
   1. https://portswigger.net/daily-swig/owasp-shakes-up-web-app-threat-categories-with-release-of-draft-top-10
   2. https://owasp.org/Top10/A02_2021-Cryptographic_Failures/
3. https://slides.com/riddhishreechaurasia/build-break-learn#/2/2
4. follow secure design patterns and principles
   1. Follow best practices, wherever possible
   2. Build things with security-centric mindset
   3. Secure design principles must be followed and adhered to for the lifetime of the application/services
   4. Code reviews must be done thoroughly to avoid any bad code going into the production
   5. Regular code audits and pentests are a good way to ensure the security of your products. It’s a general advice that would help detect and mitigate most of the trivial issues.
5. The simplest example would be misconfigurations in the cloud service called IAM (Identity and Access Management). If the permissions assigned to an entity is more than it needs to do it’s job effectively, this could open room for exploitation, if the credentials for that entity got compromised or misused by trusted parties.
   1. Disable unnecessary features that are not required in the production environments.
   2. Follow “Principle of Least Privilege”. Assign only the required privileges to the entities, to carry out their tasks effectively.
   3. Configure the security headers properly: they should not be over-permissive, else they tend to become ineffective!
   4. Make sure to update the services and packages being used
   5. Services must be configured with security in mind.
   6. Follow repeated hardening and patching procedure.
   7. Audit your infrastructure and get regular pentest to ensure high security of your apps/services. It’s a general advice that would help detect and mitigate most of the trivial issues.
   8. https://medium.com/@shivam_bathla/a05-2021-security-misconfiguration-fe6d321d71d7
6. Managing your dependencies is a great deal of work. It’s not as simple as running the update command or downloading the updated dependencies & packages. But it much more than this: your apps might break with the latest changes, some features might get deprecated, functions might renamed, the dependencies might be abandoned, the fix might not work on your system without breaking some other dependencies, creating a havoc. This process of updating things and making sure that they remain the latest sounds simple but it’s quite a lot of work and not always feasible
   1. Maintain an inventory of components you are using and ensure that they are kept up-to-date.
   2. Remove unused dependencies and components to reduce the attack surface and your liabilities (yes, code is indeed a great liability!)
   3. Install the components via trusted channels and make sure to validate their integrity. Also, it’s better to use signed packages (if available).
   4. Be on the lookout for any security patches for the components you are relying on. If the packages you use are not maintained, then either make sure you apply patches yourself or use some alternate component that is well maintained and has a big user-base and supporting community. If possible, then this should actually be done right from the start — choose your dependencies and components wisely!
   5. https://medium.com/@shivam_bathla/a06-2021-vulnerable-and-outdated-components-a5d96017049c    
7. Can you fake your identity? Does the system grant you access with this faked identity?
   1. Password bruteforcing, and credential stuffing
   2. Flawed password reset functionality
   3. Mishandled session identifiers
   4. https://medium.com/@shivam_bathla/a07-2021-identification-and-authentication-failures-b585c856eb24
8. How sure are you about the integrity of the apps or data that you are consuming? Ensure that a software supply chain security tool, such as **OWASP Dependency Check** or **OWASP CycloneDX**, is used to verify that components do not contain known vulnerabilities.
   1. https://www.fireeye.com/blog/threat-research/2020/12/evasive-attacker-leverages-solarwinds-supply-chain-compromises-with-sunburst-backdoor.html
9.  When a security-critical event occurs, the software either does not record the event or omits important details about the event when logging it. When security-critical events are not logged properly, such as a failed login attempt, this can make malicious behavior more difficult to detect and may hinder forensic analysis after an attack succeeds. If security critical information is not recorded, there will be no trail for forensic analysis and discovering the cause of problems or the source of attacks may become more difficult or impossible.
   2. https://www.sans.org/brochure/course/log-management-in-depth/6
   3. https://owasp-top-10-proactive-controls-2018.readthedocs.io/en/latest/c9-implement-security-logging-monitoring.html
   4. https://cwe.mitre.org/data/definitions/778.html
   5. https://docs.microsoft.com/en-us/azure/architecture/best-practices/monitoring
10. https://blog.appsecco.com/server-side-request-forgery-via-html-injection-in-pdf-download-90ee4053e911

## Getting Serious?

**Pre-requisites:**
Create a free account on [portswigger.net](https://portswigger.net/users/register)

**Try out these labs:**
1. [SQL Injection](https://portswigger.net/web-security/sql-injection)
2. [XSS](https://portswigger.net/web-security/cross-site-scripting)
3. [CSRF](https://portswigger.net/web-security/csrf)
4. [Clickjacking](https://portswigger.net/web-security/clickjacking)
5. [XXE](https://portswigger.net/web-security/xxe)
6. [Many More](https://portswigger.net/web-security/all-labs)

## Reference

* https://owasp.org/Top10/