# flutter_project_template

![Version](https://img.shields.io/github/v/tag/apomalyn/flutter_project_template?label=Latest%20version)
![Coverage Badge](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/apomalyn/63e992d7042dbac4db9abaecb78df0eb/raw/2dd431e3f59a5217a8dd051dd0253b07ca824019/flutter_project_template_badge_coverage.json)

This repository is a template of CI for Flutter project.

## What this repo offer?

| Feature type | Name                   | Description                                                                                                                                                                 | Implementation status |
|--------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| CI           | Version tag validation | Check if the version of the application has been changed on each PR.                                                                                                        | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L14) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CI           | Test and checks        | Run `flutter test`, `flutter analyze` and `flutter format` on each PR.                                                                                                      | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L47) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CI           | Coverage               | Comment the coverage percentage from lcov on each PR. Display the coverage percentage on a badge for the master branch                                                   | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L84) [![Doc](https://img.shields.io/badge/Doc-Done-green.svg)]() |
| CI           | Update goldens         | Sometimes updating goldens can be frustrating especially when you are multiple dev with different OS. The goal is to offer a simple way to update the goldens for everyone. | [![CI](https://img.shields.io/badge/CI-Done-green.svg)]() [![Doc](https://img.shields.io/badge/Doc-Done-green.svg)]() |
| CI           | Build                  | Build the application for Android (aab), iOS (ipa), MacOS, Linux, Windows and web                                                                                            | [![Android](https://img.shields.io/badge/Android-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L144) [![iOS](https://img.shields.io/badge/iOS-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L144) [![Web](https://img.shields.io/badge/Web-Not_started-red.svg)]() [![MacOS](https://img.shields.io/badge/MacOS-Not_started-red.svg)]() [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() [![Linux](https://img.shields.io/badge/Linux-Not_started-red.svg)]() [![Windows](https://img.shields.io/badge/Windows-Not_started-red.svg)]() |
| CI           | Github release         | When a PR lands in main branch, create a draft release (can be a pre-release also, your choice) with an automatic changelog and it's own version.                           | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L211) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CD           | Store release          | When a github release is published, the application should be sent to the stores.                                                       | [![Google Play Store](https://img.shields.io/badge/Google_Play_Store-Not_started-red.svg)]() [![iOS](https://img.shields.io/badge/Apple_App_Store-Not_started-red.svg)]() [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |

## Use the CI

### Setup gist for the code coverage badge

Big thanks to _The Jared Wilcurt_ for the technique explained [here](https://dev.to/thejaredwilcurt/coverage-badge-with-github-actions-finally-59fa).

1. First you need to create a **public gist** in [Github gist](gist.github.com). Copy the id of the gist (you can find it in the URL just after your username).
2. Create a secret called `GIST_ID_COVERAGE_BADGE` with the ID of the created gist as value.
3. Create a [developer token](https://github.com/settings/tokens) with the `gist` scope. Copy the token.
4. Create a secret called `GIST_COVERAGE_BADGE_TOKEN` with the token just created at the previous step as value.
5. Do not forget to copy `scripts/ci_determine_coverage_percentage.sh` in your repository.
6. Add this badge to your README: `[![Coverage Badge](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/<YOUR_USERNAME>/<YOUR_GIST_ID>/raw/<REPOSITORY_NAME>_master_badge_coverage.json)]`
7. There you go! :smile:

### Commit goldens files

When you wish to regenerate the goldens files of your project, simply add `[CI UPDATE GOLDENS]` to your commit message.
The CI will update all the goldens files during the `testing` job then will push the new/updated files. 

:warning: Your goldens files have to be stored under the `test` folder of the project. Otherwise, update `Commit golden files`
step under the `testing` job. :warning:

#### Setup

1. Create a [developer token](https://github.com/settings/tokens) with the `repo` scope. Copy the token.
2. Create a secret called `PAT` with the token just created at the previous step.
3. Enjoy! :smile:

## Using the following actions

- [Split action](https://github.com/marketplace/actions/split-action) by JungWinter
- [Tag exists action](https://github.com/marketplace/actions/tag-exists-action) by mukunku
- [Flutter action](https://github.com/marketplace/actions/flutter-action) by subosito
- [LCOV reporter action](https://github.com/marketplace/actions/code-coverage-report) by romeovs
- [Dynamic badge action](https://github.com/marketplace/actions/dynamic-badges) by schneegans
- [Automatic releases action](https://github.com/marketplace/actions/automatic-releases) by marvinpinto
- [Auto commit action](https://github.com/marketplace/actions/git-auto-commit) by stefanzweifel
