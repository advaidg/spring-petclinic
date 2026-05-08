# VRA proposals

## VRA proposal for CVE-2026-22735

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.6, 6.2.17`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-22735 vulnerability in Spring WebMVC and WebFlux can lead to stream corruption when handling Server-Sent Events, posing a data integrity risk. Bumping spring-webmvc to 7.0.6 and 6.2.17 addresses the issue with minimal impact, as both versions are compatible with Spring Boot 3.1.x and JDK 17. Regenerating the dependency lockfile ensures consistency across the build. This patch is low-risk and aligns with our security and compatibility constraints.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.6, 6.2.17
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
