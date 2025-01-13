Committing code changes in a version control system like Git is a crucial part of the development process. Following
best practices for Git commits can help make your project history more understandable and maintainable. Here are some
best practices for Git commits:

1. **Keep Commits Small and Focused**:
    - Each commit should represent a single, logical change. Avoid making multiple unrelated changes in a single commit.
    - Smaller commits make it easier to understand the history and to identify when and why specific changes were made.

2. **Write Descriptive Commit Messages**:
    - Provide a clear and concise summary of the change in the commit message's first line. The summary should be under
      72 characters.
    - If necessary, provide a more detailed explanation of the change in the subsequent lines, leaving a blank line
      after the summary.
    - Use the imperative mood in the summary (e.g., "Add feature" instead of "Added feature").
    - Include any relevant context, issue numbers, or references to external resources in the commit message.

3. **Follow a Consistent Style**:
    - Stick to a consistent naming convention and coding style for your commits. This makes it easier for team members
      to understand and review your changes.
    - Consider using prefixes in your commit messages to indicate the type of change (e.g., "feat:" for features, "fix:"
      for bug fixes, "docs:" for documentation updates).

4. **Commit Often**:
    - Make small, incremental commits as you work on a feature or fix a bug. Frequent commits help in tracking progress
      and identifying issues early.
    - Avoid committing large, unmanageable changes all at once.

5. **Review Before Committing**:
    - Review your changes before committing to catch any typos, debugging statements, or unintentional changes.
    - Run tests and ensure that your code builds successfully.

6. **Use Interactive Rebase**:
    - Before pushing your changes to a shared repository, consider using an interactive rebase to clean up your commit
      history.
    - Squash related commits together to create a more concise and meaningful history.

7. **Avoid Committing Generated or Temporary Files**:
    - Exclude generated files, build artifacts, and editor-specific files from version control by using `.gitignore`
      files.

8. **Reference Issues and Pull Requests**:
    - If your project uses an issue tracker or pull request system (e.g., GitHub issues), reference the corresponding
      issue or pull request in your commit message. This helps link code changes to specific tasks or discussions.

9. **Use Signed Commits When Appropriate**:
    - In some projects or organizations, signed commits may be required for security or compliance reasons. Learn how to
      create signed commits if necessary.

10. **Commit Messages are for Humans**:
    - Remember that commit messages are primarily for humans to understand the history of the project. Write messages
      that future you and your collaborators can easily understand.

Here's an example of a well-structured commit message:

```
feat: Add user authentication

- Implement user registration and login functionality
- Create user model and database schema
- Update documentation with authentication details

Closes #123
```

By following these best practices, you can maintain a clean and understandable Git commit history, which will make
collaboration and code maintenance more efficient.