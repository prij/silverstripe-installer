# Contributing to Silverstripe Installer

First off, thanks for taking the time to contribute! 🎉

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates.

When creating a bug report, include:

- **Clear title** describing the issue
- **Steps to reproduce** the behaviour
- **Expected behaviour** vs what actually happened
- **Your environment**: OS, Bash version (`bash --version`), Composer version
- **Terminal output** if relevant

### Suggesting Features

Feature suggestions are welcome! Please:

- Check existing issues/discussions first
- Clearly describe the feature and its use case
- Consider if it fits the project's scope (simple, focused installer)

### Pull Requests

1. Fork the repo and create your branch from `main`
2. Test your changes thoroughly
3. Update documentation if needed
4. Follow the existing code style
5. Write a clear PR description

## Code Style

- Use 4-space indentation
- Quote variables: `"${variable}"`
- Use `[[ ]]` for conditionals
- Add comments for non-obvious logic
- Keep functions focused and small

## Testing Your Changes

Before submitting:

```bash
# Test in an empty directory
mkdir /tmp/test-install && cd /tmp/test-install
/path/to/your/modified/ss-install.sh

# Test the warning for non-empty directories
touch testfile
/path/to/your/modified/ss-install.sh

# Clean up
rm -rf /tmp/test-install
```

## Questions?

Feel free to open an issue for any questions about contributing.
