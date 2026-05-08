# VRA proposals

## VRA proposal for CVE-2026-40976

- Bump `org.springframework.boot:spring-boot` from `4.0.3` to `4.0.6`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40976 vulnerability exposes Actuator endpoints without proper authorization in Spring Boot 4.0.3, posing a security risk. Bumping to 4.0.6 resolves this by applying the necessary security fix. We will update the dependency in the build catalog and regenerate the lockfile to ensure consistency. The change is compatible with Spring Boot 3.1.x and JDK 17, with no functional impact.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot 4.0.3 → 4.0.6
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
