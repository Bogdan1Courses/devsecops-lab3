STRIDE Category	Threat Example	Mitigation
Spoofing	Attacker impersonates a developer via stolen GitHub PAT	Enforce MFA, use short-lived tokens, require signed commits
Tampering	Attacker modifies CI workflow file in a PR (PPE attack)	Protect workflow files via CODEOWNERS, require reviews
Repudiation	Unsigned commits — no proof who made a change	Require GPG-signed commits, enable audit logging
Info Disclosure	AWS credentials leaked in build logs	Mask secrets in CI, use OIDC instead of static keys
Denial of Service	Fork bomb or infinite loop in CI consuming runner resources	Set job timeouts, use concurrency limits
Elevation of Privilege	GITHUB_TOKEN with write permissions exploited via PPE	Set minimum token permissions (contents: read)
