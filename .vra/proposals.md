# VRA proposals

## VRA proposal for CVE-2026-40972

- Bump `org.springframework.boot:spring-boot-devtools` from `4.0.3` to `4.0.6`
- Declared at `pom.xml` line 117
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    This migration addresses CVE-2026-40972, a timing attack vulnerability in Spring Boot DevTools' secret comparison mechanism. Bumping to 4.0.6 resolves the issue by implementing constant-time comparison. We will refresh the dependency lockfile to ensure consistency. JDK compatibility is untested but likely unchanged, so no additional changes are required.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot-devtools 4.0.3 → 4.0.6
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
