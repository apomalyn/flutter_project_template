# flutter_project_template

![Version](https://img.shields.io/github/v/tag/apomalyn/flutter_project_template?label=Latest%20version)

This repository is a template of CI for Flutter project.

## What this repo offer?

| Feature type | Name                   | Description                                                                                                                                                                 | Implementation status |
|--------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| CI           | Version tag validation | Check if the version of the application has been changed on each PR.                                                                                                        | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L14) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CI           | Test and checks        | Run `flutter test`, `flutter analyze` and `flutter format` on each PR.                                                                                                      | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L47) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CI           | Coverage               | - Comment the coverage percentage from lcov on each PR - Display the coverage percentage on a badge for the master branch                                                   | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L84) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CI           | Update goldens         | Sometimes updating goldens can be frustrating especially when you are multiple dev with different OS. The goal is to offer a simple way to update the goldens for everyone. | [![CI](https://img.shields.io/badge/CI-In_progress-orange.svg)]() [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CI           | Build                  | Build the application for Android (aab), iOS (ipa), MacOS, Linux, Windows and web                                                                                            | [![Android](https://img.shields.io/badge/Android-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L144) [![iOS](https://img.shields.io/badge/iOS-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L144) [![Web](https://img.shields.io/badge/Web-Not_started-red.svg)]() [![MacOS](https://img.shields.io/badge/MacOS-Not_started-red.svg)]() [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() [![Linux](https://img.shields.io/badge/Linux-Not_started-red.svg)]() [![Windows](https://img.shields.io/badge/Windows-Not_started-red.svg)]() |
| CI           | Github release         | When a PR lands in main branch, create a draft release (can be a pre-release also, your choice) with an automatic changelog and it's own version.                           | [![CI](https://img.shields.io/badge/CI-Done-green.svg)](https://github.com/apomalyn/flutter_project_template/blob/main/.github/workflows/main-workflow.yaml#L211) [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |
| CD           | Store release          | When a github release is published, the application should be sent to the stores.                                                       | [![Google Play Store](https://img.shields.io/badge/Google_Play_Store-Not_started-red.svg)]() [![iOS](https://img.shields.io/badge/Apple_App_Store-Not_started-red.svg)]() [![Doc](https://img.shields.io/badge/Doc-Not_started-red.svg)]() |

## Getting Started

### Setup gist for the code coverage

TODO

## Using

- [Split action](https://github.com/marketplace/actions/split-action) by JungWinter
- [Tag exists action](https://github.com/marketplace/actions/tag-exists-action) by mukunku
- [Flutter action](https://github.com/marketplace/actions/flutter-action) by subosito
- [LCOV reporter action](https://github.com/marketplace/actions/code-coverage-report) by romeovs
- [Dynamic badge action](https://github.com/marketplace/actions/dynamic-badges) by schneegans
- [Automatic releases action](https://github.com/marketplace/actions/automatic-releases) by marvinpinto