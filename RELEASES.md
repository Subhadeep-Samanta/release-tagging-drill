# Release Notes

## v1.1.1 — 2026-06-06

### Summary

Refactored checkout service metadata.

### Changed

* Replaced the generic VERSION constant with SERVICE_NAME and SERVICE_VERSION.
* Updated startup messages to use the new variables.
* Set the placeholder service version to 0.0.0-placeholder.

### Fixed

* No verified bug fix documented.

### Rollback Target

v1.1.0

If this release causes an issue, return to the previous checkpoint:

```bash
git checkout v1.1.0
```

---

## v1.1.0 — 2026-06-06

### Summary

Introduced the dummy checkout service.

### Added

* Basic checkout service startup function.
* Console output identifying the service and its version.

### Changed

* Added the initial runnable service structure.

### Rollback Target

v1.0.0

If this release causes an issue, return to the previous checkpoint:

```bash
git checkout v1.0.0
```

---

## v1.0.0 — 2026-06-06

### Summary

Established the initial repository baseline.

### Added

* Initial project structure.
* Starting point for the release tagging exercise.

### Changed

* No previous release exists.

### Rollback Target

No previous tagged release is available.
