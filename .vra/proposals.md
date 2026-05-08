# VRA proposals

## VRA proposal for CVE-2026-40973

- Bump `org.springframework.boot:spring-boot` from `4.0.3` to `4.0.6, 3.5.14`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40973 vulnerability in Spring Boot 4.0.3 allows arbitrary code execution and session hijacking via predictable temporary directories, posing a severe security risk. We are addressing this by bumping to fixed versions 4.0.6 and 3.5.14, which resolve the issue. The dependency lockfile will be regenerated to ensure consistent and secure dependency resolution. This change is compatible with Spring Boot 3.1.x and JDK 17, with no expected breaking changes.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework.boot:spring-boot 4.0.3 → 4.0.6, 3.5.14
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
