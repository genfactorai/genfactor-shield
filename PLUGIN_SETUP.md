# Genfactor Shield — Plugin Setup

This repository is configured as a Claude Code plugin marketplace.

## What's Included

### Plugin Marketplace Configuration

**Location**: `.claude-plugin/`

#### Marketplace Definition
- **`marketplace.json`** — Defines 7 security testing plugins:
  - `shield-fuzzing` — SQL/NoSQL/Command injection payloads
  - `shield-passwords` — Password wordlists
  - `shield-patterns` — API key and sensitive data patterns
  - `shield-payloads` — XSS, XXE, template injection
  - `shield-usernames` — Username wordlists
  - `shield-webshells` — Web shell samples for detection
  - `shield-llm` — LLM/AI security testing prompts

#### Plugin Manifest
- **`plugin.json`** — Main plugin metadata and configuration

### 5 Slash Commands

**Location**: `.claude-plugin/commands/`

1. **`test-sql-injection.md`** — SQL injection testing assistant
2. **`test-xss.md`** — XSS vulnerability testing
3. **`get-wordlist.md`** — Wordlist access helper
4. **`detect-webshell.md`** — Web shell detection (defensive)
5. **`scan-secrets.md`** — API key and secrets scanner

### 3 Specialized Agents

**Location**: `.claude-plugin/agents/`

1. **`pentest-advisor.md`** — Penetration Testing Advisor
2. **`ctf-assistant.md`** — CTF Competition Assistant
3. **`bug-bounty-hunter.md`** — Bug Bounty Hunter Advisor

## How Users Install

### Add Marketplace

```bash
/plugin marketplace add genfactorai/genfactor-shield
```

Then browse and install plugins:

```bash
/plugin
```

### Install Individual Plugins

```bash
/plugin install shield-fuzzing@genfactor-shield
/plugin install shield-passwords@genfactor-shield
/plugin install shield-patterns@genfactor-shield
/plugin install shield-payloads@genfactor-shield
/plugin install shield-usernames@genfactor-shield
/plugin install shield-webshells@genfactor-shield
/plugin install shield-llm@genfactor-shield
```

## How Users Use It

### Slash Commands

```bash
/test-sql-injection    # Interactive SQL injection guidance
/test-xss              # XSS testing assistance
/get-wordlist          # Access curated wordlists
/detect-webshell       # Defensive web shell detection
/scan-secrets          # Scan for exposed credentials
```

### Agents

```
"Help me with penetration testing using the pentest-advisor agent"
"Solve this CTF challenge using the ctf-assistant agent"
"Guide me through bug bounty hunting with the bug-bounty-hunter agent"
```

## Plugin Architecture

```
.claude-plugin/
├── marketplace.json              # Marketplace catalog with 7 plugins
├── plugin.json                   # Main plugin manifest
├── commands/                     # 5 interactive slash commands
│   ├── test-sql-injection.md
│   ├── test-xss.md
│   ├── get-wordlist.md
│   ├── detect-webshell.md
│   └── scan-secrets.md
├── agents/                       # 3 specialized expert agents
│   ├── pentest-advisor.md
│   ├── ctf-assistant.md
│   └── bug-bounty-hunter.md
└── QUICKSTART.md
```

## Testing the Marketplace

### Validate Structure

```bash
# Check all files exist
ls -R .claude-plugin/

# Validate JSON syntax
cat .claude-plugin/marketplace.json | python -m json.tool
cat .claude-plugin/plugin.json | python -m json.tool
```

### Test Installation (Local)

```bash
/plugin marketplace add ./
/plugin
/plugin install shield-fuzzing@genfactor-shield
```

## Credits

- **SecLists**: Original wordlists and payloads by Daniel Miessler
- **Claude Code**: Plugin system by Anthropic
- **Genfactor**: Curated and packaged by Genfactor

---

**Genfactor Shield** v1.0.0
