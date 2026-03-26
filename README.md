# Genfactor Shield

A curated collection of security testing resources packaged as Claude Code plugins by [Genfactor](https://github.com/genfactorai).

## Overview

Genfactor Shield provides organized, immediately accessible security testing resources that integrate with Claude Code workflows. Built on curated content from [SecLists](https://github.com/danielmiessler/SecLists), these plugins give you instant access to essential wordlists, payloads, patterns, and detection tools for:

- Authorized penetration testing and security assessments
- Bug bounty program research
- CTF competition problem solving
- Security tool development and testing
- LLM/AI security testing and red teaming
- Vulnerability research in controlled environments

## Quick Start

### Install the Marketplace

```bash
/plugin marketplace add genfactorai/genfactor-shield
```

### Browse and Install Plugins

```bash
# Browse all available plugins
/plugin

# Install individual plugins
/plugin install shield-fuzzing@genfactor-shield
/plugin install shield-passwords@genfactor-shield
/plugin install shield-patterns@genfactor-shield
/plugin install shield-payloads@genfactor-shield
/plugin install shield-usernames@genfactor-shield
/plugin install shield-webshells@genfactor-shield
/plugin install shield-llm@genfactor-shield
```

### Verify Installation

```bash
# Try a command
/test-sql-injection

# Or ask Claude naturally
"Use the shield-fuzzing skill to show me SQL injection payloads"
```

## What You Get

### 7 Plugins

| Plugin | What it provides |
|:--|:--|
| `shield-fuzzing` | SQL injection, command injection, NoSQL injection payloads |
| `shield-passwords` | Common passwords, breach compilations, probable passwords |
| `shield-patterns` | API key detection, credit card formats, email/IP/SSN patterns |
| `shield-payloads` | XSS vectors, XXE payloads, template injection, file upload bypasses |
| `shield-usernames` | Default usernames, common accounts, service-specific names |
| `shield-webshells` | PHP, ASP, JSP, Python web shell samples for detection |
| `shield-llm` | Bias detection, data leakage, alignment testing, adversarial prompts |

### 5 Slash Commands

| Command | Purpose |
|:--|:--|
| `/test-sql-injection` | SQL injection testing with database-specific guidance |
| `/test-xss` | XSS testing with context-aware payload suggestions |
| `/get-wordlist` | Quick access to curated wordlists |
| `/detect-webshell` | Defensive web shell detection guidance |
| `/scan-secrets` | Find exposed API keys and credentials |

### 3 Specialized Agents

| Agent | Role |
|:--|:--|
| `pentest-advisor` | Strategic penetration testing methodology and planning |
| `ctf-assistant` | CTF competition challenge solver with educational focus |
| `bug-bounty-hunter` | Professional bug bounty hunting and responsible disclosure |

## Usage

### Slash Commands

```bash
/test-sql-injection    # Interactive SQL injection testing guide
/test-xss              # XSS vulnerability testing
/get-wordlist          # Access curated wordlists
/detect-webshell       # Web shell detection (defensive)
/scan-secrets          # Scan for exposed secrets
```

### Natural Language

```bash
"Use the shield-fuzzing skill to help me test for SQL injection vulnerabilities"
"Show me common passwords from the shield-passwords skill"
"Help me detect exposed API keys using the shield-patterns skill"
"I need XSS payloads from the shield-payloads skill"
```

### Specialized Agents

```bash
"Use the pentest-advisor agent to help me plan a security assessment"
"Use the ctf-assistant agent to help me solve this web exploitation challenge"
"Use the bug-bounty-hunter agent to help me test this bug bounty program responsibly"
```

### LLM Security Testing

```bash
"Use the shield-llm skill to test this AI model for gender bias"
"Use the shield-llm skill to test for data leakage and privacy issues"
"Use the shield-llm skill for a red team assessment on this LLM"
```

## Available Plugins

### shield-fuzzing
Essential fuzzing payloads for vulnerability testing:
- SQL injection testing payloads
- Command injection patterns
- NoSQL injection vectors
- LDAP injection strings
- Special character fuzzing
- Authentication bypass patterns

### shield-passwords
Curated password lists for authorized credential testing:
- 500 worst passwords
- 10K most common passwords
- 100K NCSC password list
- Dark web breach compilations
- Probable password variations

### shield-patterns
Sensitive data patterns for security testing:
- API key detection patterns
- Credit card format validation
- Email address patterns
- IP address discovery
- SSN format matching
- Phone number patterns

### shield-payloads
Specialized attack payloads for testing:
- XSS injection vectors
- XXE payloads
- Template injection
- File upload bypasses
- Path traversal strings

### shield-usernames
Common username wordlists:
- Default usernames
- Common account names
- Service-specific usernames
- Admin account patterns

### shield-webshells
Web shell samples for detection and analysis:
- PHP web shells
- ASP/ASPX shells
- JSP shells
- Python shells
- Perl shells

### shield-llm
Comprehensive AI/ML security testing prompts:
- Bias detection (gender, nationality, race/ethnicity)
- Data leakage and privacy testing
- Memory recall testing
- Alignment and divergence attacks
- Adversarial prompt resistance
- AI safety evaluation

## Project Structure

```
genfactor-shield/
├── .claude-plugin/
│   ├── marketplace.json              # Marketplace definition
│   ├── plugin.json                   # Plugin manifest
│   ├── commands/                     # Slash commands
│   │   ├── test-sql-injection.md
│   │   ├── test-xss.md
│   │   ├── get-wordlist.md
│   │   ├── detect-webshell.md
│   │   └── scan-secrets.md
│   └── agents/                       # Specialized agents
│       ├── pentest-advisor.md
│       ├── ctf-assistant.md
│       └── bug-bounty-hunter.md
├── seclists-categories/
│   ├── fuzzing/                      # SQL/NoSQL/Command injection
│   ├── passwords/                    # Password wordlists
│   ├── pattern-matching/             # API keys, sensitive data
│   ├── payloads/                     # XSS, XXE, file upload
│   ├── usernames/                    # Username wordlists
│   └── web-shells/                   # Web shell samples
└── LLM_Testing/                      # AI/ML security testing
```

## Security & Ethics

### Authorized Use Cases
- Authorized penetration testing with written permission
- Bug bounty programs (within documented scope)
- CTF competitions and challenges
- Security research in controlled lab environments
- Testing your own systems and applications
- LLM safety evaluation and bias testing
- Educational demonstrations with proper safeguards

### Prohibited Use Cases
- Unauthorized access attempts against any system
- Testing systems without explicit permission
- Malicious activities or attacks
- Privacy violations or data theft
- Attacks against critical infrastructure
- Mass exploitation or automated attacks

## Source & Attribution

Security testing resources sourced from [SecLists](https://github.com/danielmiessler/SecLists) by Daniel Miessler and contributors (MIT License).

## Requirements

- Claude Code CLI (latest version)
- Basic understanding of security testing concepts
- Authorization for security testing on target systems

## License

MIT License - Use responsibly with proper authorization.

---

**Genfactor Shield** | Security testing tools for Claude Code
