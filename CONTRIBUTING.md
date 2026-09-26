# Contributing to WhAlert

Thank you for your interest in contributing to WhAlert! We welcome contributions from everyone.

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

## How to Contribute

### Reporting Issues

If you find a bug or have a feature request:

1. **Search existing issues** to see if it's already been reported
2. **Create a new issue** with a clear title and description
3. **Include as much detail as possible**:
   - Steps to reproduce the issue
   - Expected vs. actual behavior
   - Screenshots (if applicable)
   - Device information (Android version, device model)
   - App version

### Suggesting Features

We welcome feature suggestions! Please:

1. **Create an issue** with the "enhancement" label
2. **Explain the use case** - Why would this feature be useful?
3. **Describe the proposed solution** - How should it work?
4. **Consider the scope** - Is this a small change or a major feature?

### Pull Requests

We accept pull requests! Here's how to contribute code:

1. **Fork the repository** and create a new branch
2. **Make your changes** following our coding standards
3. **Test your changes** thoroughly
4. **Update documentation** if needed
5. **Submit a pull request** with a clear description

## Development Setup

### Prerequisites

- Android Studio (latest stable version)
- Java JDK 17 or higher
- Android SDK (API 24+)
- Git

### Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/mamadoubdoumbia9-sudo/My-room.git
   cd My-room/WhAlert
   ```

2. Open the project in Android Studio

3. Build the project to ensure everything compiles

4. Run the app on an emulator or physical device

### Project Structure

```
WhAlert/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/whalert/app/
│   │   │   │   ├── data/           # Data layer (repositories, models)
│   │   │   │   ├── di/             # Dependency injection
│   │   │   │   ├── domain/         # Domain layer (use cases)
│   │   │   │   ├── presentation/   # UI layer (screens, viewmodels)
│   │   │   │   └── util/           # Utility classes
│   │   │   └── res/               # Resources
│   │   └── test/                 # Unit tests
│   └── build.gradle.kts
├── build.gradle.kts
└── settings.gradle.kts
```

## Coding Standards

### Kotlin

- Follow [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html)
- Use meaningful variable and function names
- Keep functions small and focused
- Use null safety features (non-null types where possible)
- Prefer immutability (val over var)
- Use data classes for simple data containers

### Architecture

- Follow MVVM (Model-View-ViewModel) pattern
- Keep business logic in the domain layer
- Keep data access in the data layer
- Keep UI logic in the presentation layer
- Use dependency injection (Koin)
- Keep ViewModels thin (move logic to use cases)

### Jetpack Compose

- Follow [Compose Best Practices](https://developer.android.com/jetpack/compose/best-practices)
- Keep composables small and focused
- Use state hoisting for composables
- Avoid business logic in composables
- Use Material Design 3 components
- Follow accessibility best practices

### Naming Conventions

- **Classes**: PascalCase (e.g., `ReportViewModel`)
- **Functions**: camelCase (e.g., `getReportById`)
- **Variables**: camelCase (e.g., `reportId`)
- **Constants**: UPPER_SNAKE_CASE (e.g., `MAX_REPORT_LENGTH`)
- **Files**: snake_case (e.g., `report_detail_screen.kt`)
- **Packages**: lowercase (e.g., `com.whalert.app.data`)

### Code Formatting

- Use the official Kotlin code style (configured in the project)
- Run `ktfmt` or `ktlint` before committing
- Keep line lengths under 100 characters when possible

## Testing

### Unit Tests

- Test business logic in the domain layer
- Test ViewModel logic
- Test utility functions
- Use Mockito for mocking dependencies
- Use JUnit for test framework

### UI Tests

- Test critical user flows
- Test accessibility
- Use Espresso for UI testing
- Use Compose testing tools for Compose UI

### Test Coverage

- Aim for 80%+ test coverage
- Focus on critical paths first
- Test edge cases
- Keep tests maintainable

## Commit Guidelines

### Commit Messages

Use [Conventional Commits](https://www.conventionalcommits.org/) format:

```
type(scope): description

body

footer
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Build or dependency updates

Example:
```
feat(report): add evidence attachment support

- Add ability to attach screenshots to reports
- Add image picker integration
- Update UI to display attached evidence

Closes #123
```

### Commit Content

- Keep commits small and focused
- Each commit should do one thing
- Include tests with new features
- Update documentation when needed

## Pull Request Guidelines

### PR Title

Use the same format as commit messages:
```
feat(report): add evidence attachment support
```

### PR Description

Include:
- **What** the PR does
- **Why** it's needed
- **How** it was implemented
- **Screenshots** (if UI changes)
- **Testing** done
- **Related issues** (use "Closes #123" to auto-close)

### PR Checklist

Before submitting a PR, make sure:

- [ ] Code compiles without errors
- [ ] All existing tests pass
- [ ] New tests are added for new functionality
- [ ] Documentation is updated (if needed)
- [ ] Code follows the project's coding standards
- [ ] No sensitive information is included
- [ ] The PR is focused on one feature/fix

## Review Process

1. **Initial Review**: A maintainer will review your PR within 3-5 business days
2. **Feedback**: You may receive feedback or requests for changes
3. **Updates**: Make the requested changes and push new commits
4. **Approval**: Once approved, a maintainer will merge your PR
5. **Release**: Your changes will be included in the next release

## Release Process

### Versioning

WhAlert uses [Semantic Versioning](https://semver.org/):

- **Major** (X.0.0): Breaking changes
- **Minor** (0.X.0): New features (backward compatible)
- **Patch** (0.0.X): Bug fixes (backward compatible)

### Release Steps

1. Update version in `build.gradle.kts`
2. Update `CHANGELOG.md`
3. Create a Git tag
4. Build and publish the APK
5. Update GitHub releases
6. Announce the release

## Security

If you discover a security vulnerability:

1. **Do not** create a public issue
2. **Email** the maintainers privately
3. Allow reasonable time for a fix before public disclosure

## License

By contributing to WhAlert, you agree that your contributions will be licensed under the same [MIT License](LICENSE) as the project.

## Questions?

If you have questions about contributing, please:

1. Check this document
2. Check the [FAQ](README.md#faq)
3. Create an issue with your question

We're happy to help!

---

*Thank you for contributing to WhAlert!*
