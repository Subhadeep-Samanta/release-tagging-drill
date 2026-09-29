
# Release Versioning Convention

## 1. Semantic Versioning Rules

The team follows Semantic Versioning using the format:

MAJOR.MINOR.PATCH

### MAJOR

Increment MAJOR when introducing incompatible changes that require existing users or integrations to change.

Example:

v1.4.2 -> v2.0.0

### MINOR

Increment MINOR when adding new functionality in a backward-compatible manner.

Example:

v1.4.2 -> v1.5.0

### PATCH

Increment PATCH when fixing bugs or making backward-compatible corrections without adding new functionality.

Example:

v1.4.2 -> v1.4.3

## 2. Tag Naming Format

All production release tags must follow:

vMAJOR.MINOR.PATCH

Examples:

- v1.0.0
- v1.1.0
- v1.1.1
- v2.0.0

The lowercase `v` prefix is mandatory.

Names such as `release_2`, `latest-good`, `stable-build`, and `v2-final-FINAL` are not permitted for new releases.

## 3. Annotated Git Tags

All production releases must use annotated Git tags.

Annotated tags store a tag message, tagger information, and timestamp, making them more suitable for release records and auditing.

The required command is:

git tag -a v1.1.0 -m "Release 1.1.0: Added checkout validation"

Lightweight tags must not be used for production releases.

## 4. Pre-release Naming

Release candidates and beta versions use a suffix after the semantic version.

Examples:

- v1.5.0-beta.1
- v1.5.0-beta.2
- v1.5.0-rc.1
- v1.5.0-rc.2

Pre-release versions are ordered before the corresponding final release.

For example:

v1.5.0-beta.1 < v1.5.0-rc.1 < v1.5.0

The final release must not contain a pre-release suffix.

## 5. Release Management Rules

1. Every production release must have a unique semantic version.
2. Every release tag must point to the exact commit being deployed.
3. Release tags must be annotated with meaningful messages.
4. Every release must have a corresponding entry in RELEASE-MAP.md.
5. Release notes must document changes and the previous known-good rollback target.
6. Release tags must be pushed to the remote repository.
7. Existing release tags must not be silently moved or overwritten.