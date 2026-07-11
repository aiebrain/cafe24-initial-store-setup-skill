# Cafe24 Initial Store Setup Skill

A Hermes Agent skill for preparing a Korean Cafe24 self-hosted store before PG approval.

## What it covers

- Business, footer, customer-service, and privacy-manager information
- Company introduction and mobile service inquiry guidance
- Existing Cafe24 standard terms: company/store-name substitution checks
- Bank-transfer display consistency checks
- Public footer verification and PG-preapproval readiness checklist

The user performs login, MFA/OTP, identity verification, PG application, contracts, and document submission. The skill never invents business details, account details, or legal-policy content.

## Install

Copy the skill directory into your Hermes skills directory:

```bash
mkdir -p ~/.hermes/skills/ecommerce
cp -R skills/ecommerce/cafe24-initial-store-setup ~/.hermes/skills/ecommerce/
```

Restart Hermes or start a new session, then load it with:

```text
/skill cafe24-initial-store-setup
```

## Browser fallback

The skill uses an available interactive browser path in this order:

1. Existing Browser Harness / Chrome CDP
2. Hermes browser tool
3. Desktop browser with computer-use
4. Official Microsoft Playwright MCP installation and smoke test
5. Manual field-by-field guidance if no visible user-login browser is available

## Verification

```bash
hermes skills list
```

Confirm that `cafe24-initial-store-setup` is listed.

## Safety

Saving store configuration requires the user to provide the underlying business information and authorize the change. PG contracts, applications, payments, user login, and identity verification remain user actions.
