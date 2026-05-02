# Security Policy · Biztonsági irányelv

## Reporting a Vulnerability · Sebezhetőség bejelentése

### English

If you discover a security vulnerability in any Forum Hungaricum repository, service, or infrastructure, please report it responsibly.

**Email**: [security@forumhungaricum.eu](mailto:security@forumhungaricum.eu)

**PGP key**: published at [forumhungaricum.eu/.well-known/security.txt](https://forumhungaricum.eu/.well-known/security.txt) once available (RFC 9116 compliant).

**Please include**:
- Description of the vulnerability
- Steps to reproduce
- Affected component (repository, service, endpoint)
- Suggested mitigation if known
- Whether you wish to be acknowledged in the disclosure

### Magyarul

Ha sebezhetőséget fedezel fel bármely Forum Hungaricum repository-ban, szolgáltatásban vagy infrastruktúrában, kérünk, jelentsd felelősségteljesen.

**Email**: [security@forumhungaricum.eu](mailto:security@forumhungaricum.eu)

**Mit kérünk**:
- A sebezhetőség leírása
- Lépésenkénti reprodukció
- Érintett komponens (repository, szolgáltatás, végpont)
- Javasolt mitigáció, ha ismert
- Szeretnéd-e nyilvánosan elismertetni a felfedezésedet a publikálás során

---

## Response Timeline · Válaszadási időkeret

| Severity | Initial response | Mitigation timeline |
|---|---|---|
| **Critical** (RCE, data exfiltration, credential exposure) | within 24 hours | 7 days |
| **High** (privilege escalation, auth bypass) | within 48 hours | 14 days |
| **Medium** (XSS, CSRF, info leak) | within 5 days | 30 days |
| **Low** (rate-limit issues, hardening) | within 14 days | 90 days |

We follow **coordinated disclosure**: we'll work with you on a disclosure timeline that allows us to fix the issue before public announcement.

A **koordinált felfedés** elvét követjük: együttműködve dolgozunk veled olyan publikálási ütemterven, ami lehetővé teszi a hiba javítását a nyilvános bejelentés előtt.

---

## Scope · Hatáskör

### In scope · Hatáskörbe tartozik
- All production services hosted under `*.forumhungaricum.eu`
- All public Forum Hungaricum repositories
- Email infrastructure on `forumhungaricum.eu`
- Anonymous intake (Tabella) when deployed

### Out of scope · Hatáskörön kívül
- Third-party services we depend on (GitHub, Cloudflare, etc.) — please report to them directly
- Beta or experimental features clearly marked as such
- Theoretical attacks without practical demonstration
- Vulnerabilities in dependencies that we don't directly include
- DoS attacks against rate-limited endpoints
- Social engineering attacks against staff or contributors

---

## Safe Harbor · Védett zóna

We commit to:

- **Not pursuing legal action** against researchers who follow this policy in good faith
- **Working with you** to understand and resolve the issue quickly
- **Recognizing** your contribution publicly (if you wish) once the issue is resolved
- **Notifying you** before publishing the fix or disclosure

Researchers who:
- Make a good-faith effort to comply with this policy
- Avoid privacy violations, destruction of data, and interruption or degradation of our services
- Do not exploit beyond what's necessary to confirm the vulnerability

…are welcome and protected.

Vállaljuk, hogy:
- **Nem indítunk jogi eljárást** olyan kutatókkal szemben, akik jóhiszeműen követik ezt az irányelvet
- **Együttműködünk** a probléma gyors megértéséért és megoldásáért
- **Nyilvánosan elismerjük** a hozzájárulásodat (ha akarod) a probléma megoldása után
- **Értesítünk** a javítás vagy publikálás előtt

---

## Hall of Fame · Felfedezők elismerése

A list of researchers who have responsibly disclosed vulnerabilities will be maintained at [forumhungaricum.eu/security/hall-of-fame](https://forumhungaricum.eu/security/hall-of-fame) once available.

---

*Last updated: 2026-05-02*
