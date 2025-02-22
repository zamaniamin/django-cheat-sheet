✨ Automate conventional Git commits in PyCharm! This AI prompt generates
clean, [structured messages](commit-message-structure.md) (type, scope,
summary, details) in seconds. Say goodbye to messy commits!

Go to Pycharm and follow these steps:

1. Press `Ctrl`+`Alt`+`S` to open settings and then select **`Tools | AI Assistant | Prompt Library`**.
2. In the **`Built-In Actions`** section, select **`Commit Message Generation`**.
3. In the editor field on the right, specify the rules for commit message generation, copy this prompt:

```markdown title="Prompt"
Generate a Git commit message that follows our conventional commit message structure. The commit message should contain
the following sections:

1. **Type** (mandatory): Use one of the following types to specify the purpose of the commit:
    - feat (new feature)
    - fix (bug fix)
    - docs (documentation changes)
    - style (code formatting and style changes)
    - refactor (code restructuring without behavior change)
    - test (updates or additions to tests)
    - chore (maintenance tasks)

2. **Scope** (optional): If applicable, specify the project’s module or component in parentheses immediately after the
   type (e.g., feat(auth)).

3. **Description** (mandatory): A one-line summary of the change in imperative mood and under 72 characters.

4. **Body** (optional): If necessary, add one or more paragraphs with bullet points detailing the changes. Make sure
   there’s a blank line between the description and the body.

Here is the expected structure:

----------------------------------------------------------
<type>(<scope>): <Short description (max 72 chars)>

- <Detailed change point 1>
- <Detailed change point 2>
- <More details if necessary>

----------------------------------------------------------

For example, if you are adding a user authentication feature, you might receive a prompt similar to:

feat(auth): Add user authentication

- Implement user registration and login functionality.
- Create user model and update the database schema.
- Update documentation with authentication instructions.

Please generate the commit message based on the provided details.
```

Click **Apply**.  
Done. Say goodbye to messy commits!