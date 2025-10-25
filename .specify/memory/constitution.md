# Account Dashboard Web Constitution


## Core Principles

### I. JSON-Driven Layouts
All dashboard layouts and widget configurations MUST be defined in JSON files. No hardcoded UI layouts are permitted. This ensures flexibility, portability, and enables non-developers to modify dashboards.

### II. Widget Rendering
The app MUST support rendering a set of reusable widgets (charts, tables, text, etc.) based on the JSON configuration. Widgets MUST be independently testable and accept only JSON-defined props.

### III. Static Hosting & Offline Access
The app MUST be deployable as a static site (no server-side code required at runtime). All assets, configs, and data required for rendering MUST be available at build or load time. The app MUST support offline access for all dashboard features, using browser storage and caching.

### IV. Testability
All layouts and widgets MUST have automated tests verifying correct rendering for valid and invalid JSON configurations. Test coverage MUST include edge cases and error handling for malformed configs.

### V. Simplicity & Maintainability
The codebase MUST avoid unnecessary complexity. Prefer declarative, composable patterns. All features MUST be documented and easy to extend with new widgets or layouts.


## Additional Constraints

- Technology stack MUST be HTML5, JavaScript, and CSS3. All client logic MUST run in the browser.
- Local data storage MUST use SQLite (via WebAssembly or browser-supported SQLite solution) for dashboard state and widget data.
- The app MUST support cloud storage integration for dashboard configs and user data (e.g., via REST API or cloud file storage).
- Caching and eviction policies MUST be implemented for dashboard data and widgets, with clear rules for when data is refreshed or removed.
- Offline access is REQUIRED: all dashboard features MUST work without network connectivity, using cached or local data.
- No runtime secrets or server dependencies allowed.
- All configuration files MUST be version-controlled.


## Development Workflow

- All changes MUST be peer-reviewed.
- Automated tests MUST pass before merge.
- New widgets or layouts MUST include documentation and example JSON configs.


## Governance

- This constitution supersedes all other project practices.
- Amendments require documentation, approval by project maintainers, and a migration plan if breaking changes are introduced.
- All PRs and reviews MUST verify compliance with the constitution.
- Versioning follows semantic versioning: MAJOR for breaking/removal, MINOR for new principles/sections, PATCH for clarifications.
- Compliance reviews are required at each release.

<!--
Sync Impact Report
Version change: 0.0.0 → 1.0.0
List of modified principles: N/A (initial version)
Added sections: All (initial constitution)
Removed sections: None
Templates requiring updates: plan-template.md ✅, spec-template.md ✅, tasks-template.md ✅
Follow-up TODOs: TODO(RATIFICATION_DATE): Set original adoption date
-->

<!--
Sync Impact Report
Version change: 1.0.0 → 1.1.0
List of modified principles: III. Static Hosting → III. Static Hosting & Offline Access
Added sections: Technology stack, SQLite, cloud storage, caching/eviction, offline access
Removed sections: None
Templates requiring updates: plan-template.md ✅, spec-template.md ✅, tasks-template.md ✅
Follow-up TODOs: TODO(RATIFICATION_DATE): Set original adoption date
-->

**Version**: 1.1.0 | **Ratified**: TODO(RATIFICATION_DATE): Set original adoption date | **Last Amended**: 2025-10-25
