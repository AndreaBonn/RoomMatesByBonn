# Security Policy

> **[🇮🇹 Leggi in Italiano](./SECURITY_IT.md)** | **🇬🇧 English**

---

## 🔒 Security Overview

Security is a top priority for RoomMate App. This document outlines our security practices, supported versions, and how to report vulnerabilities.

**Quick Links:**
- [Supported Versions](#supported-versions)
- [Reporting a Vulnerability](#reporting-a-vulnerability)
- [Security Best Practices](#security-best-practices)
- [Data Protection](#data-protection)
- [Third-Party Security](#third-party-security)

---

## 📋 Supported Versions

We actively maintain and provide security updates for the following versions:

| Version | Supported          | Status |
| ------- | ------------------ | ------ |
| 1.0.x   | ✅ Yes            | Active |
| < 1.0   | ❌ No             | Deprecated |

**Update Policy:**
- Security patches are released as soon as possible after discovery
- Users are notified of critical security updates through the application
- We recommend always using the latest version

---

## 🚨 Reporting a Vulnerability

We take all security vulnerabilities seriously. If you discover a security issue, please follow these guidelines:

### How to Report

**DO NOT** create a public GitHub issue for security vulnerabilities.

Instead, please report security issues privately:

1. **Email**: Send details to `andreabonacci95@protonmail.com`
2. **Subject Line**: Use "SECURITY: [Brief Description]"
3. **Include**:
   - Description of the vulnerability
   - Steps to reproduce the issue
   - Potential impact assessment
   - Suggested fix (if any)
   - Your contact information

### What to Expect

- **Acknowledgment**: Within 48 hours of your report
- **Initial Assessment**: Within 5 business days
- **Status Updates**: Regular updates on progress
- **Resolution Timeline**: Varies based on severity
  - Critical: 1-7 days
  - High: 7-14 days
  - Medium: 14-30 days
  - Low: 30-90 days

### Responsible Disclosure

We follow responsible disclosure practices:

1. **Confidentiality**: We keep your report confidential until a fix is deployed
2. **Credit**: We acknowledge security researchers (with permission)
3. **Coordination**: We work with you to understand and fix the issue
4. **Public Disclosure**: Only after a fix is deployed and users have time to update

### Bug Bounty

Currently, we do not offer a formal bug bounty program. However, we deeply appreciate security researchers who help us improve the application's security.

---

## 🛡️ Security Best Practices

### For Users

#### Account Security

✅ **DO**:
- Use a strong, unique password (minimum 8 characters with uppercase, lowercase, numbers, and symbols)
- Enable two-factor authentication when available
- Keep your email account secure (it's used for password recovery)
- Log out from shared devices
- Regularly review your account activity

❌ **DON'T**:
- Share your password with anyone, including roommates
- Use the same password across multiple services
- Save passwords in unsecured locations
- Leave your account logged in on public computers

#### House Invite Codes

✅ **DO**:
- Share invite codes only with trusted roommates
- Regenerate invite codes if compromised
- Remove members who no longer live in the house

❌ **DON'T**:
- Post invite codes publicly (social media, forums, etc.)
- Share invite codes with people you don't know
- Reuse old invite codes

#### API Keys (AI Features)

✅ **DO**:
- Keep your AI provider API keys confidential
- Use the local storage option for maximum security
- Set usage limits on your AI provider accounts
- Regularly rotate your API keys
- Monitor your AI provider usage and billing

❌ **DON'T**:
- Share your API keys with others
- Use API keys from untrusted sources
- Store API keys in plain text outside the application
- Use production API keys for testing

#### Data Privacy

✅ **DO**:
- Review what data you share with roommates
- Use strong passwords for sensitive documents
- Regularly review house members
- Be cautious about what you post in announcements

❌ **DON'T**:
- Share sensitive personal information in public announcements
- Upload confidential documents without encryption
- Grant admin access to untrusted users

### For Administrators

#### House Management

✅ **DO**:
- Regularly audit house members
- Remove inactive or former roommates promptly
- Review and approve new member requests carefully
- Keep contact information up to date
- Regularly backup important data (export features)

❌ **DON'T**:
- Grant admin privileges unnecessarily
- Leave former roommates with access
- Ignore suspicious activity
- Share admin credentials

#### Data Management

✅ **DO**:
- Regularly export important financial data
- Review expense history for anomalies
- Keep receipts for significant expenses
- Document important house decisions

❌ **DON'T**:
- Delete important records without backup
- Ignore discrepancies in financial data
- Share sensitive house information publicly

---

## 🔐 Data Protection

### Data Storage

**Firebase Firestore**:
- All data is encrypted in transit (HTTPS/TLS)
- Data at rest is encrypted by Google Cloud Platform
- Database access is controlled by Firestore Security Rules
- Multi-region replication for reliability

**Local Storage**:
- PWA cache for offline functionality
- IndexedDB for local data persistence
- Automatic cache invalidation
- Secure storage for API keys (when local option is selected)

### Data Access Control

**Role-Based Access**:
- **Admin**: Full access to house data, member management
- **Member**: Access to shared data, limited modification rights
- **User**: Access only to personal data and houses they belong to

**Security Rules**:
- Firestore Security Rules enforce access control at the database level
- Users can only access data from houses they are members of
- Personal data (API keys, profile) is accessible only by the owner
- NPC (virtual member) data is accessible by all house members

### Data Retention

- **Active Data**: Retained while you use the application
- **Deleted Accounts**: Data is anonymized but retained for historical records
- **Inactive Houses**: Data is retained indefinitely (you control deletion)
- **Exports**: You can export all your data at any time

### Data Deletion

Users can:
- Delete their own account (profile data is removed)
- Leave houses (membership is removed, historical data remains)
- Delete content they created (expenses, announcements, etc.)

Admins can:
- Remove members from houses
- Delete house data
- Export all house data before deletion

---

## 🔗 Third-Party Security

### Firebase (Google)

- **Security**: Enterprise-grade security by Google Cloud Platform
- **Compliance**: SOC 2, ISO 27001, GDPR compliant
- **Documentation**: [Firebase Security](https://firebase.google.com/support/privacy)

### AI Providers

**OpenAI**:
- API keys are encrypted
- Data is not used for model training (per API terms)
- [OpenAI Security](https://openai.com/security)

**Anthropic Claude**:
- Enterprise-grade security
- Data privacy commitments
- [Anthropic Security](https://www.anthropic.com/security)

**Google Gemini**:
- Google Cloud security standards
- [Google AI Security](https://ai.google/responsibility/safety-security/)

**Groq**:
- Fast inference with security
- [Groq Security](https://groq.com/security/)

### Brevo (Email Service)

- **Security**: ISO 27001 certified
- **Compliance**: GDPR compliant
- **Documentation**: [Brevo Security](https://www.brevo.com/legal/securitypolicy/)

### Dependencies

- Regular dependency updates via npm
- Automated vulnerability scanning
- Security patches applied promptly
- Minimal dependency footprint

---

## 🔍 Security Features

### Authentication

- **Firebase Authentication**: Industry-standard authentication
- **Password Requirements**: Minimum 8 characters, complexity requirements
- **Session Management**: Secure token-based sessions
- **Password Reset**: Secure email-based password recovery

### Authorization

- **Firestore Security Rules**: Database-level access control
- **Role-Based Access Control (RBAC)**: Admin and member roles
- **Resource-Level Permissions**: Fine-grained access control
- **Automatic Validation**: Server-side validation of all operations

### Data Transmission

- **HTTPS Only**: All communications encrypted with TLS 1.2+
- **Secure Headers**: CSP, HSTS, X-Frame-Options configured
- **API Security**: Bearer token authentication for all API calls

### Application Security

- **Input Validation**: All user inputs validated and sanitized
- **XSS Protection**: React's built-in XSS protection
- **CSRF Protection**: Token-based CSRF protection
- **SQL Injection**: Not applicable (NoSQL database)
- **Rate Limiting**: Protection against brute force attacks

### PWA Security

- **Service Worker**: Secure caching strategies
- **HTTPS Required**: PWA only works over HTTPS
- **Content Security Policy**: Strict CSP headers
- **Subresource Integrity**: Verified external resources

---

## 📱 Mobile Security

### PWA Installation

- Install only from trusted sources (official URL)
- Verify HTTPS connection before installation
- Review permissions requested by the app

### Offline Data

- Offline data is stored securely in IndexedDB
- Automatic sync when connection is restored
- Cache is cleared on logout

### Device Security

- Use device lock screen protection
- Enable biometric authentication if available
- Keep your device OS updated
- Use trusted networks for sensitive operations

---

## 🚀 Incident Response

### Our Process

1. **Detection**: Monitoring and user reports
2. **Assessment**: Evaluate severity and impact
3. **Containment**: Immediate actions to limit damage
4. **Eradication**: Remove the vulnerability
5. **Recovery**: Restore normal operations
6. **Lessons Learned**: Post-incident analysis

### User Notification

We will notify users in case of:
- Data breaches affecting personal information
- Security vulnerabilities requiring immediate action
- Significant security updates

Notification methods:
- In-app notifications
- Email to registered address
- Public announcement (if appropriate)

---

## 📚 Security Resources

### For Developers

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Firebase Security Rules](https://firebase.google.com/docs/rules)
- [React Security Best Practices](https://reactjs.org/docs/dom-elements.html#dangerouslysetinnerhtml)

### For Users

- [Password Security Guide](https://www.ncsc.gov.uk/collection/top-tips-for-staying-secure-online/use-a-strong-and-separate-password-for-email)
- [Two-Factor Authentication](https://www.cisa.gov/mfa)
- [Phishing Awareness](https://www.consumer.ftc.gov/articles/how-recognize-and-avoid-phishing-scams)

---

## 📞 Contact

For security concerns or questions:

**Security Contact**: andreabonacci95@protonmail.com

**Author**: Andrea Bonacci
- GitHub: [@AndreaBonn](https://github.com/AndreaBonn)

**Response Time**: We aim to respond to security inquiries within 48 hours.

---

## 📝 Security Changelog

### Version 1.0.0 (December 2024)

- ✅ Firebase Authentication implementation
- ✅ Firestore Security Rules deployed
- ✅ HTTPS-only enforcement
- ✅ Role-based access control
- ✅ API key encryption options
- ✅ PWA security features
- ✅ Input validation and sanitization
- ✅ Secure session management

---

## 🔄 Updates to This Policy

This security policy may be updated periodically. Significant changes will be announced through:
- In-app notifications
- README updates
- Email notifications (for critical changes)

**Last Updated**: December 2024

---

**[🏠 Back to README](./README.md)** | **[🇮🇹 Versione Italiana](./SECURITY_IT.md)** | **[📄 License](./LICENSE.md)**
