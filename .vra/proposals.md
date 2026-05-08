# VRA proposals

## VRA proposal for CVE-2026-42198

- Bump `org.postgresql:postgresql` from `4.0.3` to `42.7.11`
- Declared at `pom.xml` line 92
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-42198 vulnerability in pgjdbc allows for client-side DoS via malicious SCRAM-SHA-256 authentication, which is resolved in version 42.7.11. We will patch by bumping the dependency to 42.7.11 and regenerating the lockfile to ensure compatibility with Spring Boot 3.1.x and JDK 17. This change is low-risk and requires no code changes.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.postgresql:postgresql 42.7.10 → 42.7.11
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
