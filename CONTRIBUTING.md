# Contributing to RemTV

Thank you for your interest in RemTV. Bug reports, ideas, documentation improvements, and pull requests are welcome.

## Before opening an issue

Please check whether the issue has already been reported. For bug reports, include:

- TV or streaming-device manufacturer and model;
- Android / Google TV version;
- RemTV version or commit;
- exact steps to reproduce the issue;
- expected and actual behavior;
- screenshots or relevant `logcat` output, with personal data removed.

Do not attach passwords, access tokens, signing keys, or other secrets.

## Pull requests

1. Keep each pull request focused on one change.
2. Explain the problem and the proposed solution.
3. Describe how the change was tested. If it was not tested on a physical TV, state that clearly.
4. Preserve remote-control navigation and accessibility.
5. Avoid unrelated formatting or generated-file changes.
6. Update documentation when behavior or setup instructions change.

## Building

See the build requirements and platform-specific commands in [README.md](README.md#сборка-из-исходников).

## Security-sensitive features

Changes involving ADB, permissions, package disabling, app installation, or system settings require particular care. Explain the security implications and provide safe defaults. Never add credentials or signing material to the repository.

## License

By contributing, you agree that your contributions are provided under the project's Apache License 2.0, unless explicitly stated otherwise.
