# EnvSync | Environment Synchronizer

<p align="center">
  <img src="https://img.shields.io/badge/DevOps-Environment%20Sync-4ECDC4?style=for-the-badge" alt=""/>
  <img src="https://img.shields.io/badge/Platform-Cross--Platform-FF6B6B?style=for-the-badge" alt=""/>
</p>

---

### Sync environment variables across your projects

Keep your development, staging, and production environment variables in sync without the headache.

```bash
# Export from current shell
envsync export > .env.example

# Import from file
envsync import .env.production

# Compare environments
envsync diff .env.dev .env.prod
```

---

## Why EnvSync?

- 🔄 **Bidirectional sync** - Import/export any direction
- 📊 **Diff view** - Compare environments visually
- 🔒 **Secure** - Never commits secrets to git
- 🎯 **Type-safe** - Validates types on import
- 📝 **Template support** - Generate .env templates

---

## Installation

```bash
# Script (fastest)
curl -sSL https://raw.githubusercontent.com/simplestar-992/envsync/main/envsync | bash

# From source
git clone https://github.com/simplestar-992/envsync.git
cd envsync && go build -o envsync envsync
```

---

## Usage

```bash
# Export current env to file
envsync export -o .env

# Export with values masked
envsync export -mask -o .env.example

# Import from file
source <(envsync export)

# Diff two env files
envsync diff .env.dev .env.prod

# Sync between files
envsync sync -source .env.dist -target .env
```

---

MIT © 2024 [simplestar-992](https://github.com/simplestar-992)
