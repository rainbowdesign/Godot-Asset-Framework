# Contributing Guide (draft)

Thank you for considering contributing to this project!  
This document explains how to contribute, the standards we follow, and the review process for pull requests.

---

## 1. How to Contribute
- Fork the repository and create a feature branch.
- Make your changes in a clear, modular way.
- Write tests where applicable.
- Submit a pull request (PR) with a clear description of your changes.
- Follow the coding style and quality standards outlined below.

---

## 2. Coding Style
We follow the official [Godot GDScript Style Guide](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_styleguide.html).

Additional project-specific rules:
- Use `gdformat` and `gdlint` to ensure consistent formatting.
- Favor clarity over cleverness.
- Document public APIs and complex logic.
- Keep code consistent across modules.

---

## 3. Pull Request Review & Approval
- **Primary Maintainer**: The project maintainer (currently Rainbow) has final authority to approve and merge PRs.
- **Delegation**: Trusted contributors may be granted review rights (listed in `GOVERNANCE.md`).
- **Process**:
  1. Automated checks (linting, tests, AI review) must pass.
  2. At least one maintainer or delegated reviewer must approve.
  3. Large or controversial changes may require multiple reviewers or governance discussion.
- **No auto-merge**: PRs cannot be merged without review.

---

## 4. Testing & Coverage
- All core modules should include unit tests where practical.
- Tests should cover critical logic and edge cases.
- Code coverage will be tracked; while 100% is not required, meaningful coverage of critical systems is expected.
- Continuous Integration (CI) runs tests automatically on each PR.

---

## 5. Security Standards
This project treats security as a first-class concern.

- **No Malicious Code**: Contributions must not include hidden or harmful behavior.
- **No Networking by Default**: Modules must not use networking APIs (`HTTPClient`, `WebSocketClient`, etc.) unless explicitly approved.
- **No System Execution**: Calls to `OS.execute()` or similar are prohibited unless justified and approved.
- **Sandboxed CI**: All PRs run in isolated CI environments to prevent harmful effects.
- **Transparency**: Suspicious code will be flagged and discussed openly.

---

## 6. Automated Checks
To maintain quality and security, all PRs are subject to automated checks:

- **Linting & Formatting**: `gdformat` and `gdlint` enforce style consistency.
- **Unit Tests**: Run automatically in CI.
- **Coverage Reports**: Ensure critical systems are tested.
- **AI-Assisted Review**:
  - PRs are scanned by AI tools for security, performance, and bug risks.
  - Disallowed APIs (networking, system execution) are flagged automatically.
  - AI review results appear in the PR discussion.
- **Branch Protection**: PRs cannot be merged unless all required checks pass.
