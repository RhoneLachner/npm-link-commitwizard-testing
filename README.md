# npm-link-commitwizard-testing

Environment to test the **CommitWizard-CLI** package locally using `npm link`.

## Purpose

To ensure that the **CommitWizard-CLI** works as expected by testing its ability to:
- Prompt for commit categories.
- Prompt for commit messages.
- Create commits using Git.

## Steps to Test CommitWizard-CLI

1. **Link CommitWizard-CLI Locally**  
   Navigate to the `CommitWizard-CLI` directory on your computer and link it globally:  
   `cd /path/to/CommitWizard-CLI`  
   `npm link`

2. **Link CommitWizard-CLI to the Testing Repository**  
   In this testing repository, link the globally linked `CommitWizard-CLI` package:  
   `npm link commitwizard-cli`

3. **Initialize Git (If Not Already Done)**  
   Ensure the repository is a valid Git repository:  
   `git init`

4. **Create a Test File**  
   Add and commit a sample file for testing:  
   `echo "Test file" > test.txt`  
   `git add test.txt`  
   `git commit -m "Initial commit"`

5. **Run CommitWizard-CLI**  
   Use the `commitwizard` command to test the CLI:  
   `commitwizard`

## Expected Behavior

- The CLI should prompt you to select a commit category.
- After selecting a category, it should prompt you to enter a commit message.
- A new Git commit should be created using the selected category and message.

## Unlink CommitWizard-CLI (Optional)

1. In this repository:  
   `npm unlink commitwizard-cli`

2. Globally unlink `CommitWizard-CLI`:  
   `npm unlink -g commitwizard-cli`
