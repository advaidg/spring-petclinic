# VRA proposals

## VRA proposal for CVE-2026-40976

- Bump `org.springframework.boot:spring-boot` from `4.0.3` to `4.0.6`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40976 vulnerability affects Spring Boot's default security configuration when Actuator is present but Health endpoints are not restricted, exposing potential unauthorized access. Bumping to 4.0.6 resolves this by updating the security filter chain to enforce authorization rules. We will update the build catalog and regenerate the dependency lockfile to ensure compatibility with Spring Boot 3.1.x and JDK 17. No code changes are required, making this a low-risk, high-impact patch.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot 4.0.3 → 4.0.6
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
