# VRA proposals

## VRA proposal for CVE-2026-40976

- Bump `org.springframework.boot:spring-boot` from `4.0.3` to `4.0.6`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40976 vulnerability affects Spring Boot's default security configuration when Actuator is present but Health endpoints are exposed without authorization. Bumping to 4.0.6 resolves this by updating the security filter chain to enforce proper authorization rules. We will update the dependency in the build catalog and regenerate the lockfile to ensure compatibility with Spring Boot 3.1.x and JDK 17. This patch is low-risk and aligns with our security remediation priorities.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot 4.0.3 → 4.0.6
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
