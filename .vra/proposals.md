# VRA proposals

## VRA proposal for CVE-2026-22733

- Bump `org.springframework.boot:spring-boot-starter-actuator` from `4.0.3` to `4.0.4`
- Declared at `pom.xml` line 44
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-22733 vulnerability in Spring Boot's Actuator endpoints allows authentication bypass when using CloudFoundry-specific endpoints, posing a security risk. Bumping to 4.0.4 resolves this issue by applying the upstream fix. We will update the dependency in the build catalog and regenerate the lockfile to ensure consistency. JDK compatibility is untested, so further validation may be required.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot-starter-actuator 4.0.3 → 4.0.4
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
