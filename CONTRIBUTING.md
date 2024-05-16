# Rain contribution guidelines

Thank you for your interest in contributing to Rain!

Our project demands high reliability and security as it involves financial transactions in a decentralized environment. This document covers how you can contribute effectively

## Bug reports

If you find a bug, please open an issue with a detailed report. Your bug report should include:
- Steps to reproduce.
- The version of Raindex, or the commit for the library/contract you are using.
- Your environment details (e.g. Mac/Windows).

If the bug is related to the app, please provide a video or screenshots showing the issue.

If the bug is related to one of the Rain libraries, provide a minimal code example that reproduces the bug.

## Submitting a Pull Request (PR)

Contributions to the Rain codebase happen via Pull Requests.

When you start a new PR there will be a template. Please complete this to the best of your ability before submitting the PR.

Otherwise, there are some basic guidelines for PR submission.

- **Small PRs:** Make small, clear PRs that logically group changes and make them easier to review.
- **Descriptive Titles:** Use descriptive titles and descriptions in your pull requests to explain the why and what of your changes.
- **Link Issues:** Reference any relevant issues or other pull requests.
- **Tests**: See next section.

### Chaining PRs

Sometimes you may need to "chain" PRs, meaning each merges into the next vs merging directly into main.

There's two reasons you may decide to chain your PRs:
- Your changes are spread across multiple repos and one is a dependency of the other
- The task at hand is too large for a single PR and needs to be split into parts

If neither of these are the case, please do not chain your PRs, as it:

- introduces artificial dependencies, making it harder to manage/merge priorities
- is error prone if the base branch is not manually updated along the chain each merge
- can make it more difficult to understand each PR if the review structure implies logical complection where none exists

### Testing and Quality Assurance

We are building open source financial software that operates in a highly adversarial environment. It handles real money onchain, is permissionless and we have no admin keys or control over code running in production.

This is exciting for what it enables, but also implies high risks in the face of bugs and security vulnerabilities in the code. Therefore:

- **Mandatory testing:** All code contributions must be thoroughly tested in a codified and reproduceable way on CI infrastructure, e.g. unit testing, fuzzing, benchmarking, simulating etc.
- **Write testable code:** Writing tests for code is not an afterthought, it impacts how code is structured from the ground up. If you regularly unit test your code, you will understand the myriad of ways that logic has to be broken down and structured to be testable in the first place.

### Code without tests
If there is a valid reason to submit a pull request without accompanying tests, you must demonstrate this somehow. For example, this could be linking to the lines of code where testing is already happening. If code is submitted without tests and without explanation, it won't be reviewed.

