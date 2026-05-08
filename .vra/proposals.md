# VRA proposals

## VRA proposal for CVE-2026-22741

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.7, 6.2.18`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    CVE-2026-22741 allows DoS via cache poisoning in Spring MVC and WebFlux, affecting version 7.0.5. We are patching by upgrading to 7.0.7 (preferred) or 6.2.18, both of which contain the fix. The dependency lockfile will be regenerated to ensure consistency. The change is compatible with Spring Boot 3.1.x and JDK 17.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.7, 6.2.18
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
