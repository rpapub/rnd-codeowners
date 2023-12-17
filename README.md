# R&D on GitHub Branch Protection and Team Permissions

## About the Repository

Welcome to the `rnd-codeowners` repository. The primary goal of this repository is to research and test various configurations related to GitHub branch protection rules, team permissions, and the usage (or non-usage) of the `CODEOWNERS` file in a collaborative development environment.

### Intention

- **Experimentation**: This repository serves as a testing ground to understand how different branch protection strategies and permission settings affect the development workflow in GitHub.
- **Learning & Documentation**: Through practical application, we aim to document the effects of various settings, particularly focusing on how they impact pull requests, code reviews, and the CI/CD pipeline setup using GitHub Actions.

### Key Focus Areas

- **Branch Protection Rules**: Investigating how different protection rules can be applied to branches like `main`, `integration`, `development/*`, and `feature/*`.
- **Team Roles & Permissions**: Understanding the impact of different permission levels assigned to teams like `pbp-developer`, `pbp-maintainer`, `global-owner`, `pbp-cicd-pipeline`, and `pbp-readonly`.
- **Pull Request Management**: Testing the pull request flow, especially who can open, review, and merge pull requests under various scenarios.
- **CI/CD Integration**: Examining how GitHub Actions work with protected branches and permission-limited pull requests.
- **`CODEOWNERS` Use Cases**: Exploring scenarios both with and without the `CODEOWNERS` file to determine its impact on repository management.

## Expected Behavior

- **Pull Requests to `integration`**: Can be created by anyone but can only be merged by members of `pbp-maintainer` or `global-owner`.
- **Pull Requests from `main` to `main`**: Can only be merged by `pbp-cicd-pipeline` or `global-owner`.
- **Developer Restrictions**: Members of `pbp-developer` can create branches and open pull requests but cannot merge them into `integration` or `main`.
- **CI/CD Pipeline Restrictions**: Automated workflows should not progress to release or deployment stages without appropriate approvals.
- **Contribution & Review**: All contributions are subject to review, aligning with the defined branch protection rules.

## Contributing

Contributors are encouraged to experiment with different settings and scenarios. Please document your findings and experiences in the issues or pull requests to enhance our collective understanding.

## Feedback and Questions

For any feedback or questions, feel free to open an issue in this repository. Your input is valuable in shaping the outcomes of this research.
