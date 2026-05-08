# VRA proposals

## VRA proposal for CVE-2026-41901

- Bump `org.thymeleaf:thymeleaf-spring6` from `3.1.3.RELEASE` to `3.1.5.RELEASE`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-41901 vulnerability in Thymeleaf's sandboxed expressions allows improper recognition of unauthorized syntax patterns, posing a security risk. Bumping to 3.1.5.RELEASE resolves this issue. The patch is compatible with Spring Boot 3.1.x and JDK 17, and can be implemented by updating the dependency in the build catalog and regenerating the lockfile. No code changes are required.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.thymeleaf:thymeleaf-spring6 3.1.3.RELEASE → 3.1.5.RELEASE
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
