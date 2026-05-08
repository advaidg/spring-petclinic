# VRA proposals

## VRA proposal for CVE-2026-40477

- Bump `org.thymeleaf:thymeleaf-spring6` from `3.1.3.RELEASE` to `3.1.4.RELEASE`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40477 vulnerability in Thymeleaf allows server-side template injection via a security bypass in expression execution, posing a serious security risk. Bumping to 3.1.4.RELEASE addresses the vulnerability by fixing the security bypass. The dependency lockfile will be regenerated to ensure consistent and secure dependency resolution. This change is compatible with Spring Boot 3.1.x and JDK 17, with no functional impact.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.thymeleaf:thymeleaf-spring6 3.1.3.RELEASE → 3.1.4.RELEASE
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
