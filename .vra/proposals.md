# VRA proposals

## VRA proposal for CVE-2026-22741

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.7, 6.2.18`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    CVE-2026-22741 allows DoS via cache poisoning in Spring WebFlux and MVC, impacting our current 7.0.5 version. Bumping to 7.0.7 or 6.2.18 resolves the vulnerability while maintaining compatibility with Spring Boot 3.1.x and JDK 17. Regenerating the dependency lockfile ensures consistent resolution. This patch_bump is low-risk and aligns with our security and dependency hygiene standards.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.7, 6.2.18
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
