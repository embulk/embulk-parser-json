# embulk-guess-json

This is one of Embulk's "standard" plugins that are embedded in Embulk's executable binary distributions.

The source code had been managed in the same [main repository of Embulk](https://github.com/embulk/embulk) until [`v0.10.33`](https://github.com/embulk/embulk/tree/v0.10.33), and in the [`embulk-standards` repository](https://github.com/embulk/embulk-standards) until [`v0.10.42`](https://github.com/embulk/embulk-standards/tree/v0.10.42).

It has been maintained in the standalone repository since `v0.11.0`.

For Maintainers
----------------

### Release

Modify `version` in `build.gradle` at a detached commit, and then tag the commit with an annotation.

```
git checkout --detach master

(Edit: Remove "-SNAPSHOT" in "version" in build.gradle.)

git add build.gradle

git commit -m "Release vX.Y.Z"

git tag -a vX.Y.Z

(Edit: Write a tag annotation in the changelog format.)
```

See [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) for the changelog format. We adopt a part of it for Git's tag annotation like below.

```
## [X.Y.Z] - YYYY-MM-DD

### Added
- Added a feature.

### Changed
- Changed something.

### Fixed
- Fixed a bug.
```

Push the annotated tag, then. It triggers a release operation on GitHub Actions after approval.

```
git push -u origin vX.Y.Z
```
