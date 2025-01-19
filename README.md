# GitHub Copilot Commit Message Instructions

This repository provides guidelines for writing commit messages using GitHub Copilot in VSCode.

## Setup Instructions

1. **Install GitHub Copilot Extension:**

   - Open VSCode.
   - Go to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window.
   - Search for "GitHub Copilot" and click "Install".

2. **Enable GitHub Copilot:**

   - After installation, you may need to sign in to GitHub to activate the extension.
   - Follow the prompts to authenticate with your GitHub account.

3. **Configure Commit Message Generation:**

   - Open your VSCode settings (`Ctrl+,` or `Cmd+,` on macOS).
   - Search for "Copilot" and ensure that the extension is enabled.
   - Optionally, you can customize the behavior of GitHub Copilot in the settings.
   - Add the following setting to your `settings.json` file to specify the commit message instructions file:
     ```json
     "github.copilot.chat.commitMessageGeneration.instructions": [
       {
         "file": ".copilot-commit-message-instructions.md"
       }
     ]
     ```

4. **Copy and Edit Instructions File:**

   - You can simply copy and paste the `.copilot-commit-message-instructions.md` file from this project into your working directory after completing the basic setup in VSCode.
   - Feel free to edit the instructions file locally to suit your project's needs.
   - Ensure that the instructions file is present in your working directory for GitHub Copilot to use it.

5. **Using GitHub Copilot for Commit Messages:**

   - When you are ready to commit changes, open the Source Control view (`Ctrl+Shift+G` or `Cmd+Shift+G` on macOS).
   - Stage your changes.
   - In the commit message input box, start typing your commit message.
   - GitHub Copilot will provide suggestions based on the commit message instructions provided in this repository.
   - Alternatively, you may see sparkles ✨ in the commit message input box. Click on them to generate a commit message using GitHub Copilot's suggestions. Once satisfied with the generated message, click "Commit".

## Commit Message Format

- Use conventional commit message format.
- The commit message should have a short description (50 characters or less) followed by a blank line and then a longer description.
- The short description should be in the format: `<type>(<scope>):<icon> <short description>`

Refer to the [Commit Message Instructions](./.copilot-commit-message-instructions.md) for detailed guidelines and examples.

## Example

### Commit Message Example

```
feat(auth): ✨ Add user authentication

Added user authentication using JWT. This includes login, registration, and token verification endpoints.

- Implemented JWT-based authentication.
- Added login and registration endpoints.
- Added middleware for token verification.

Fixes #123
```

### Breaking Change Example

```
refactor(api): ♻️ Update API endpoints

Refactored the API endpoints to follow RESTful conventions. This change affects all existing API calls.

- Updated endpoint URLs to follow RESTful conventions.
- Modified request and response formats.

BREAKING CHANGE: All existing API calls need to be updated to the new endpoint URLs.
```
