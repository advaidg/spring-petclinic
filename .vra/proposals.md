# VRA proposals

## VRA proposal for CVE-2026-40972

- Bump `org.springframework.boot:spring-boot-devtools` from `4.0.3` to `4.0.6`
- Declared at `pom.xml` line 117
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40972 vulnerability in Spring Boot DevTools 4.0.3 exposes the application to timing attacks during remote secret comparison. Bumping to 4.0.6 resolves this issue by addressing the timing-based vulnerability in the devtools' secret comparison logic. We will refresh the dependency lockfile to ensure consistency post-bump. JDK compatibility is untested but likely unaffected, as the fix is a security patch without major API changes.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot-devtools 4.0.3 → 4.0.6
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
