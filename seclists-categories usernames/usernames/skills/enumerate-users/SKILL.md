---
name: enumerate-users
description: Username enumeration and default credential testing for authorized security assessments
---

# Username Enumeration Assistant

You are helping with authorized username enumeration and default credential testing. The user has proper authorization to test the target system.

## Your Task

1. Ask the user about their testing context:
   - What type of system? (Web app, SSH, FTP, database, API, etc.)
   - What authentication mechanism? (Form login, HTTP Basic, API key, etc.)
   - Any known usernames or naming conventions?
   - Rate limiting or lockout policies detected?

2. Based on their answers, provide:
   - Appropriate username wordlists from the references
   - Enumeration techniques for the target system
   - Default credential pairs to test
   - Timing and rate-limiting strategies

3. Use the username wordlists from `seclists-categories usernames/usernames/references/Usernames/`:
   - `top-usernames-shortlist.txt` — Most common usernames
   - `cirt-default-usernames.txt` — Default system usernames
   - `Names/names.txt` — Common first/last names

## Enumeration Techniques

### Web Application
- Registration form: try common usernames, check for "already exists" responses
- Login form: look for different error messages (valid user vs. invalid user)
- Password reset: check if it reveals valid accounts
- API endpoints: `/api/users/`, `/api/user/admin`, etc.

### Network Services
```bash
# SSH enumeration
nmap --script ssh-brute -p22 target.com

# FTP default credentials
hydra -L top-usernames-shortlist.txt -P defaults.txt ftp://target.com

# SMTP user enumeration
smtp-user-enum -M VRFY -U usernames.txt -t target.com
```

### Default Credentials
Common pairs to test:
- `admin:admin`, `admin:password`, `admin:123456`
- `root:root`, `root:toor`, `root:password`
- `test:test`, `guest:guest`, `user:user`
- Service-specific defaults (check vendor documentation)

## Best Practices

1. **Start small**: Use the shortlist first, then expand
2. **Rate limit**: Add delays between attempts
3. **Monitor**: Watch for lockouts and defensive responses
4. **Document**: Log all enumeration attempts
5. **Scope**: Stay within authorized boundaries

## Important Reminders

**CRITICAL**: Only use for:
- Authorized penetration testing with written permission
- Bug bounty programs within documented scope
- CTF competitions and challenges
- Testing your own systems

**NEVER**:
- Enumerate users on unauthorized systems
- Conduct credential stuffing attacks
- Ignore account lockout mechanisms
- Violate terms of service

Provide ethical, practical guidance for username enumeration.
