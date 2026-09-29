# Release Map

## Release History

| Version (Tag) | Commit (Short Hash) | Date       | What Shipped                                          |
| ------------- | ------------------- | ---------- | ----------------------------------------------------- |
| v1.0.0        | 4febcc6             | 2026-06-06 | Initial repository baseline                           |
| v1.1.0        | c17d4c4             | 2026-06-06 | Introduced dummy checkout service                     |
| v1.1.1        | 82535d9             | 2026-06-06 | Refactored checkout service name and version metadata |

## Rollback Traceability

### 1. View Release History

```bash
git tag --sort=-v:refname
```

### 2. Identify Current Release

```bash
git describe --tags --abbrev=0
```

### 3. Inspect Previous Release

```bash
git show --no-patch v1.1.0
```

### 4. Roll Back to Last Known-Good Checkpoint

```bash
git checkout v1.1.0
```

After verification, redeploy the selected commit using the deployment process.

### Explanation

The consistent semantic versioning convention allows the team to identify releases and their corresponding commits precisely. Annotated tags provide release information, while the release map documents what each checkpoint contains. This makes rollback reproducible and reduces the uncertainty caused by the previous inconsistent tag history.

**Note:** These are exercise release checkpoints. Historical production deployment of these versions has not been independently verified.
