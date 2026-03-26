# Quick Start Guide

## Installation

### Add the Marketplace

```bash
/plugin marketplace add genfactorai/genfactor-shield
```

### Browse Available Plugins

```bash
/plugin
```

### Install All Shield Plugins

```bash
/plugin install shield-fuzzing@genfactor-shield
/plugin install shield-passwords@genfactor-shield
/plugin install shield-patterns@genfactor-shield
/plugin install shield-payloads@genfactor-shield
/plugin install shield-usernames@genfactor-shield
/plugin install shield-webshells@genfactor-shield
/plugin install shield-llm@genfactor-shield
```

## Available Commands

### Security Testing Commands

```bash
/test-sql-injection    # SQL injection testing guidance
/test-xss              # XSS vulnerability testing
/get-wordlist          # Access SecLists wordlists
/detect-webshell       # Web shell detection (defensive)
/scan-secrets          # Scan for exposed credentials
```

## Available Agents

Ask Claude Code to use these specialized agents:

- **pentest-advisor** — For penetration testing methodology and strategy
- **ctf-assistant** — For CTF competition challenges
- **bug-bounty-hunter** — For bug bounty programs and responsible disclosure

## Example Usage

### SQL Injection Testing

```bash
# Start with the command
/test-sql-injection

# Follow the interactive guidance
# Access payloads from: seclists-categories fuzzing/fuzzing/references/Fuzzing/
```

### Bug Bounty Hunting

```
"I need help testing a bug bounty program. Use the bug-bounty-hunter agent."

Then describe your target and scope.
```

### CTF Challenge

```
"Help me solve this web CTF challenge using the ctf-assistant agent."

Describe the challenge and get strategic guidance.
```

### LLM Security Testing

```
"Use the shield-llm skill to test this AI model for bias and data leakage."

Describe the model and testing goals.
```

## Security Resources

### Fuzzing Payloads
- SQL injection: `quick-SQLi.txt`, `Generic-SQLi.txt`
- NoSQL injection: `NoSQL.txt`
- Command injection: `command-injection-commix.txt`
- LDAP injection: `LDAP.txt`

### Passwords
- Common: `500-worst-passwords.txt`, `10k-most-common.txt`
- Leaked: Various breach compilations
- Probable: `probable-v2-top*.txt`

### Payloads
- XSS vectors
- XXE exploitation
- Template injection
- File upload bypasses

### Patterns
- API keys (AWS, Google, GitHub)
- Credit card formats
- Email addresses
- IP addresses

### Usernames
- Default accounts
- Common names
- Service-specific accounts

### Web Shells (Defensive)
- PHP shells
- ASP/ASPX shells
- JSP shells
- Detection patterns

## Important Reminders

**CRITICAL**: Only use for:
- Authorized penetration testing with written permission
- Bug bounty programs within documented scope
- CTF competitions and challenges
- Testing your own systems
- Educational purposes in controlled environments

**NEVER**:
- Test unauthorized systems
- Violate terms of service
- Access personal data unnecessarily
- Ignore rate limits or cause DoS
- Share vulnerabilities before responsible disclosure

## Getting Help

- Read command documentation: Each slash command has built-in guidance
- Use specialized agents: They provide comprehensive methodology
- Check SecLists documentation: https://github.com/danielmiessler/SecLists

## Support

- GitHub Issues: https://github.com/genfactorai/genfactor-shield/issues

---

**Genfactor Shield** | Always obtain proper authorization before conducting any security testing.
