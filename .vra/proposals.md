# VRA proposals

## VRA proposal for CVE-2026-22745

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.7, 6.2.18`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-22745 vulnerability in spring-webmvc 7.0.5 allows DoS via slow static resource resolution on Windows, which poses a security risk. Bumping to 7.0.7 or 6.2.18 resolves the issue while maintaining compatibility with Spring Boot 3.1.x and JDK 17. Regenerating the dependency lockfile ensures consistent and secure dependency resolution. This patch is low-risk and aligns with our security and compatibility requirements.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.7, 6.2.18
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
