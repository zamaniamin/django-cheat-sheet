## Message Structure

A well-structured Git commit message follows a consistent format that provides valuable information about the change
being made. A typical Git commit message consists of three parts:

1. **Type** (Mandatory):
    - The type specifies the purpose or nature of the commit. It describes what kind of change is being made. Common
      commit types include:
        - `feat`: A new feature or enhancement.
        - `fix`: A bug fix.
        - `docs`: Documentation updates.
        - `style`: Code style changes (e.g., formatting, indentation).
        - `refactor`: Code refactoring or restructuring that doesn't change behavior.
        - `test`: Adding or modifying tests.
        - `chore`: Maintenance or housekeeping tasks.

2. **Scope** (Optional):
    - The scope provides additional context about where the change is applied within the project. It is often the name
      of the module, file, or component affected by the change.
    - The scope is enclosed in parentheses and separated from the type by a colon. For example:
      `(auth): Add user authentication`.

3. **Description** (Mandatory):
    - The description is a concise and informative summary of the change. It should be clear and to the point.
    - The description is written in the imperative mood (e.g., "Add feature" instead of "Added feature").
    - It should be under 72 characters to ensure it is visible in most Git tools.
    - You can use multiple lines for a more detailed explanation if needed, but leave a blank line after the first line.

## feat

Here's an example of a well-structured Git commit message:

``` title="commit message"
feat(auth): Add user authentication

- Implement user registration and login functionality.
- Create user model and database schema.
- Update documentation with authentication details.

Closes #123
```

In this example:

- `feat` indicates that it's a new feature.
- `(auth)` provides context by specifying that the change is related to authentication.
- The description clearly states what the commit does.
- Bullet points are used for more detailed information.
- `Closes #123` references an associated issue or task, indicating that this commit resolves it.

## fix

Here's an example of a Git commit message for a "fix":

``` title="commit message"
fix(validation): Correct form validation error

- Fix a bug where the email validation regex was too restrictive.
- Update regex pattern to allow for valid email addresses.
- Ensure error messages are displayed correctly on the form.

Fixes #789
```

In this commit message:

- `fix` specifies that it's a bug fix.
- `(validation)` provides context about the area of the project where the fix is applied.
- The description clearly states what issue or bug is being fixed.
- Bullet points provide additional details on the changes made to address the bug.
- `Fixes #789` references the issue number associated with the bug, indicating that this commit resolves it.

## style

Here's an example of a Git commit message for a "style" change:

``` title="commit message"
style(formatting): Update code formatting

- Standardize code formatting using the PEP 8 style guide.
- Fix indentation inconsistencies and remove trailing whitespaces.
- Ensure code is more readable and follows consistent styling rules.
```

In this commit message:

- `style` specifies that it's a code style change.
- `(formatting)` provides context about the type of style change being made.
- The description clearly states that the commit is focused on code formatting improvements.
- Bullet points provide specific details about the formatting changes made to improve code consistency and readability.

"Style" commits are typically used for changes that don't affect the code's functionality but focus on improving code
aesthetics and maintainability.

## docs

Here's an example of a Git commit message for a "docs" change:

``` title="commit message"
docs(readme): Update project README

- Add installation instructions for Windows users.
- Include a troubleshooting section to address common issues.
- Improve clarity and grammar throughout the README.
```

In this commit message:

- `docs` specifies that it's a documentation update.
- `(readme)` provides context about the specific documentation being modified (in this case, the project README).
- The description clearly states that the commit is focused on updating the documentation.
- Bullet points provide specific details about the changes made to improve the README, such as adding instructions and
  improving readability.

"Docs" commits are used for documentation-related changes, such as updating README files, adding comments, or improving
inline code documentation to make it more informative and understandable.

## refactor

Here's an example of a Git commit message for a "refactor" change:

``` title="commit message"
refactor(api): Simplify user authentication logic

- Reorganize the authentication code to improve readability.
- Remove redundant functions and simplify the authentication process.
- Enhance code maintainability by breaking down complex logic into smaller functions.
```

In this commit message:

- `refactor` specifies that it's a code refactoring.
- `(api)` provides context about the specific area of the codebase where the refactoring is taking place (in this case,
  the API).
- The description clearly states that the commit is focused on code refactoring.
- Bullet points provide specific details about the changes made to simplify and improve the codebase.

"Refactor" commits are used when you make changes to the code to enhance its structure, readability, and maintainability
without changing its external behavior or adding new features.

## test

Here's an example of a Git commit message for a "test" change:

``` title="commit message"
test(unit): Add unit tests for the UserAuthService

- Create comprehensive unit tests to cover authentication scenarios.
- Ensure that user registration, login, and password reset functions are thoroughly tested.
- Achieve 100% test coverage for the UserAuthService module.
```

In this commit message:

- `test` specifies that it's a change related to testing.
- `(unit)` provides context about the type of tests being added or modified (in this case, unit tests).
- The description clearly states that the commit is focused on adding unit tests.
- Bullet points provide specific details about the tests added and their objectives.

"Test" commits are used for changes related to testing, such as adding new tests, improving test coverage, or fixing
existing tests to ensure the codebase remains reliable and well-tested.

Following a consistent commit message structure makes it easier for team members to understand the purpose of each
commit and navigate the project's history effectively. It also facilitates automated release notes generation and
integration with issue tracking systems.

## chore

Here's an example of a Git commit message for a "chore" change:

``` title="commit message"
chore(build): Update build scripts and dependencies

- Upgrade build tools to the latest versions for improved performance.
- Update third-party dependencies to address security vulnerabilities.
- Refactor build scripts to enhance build process efficiency.
```

another example:

``` title="commit message"
chore(ci): Update CI/CD configuration

- Upgrade the CI/CD pipeline to use the latest version of the build and test tools.
- Adjust environment variables to improve deployment automation.
- Optimize build process for faster integration testing.
```

In this commit message:

- `chore` specifies that it's a maintenance or housekeeping task.
- `(build)` provides context about the specific area of the project related to the build process.
- The description clearly states that the commit is focused on updating build scripts and dependencies.
- Bullet points provide specific details about the changes made, such as upgrading tools, updating dependencies, and
  refactoring scripts.

"Chore" commits are used for general tasks that are not related to adding new features, fixing bugs, or improving
documentation or tests. These can include tasks such as updating build configurations, refactoring code for performance,
or any other maintenance activities that don't fall into the specific categories of other commit types.

**Tip:**
Removing a TODO comment from your code typically falls under the category of a "chore" commit.

A "chore" commit is used for maintenance or housekeeping tasks. These tasks include actions that do not affect the
code's functionality but are necessary for the project's upkeep, organization, or overall improvement. Removing TODO
comments falls into this category because it involves cleaning up the codebase and ensuring that it doesn't contain
unnecessary or outdated comments, improving the code's readability and maintainability.