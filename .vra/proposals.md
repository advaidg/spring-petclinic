# VRA proposals

## VRA proposal for CVE-2026-42198

- Bump `org.postgresql:postgresql` from `4.0.3` to `42.7.11`
- Declared at `pom.xml` line 92
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-42198 vulnerability in pgjdbc allows client-side DoS via malicious SCRAM-SHA-256 authentication, impacting our current 42.7.10 dependency. Bumping to 42.7.11 resolves the issue via a patch_bump plan. We'll update the build catalog and regenerate the lockfile to ensure consistent dependency resolution. The fix is compatible with Spring Boot 3.1.x and JDK 17, with no expected breaking changes.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.postgresql:postgresql 42.7.10 → 42.7.11
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
