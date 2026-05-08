# VRA proposals

## VRA proposal for CVE-2026-22737

- Bump `org.springframework:spring-webmvc` from `7.0.5` to `7.0.6, 6.2.17`
- Note: VRA could not auto-edit the version line — apply manually.
- `<narrative>` — Plan rationale
    The CVE-2026-22737 vulnerability in Spring Framework's Java scripting engine allows information disclosure via template views, posing a security risk. We are addressing this by patching the affected `spring-webmvc` dependency from 7.0.5 to 7.0.6 and 6.2.17, which include the fix. The update is compatible with Spring Boot 3.1.x and JDK 17, ensuring minimal disruption. Regenerating the dependency lockfile ensures consistency across the build.
- `gradle/libs.versions.toml` — Bump version in build catalog
    org.springframework:spring-webmvc 7.0.5 → 7.0.6, 6.2.17
- `gradle.lockfile` — Refresh resolved dependency lockfile
    regenerate via ./gradlew dependencies --write-locks
