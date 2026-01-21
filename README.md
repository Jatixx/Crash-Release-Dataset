# Crash-Release-Dataset

## list_of_versions_that_introduce_crashes.txt

The data is provided in CSV format with three columns:

- **PROJECT**: The name of the Android project
- **INTRODUCE**: Git commit hash of the release that introduced the crash
- **FIX**: Git commit hash of the release that fixed the crash

These are the crashing releases from the previous work.


## mobile_app_releases.csv
This dataset contains metrics and labels for mobile app releases, including crash labels. It extends the work from "Predicting Crashing Releases of Mobile Applications" (Xia et al., 2016) by incorporating new labels while maintaining the same metrics for each release.

## File Format

The data is provided in CSV format with the following columns:

### Identification Metrics
- **project**: The name of the Android project
- **HASH**: Git commit hash of the release
- **DATE**: Release date

### Complexity Dimension
- **Cyclomatic**: cyclomatic complexity - the number of branching paths within code in all source code files in a release.
### Time Dimension
- **PreDays**: Number of days since the previous release.

### Code Dimension
- **LA**: Lines Added
- **LD**: Lines Deleted
- **SIZE**: Total number of lines of code in the current release
- **SAME**: Number of source code files that are modified by both the current and previous release.
- **CUR_file**: Number of source code files in the current release
- **PREV_file**: Number of modified source code files in the previous release

### Diffusion Dimension
- **Top_NS**: Number of unique top-level subsystems changed between two releases.
- **Bottom_NS**: Number of unique bottom-level subsystems changed between two releases.
- **NF**: Number of unique files that have changed between two releases.
- **File_entropy**: Distribution of modified files across the release.
- **Churn_entropy**: Distribution of modified code across the application.

### Commit Dimension
- **NC**: Number of Commits
- **NFC**: Number of bug-Fixing Commits
  
### Text Dimension (Scores from Commit Messages)
- **Fuzzy_score**: Fuzzy set scores of commit logs
- **NB_score**: Naive Bayes scores of commit logs
- **NBM_score**: Naive Bayes Multinomial scores of commit logs
- **DMN_score**: Discriminative Naive Bayes Multinomial scores
- **COMP_score**: Complement Naive Bayes scores

### Label
- **crash_label**: Classification label (CRASH or NON_CRASH)

## Data Source

This CSV file contains new labels while maintaining the same metrics for each release:

