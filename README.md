# Crash-Release-Dataset

## list_of_versions_that_introduce_crashes.txt

The data is provided in CSV format with three columns:

- **PROJECT**: The name of the Android project
- **INTRODUCE**: Git commit hash of the release that introduced the crash
- **FIX**: Git commit hash of the release that fixed the crash

## Data Source

The crashing releases in this dataset were identified from previous work.

## log_of_crashes.txt

This file contains the commit messages that identified releases as crashing releases. Each entry shows the commit hash and the relevant message that indicated a crash was fixed.

## File Format

The data follows this structure:
```
PROJECT:COMMIT_HASH
Commit Message
```

Where:
- **PROJECT**: The name of the Android project
- **COMMIT_HASH**: Commit hash
- **COMMIT_MESSAGE**: The commit message that indicates a crash was fixed
