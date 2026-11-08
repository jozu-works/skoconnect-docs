# Sonar Scope Alignment Quality Gate Contract

## Scope Definition

| Path | Language | Quality Gate Tool | Coverage Tool |
|------|----------|-------------------|---------------|
| `functions/` | TypeScript | SonarCloud | Jest |
| `admin-web/` | TypeScript | SonarCloud | Jest |
| `mobile/` | Dart | Flutter CI (`flutter analyze`) | Flutter CI (`flutter test`) |

## SonarCloud Scope (JS/TS Only)

**In Scope:**
- `functions/**/*.ts` — Cloud Functions (TypeScript)
- `admin-web/**/*.ts` — Admin portal (TypeScript)

**Out of Scope (Excluded):**
- `mobile/**` — All Flutter/Dart code
- `**/*.dart` — Dart files everywhere
- Test files: `**/*.test.ts`, `**/*.spec.ts`
- Config files: `**/firebase.json`, `**/tsconfig.json`, `**/.eslintrc*`

**Sonar Quality Gate Thresholds:**
- Coverage: ≥80% on new code
- Duplicated lines: ≤3% on new code
- Maintainability Rating: B or better on new code
- Reliability Rating: C or better on new code
- Security Rating: C or better on new code

## Flutter CI Scope (Dart Only)

**In Scope:**
- `mobile/**/*.dart` — All Flutter app code
- Generated files excluded from analysis

**Flutter CI Quality Gate Thresholds:**
- `flutter analyze`: Zero errors, zero warnings
- `flutter test`: 100% test pass rate

## Release Gate Decision Table

A PR is **release-ready** when it passes the relevant gate for its changed paths:

| Changed Path(s) | Sonar Gate | Flutter CI Gate | Release Status |
|-----------------|------------|-----------------|----------------|
| `functions/` only | ✅ PASS | N/A | ✅ READY |
| `admin-web/` only | ✅ PASS | N/A | ✅ READY |
| `mobile/` only | N/A | ✅ PASS | ✅ READY |
| `functions/` + `admin-web/` | ✅ PASS | N/A | ✅ READY |
| `functions/` + `mobile/` | ✅ PASS | ✅ PASS | ✅ READY |
| `admin-web/` + `mobile/` | ✅ PASS | ✅ PASS | ✅ READY |
| All three paths | ✅ PASS | ✅ PASS | ✅ READY |
| Any path with ❌ FAIL | ❌ FAIL | ❌ FAIL | ❌ BLOCKED |

**Zero Tolerance Rule:** If a PR touches code in a gated path, that path's gate must pass. There is no "partial coverage."

## CI Enforcement

### SonarCloud CI
- Runs on: PRs touching `functions/` or `admin-web/`
- Reports: SonarCloud quality gate status on PR
- Scope: Automatically excludes `mobile/**` via `sonar.exclusions` property

### Flutter CI
- Runs on: PRs touching `mobile/`
- Reports: `flutter analyze` and `flutter test` results
- Fails fast: Blocks merge on any analysis error or test failure

## Configuration Reference

**SonarCloud `sonar-project.properties`:**
```properties
sonar.exclusions=mobile/**,**/*.test.ts,**/*.spec.ts,**/firebase.json,**/tsconfig.json,**/.eslintrc*
sonar.coverage.exclusions=mobile/**,**/*.test.ts,**/*.spec.ts
sonar.typescript.lcov.reportPaths=coverage/lcov.info
```

**Flutter CI (`.github/workflows/flutter-ci.yml`):**
```yaml
jobs:
  analyze-and-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: subosito/flutter-action@v2
      - run: flutter analyze
      - run: flutter test --coverage
```

## Glossary

- **Sonar Gate:** SonarCloud quality gate status for JS/TS paths only
- **Flutter CI Gate:** `flutter analyze` + `flutter test` results for Dart paths only
- **Release-Ready:** PR passes all applicable gates for its changed code paths
- **Blocked:** PR fails any applicable gate — cannot merge
