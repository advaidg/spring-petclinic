# VRA proposals

## VRA proposal for CVE-2026-40477

- Bump `org.thymeleaf:thymeleaf-spring6` from `3.1.3.RELEASE` to `3.1.4.RELEASE`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-40477 vulnerability in Thymeleaf allows server-side template injection via a security bypass in expression execution, posing a serious security risk. Bumping to 3.1.4.RELEASE resolves this issue by addressing the underlying flaw. The update is compatible with Spring Boot 3.1.x and JDK 17, ensuring no functional disruption. Regenerating the dependency lockfile ensures consistency across the build.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.thymeleaf:thymeleaf-spring6 3.1.3.RELEASE → 3.1.4.RELEASE
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
