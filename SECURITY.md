# Security Policy

**English** | [Italiano](./SECURITY_IT.md)

## Supported Versions

| Version | Supported |
|---|---|
| 1.0.x | ✅ Security updates |
| < 1.0 | ❌ End of life |

Security fixes are applied to the current release. Users are notified of critical updates through the application.

## Reporting a Vulnerability

Do not open a public GitHub issue for security problems.

Report privately through [GitHub Security Advisories](https://github.com/AndreaBonn/RoomMatesByBonn/security/advisories/new), or by email to andreabonacci95@protonmail.com with the subject `SECURITY: <short description>`.

Please include:

- A description of the vulnerability
- Steps to reproduce
- Expected versus actual behavior
- An impact assessment (what an attacker could achieve)

Response timeline:

- Acknowledgment within 72 hours
- Assessment of severity within 5 business days
- Coordinated public disclosure after a fix is released

There is no formal bug bounty program.

## Security Measures Implemented

These are the protections in place in the application. File references point to the application source, which is private.

- **Database access control**: Firestore Security Rules scope every read and write to the household the user belongs to, with role checks for owner, admin, and member (`firestore.rules`)
- **Authentication**: Firebase Authentication with email and password; session tokens are managed by the Firebase SDK
- **HTTP security headers**: strict Content-Security-Policy (`default-src 'self'`, `object-src 'none'`, explicit connect and frame allowlists), HSTS with `preload` and a one-year max-age, `X-Frame-Options: DENY`, `X-Content-Type-Options: nosniff`, `Referrer-Policy`, and a `Permissions-Policy` that disables camera, microphone, and geolocation (`firebase.json`)
- **Transport security**: HTTPS only, served by Firebase Hosting, with `upgrade-insecure-requests` in the CSP
- **Email service hardening**: Helmet for response headers, a CORS allowlist, and rate limiting on outbound mail with a global daily cap and a per-household cap (`email-service/server.js`, `email-service/middleware/rate-limit.js`)
- **AI API keys**: stored either in the browser or in Firestore at the user's choice; the CSP `connect-src` directive restricts which provider endpoints the client can call
- **Error monitoring**: Sentry captures runtime errors for diagnosis

The application uses a NoSQL database (Firestore), so SQL injection does not apply. Output is rendered through React, which escapes content by default.

## Security Best Practices for Users

- Use a strong, unique password and keep your email account secure, since it is used for password recovery
- Share household invite codes only with people you trust, and regenerate them if exposed
- Keep AI provider API keys private; prefer browser storage and set usage limits on your provider account
- Remove members who no longer live in the house
- Log out on shared devices

## Out of Scope

The following are not treated as vulnerabilities:

- Self-XSS that requires the victim to paste code into their own console
- Social engineering attacks
- Physical attacks against devices or infrastructure
- Vulnerabilities in third-party services (Firebase, Brevo, AI providers); report these to the respective vendor
- Denial of service through excessive legitimate use

## Acknowledgments

Security researchers who responsibly disclose vulnerabilities will be listed here.

---

[Back to README](./README.md)
