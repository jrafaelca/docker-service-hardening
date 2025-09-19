Follow these guidelines when generating Git commit messages:

- Use English for all commit message content.
- Follow the Conventional Commits format:
  <type>(<optional-scope>): <short summary>

- Allowed types:
    * feat: new feature
    * fix: bug fix
    * refactor: internal changes without altering functionality
    * chore: minor tasks (infrastructure, dependencies, etc.)
    * docs: documentation
    * test: tests
    * perf: performance improvements
    * build: build system changes

- Summary line (commit title):
    * Maximum 72 characters.
    * Use lowercase, except for proper names or acronyms.
    * Do not end with a period.
    * Use imperative mood: add, fix, refactor.

- After the title, leave a blank line.

- Then, if necessary, add a body:
    * Clearly explain what was done and why.
    * Use one or more paragraphs.
    * Be clear, professional, and direct.
    * Wrap lines at a maximum of 72 characters.

- If the commit includes important or breaking changes, indicate it with:
  BREAKING CHANGE: description of the change

- Scope (optional):
    * Represents the affected part of the system (e.g., auth, api, branches, ui).

- Branch names (optional but recommended):
    * Use the format: <type>/short-description-in-kebab-case
    * Example: feat/validate-email-on-signup

- Generated commit messages should be clear and useful for automatic changelog generation.

- At the end of the message, suggest a branch name in English using the format:
  <type>/short-description-in-kebab-case
  so the user can create it if it does not exist yet.
