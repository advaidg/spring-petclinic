# VRA proposals

## VRA proposal for CVE-2026-22737

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.6, 6.2.17`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-22737 vulnerability in Spring Framework's Java scripting engine allows information disclosure via template views, impacting our current version 7.0.5. We will address this by patching to 7.0.6 (preferred) and 6.2.17, which include the fix. The migration involves bumping the version in the build catalog and regenerating the dependency lockfile via Gradle. These changes are compatible with Spring Boot 3.1.x and JDK 17, ensuring minimal disruption.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.6, 6.2.17
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
