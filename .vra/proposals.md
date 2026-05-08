# VRA proposals

## VRA proposal for CVE-2026-22737

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.6, 6.2.17`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    CVE-2026-22737 exposes information disclosure via Java scripting engines in Spring Framework versions prior to 7.0.6 and 6.2.17. We will patch by bumping `spring-webmvc` to 7.0.6 and 6.2.17, then regenerate the dependency lockfile to ensure compatibility with Spring Boot 3.1.x and JDK 17. This fix addresses the vulnerability without affecting existing functionality.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.6, 6.2.17
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
