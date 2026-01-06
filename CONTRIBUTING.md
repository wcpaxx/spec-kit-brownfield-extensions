# Contributing to spec-kit Brownfield Bootstrap Extension

Thank you for your interest in contributing! This document provides guidelines for contributing to this project.

## How to Contribute

### Reporting Bugs

1. Check if the bug has already been reported in [Issues](https://github.com/wcpaxx/spec-kit-brownfield-extensions/issues)
2. If not, create a new issue with:
   - Clear description of the problem
   - Steps to reproduce
   - Expected vs actual behavior
   - Your environment (AI tool, OS, spec-kit version)

### Suggesting Enhancements

1. Open an issue with the `enhancement` label
2. Describe the use case and expected behavior
3. Explain why this enhancement would be useful

### Pull Requests

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test with your AI coding tool
5. Commit with clear messages (`git commit -m 'Add amazing feature'`)
6. Push to your branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## Development Guidelines

### Command File Structure

When modifying command files (`speckit.brownfield-bootstrap.md` or `speckit.brownfield-bootstrap-cn.md`):

1. **Frontmatter**: Keep the YAML frontmatter with description and handoffs
2. **User Input Section**: Always include `$ARGUMENTS` handling
3. **Directory Structure**: Never deviate from spec-kit's expected paths
4. **Self-Check Lists**: Maintain pre-output validation checks
5. **Phase Organization**: Follow the Discovery → Constitution → Templates → Validation flow

### Translation Guidelines

When updating translations:

1. Keep both English and Chinese versions in sync
2. Maintain consistent terminology
3. Preserve all technical details and code blocks
4. Test both versions work correctly

### Documentation

- Update README.md when adding features
- Keep examples current and tested
- Document any new prerequisites or compatibility changes

## Code of Conduct

- Be respectful and inclusive
- Focus on constructive feedback
- Help newcomers get started

## Questions?

Feel free to open an issue with the `question` label!
