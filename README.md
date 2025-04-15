# git-aicommit

git-aicommit is a Bash script that integrates Git with the OpenAI API to automatically generate commit messages based on your staged changes. The script retrieves the diff from staged changes, sends it to OpenAI to generate a concise and informative commit message, and then opens your configured editor preloaded with the generated commit message for review and confirmation.

## Requirements

- **Git:** Required to run Git commands such as `git diff --staged` and `git commit`.
- **Curl:** Used to make HTTP requests to the OpenAI API.
- **jq:** A command-line JSON processor (install via `sudo apt-get install jq` on Ubuntu, for example).
- **OpenAI API Key:** Set the environment variable `OPENAI_API_KEY` with your OpenAI API key.

## Installation

Follow these steps to install and set up the script:

1. **Clone the repository:**

    ```bash
    git clone <REPOSITORY_URL>
    ```

2. **Navigate to the project directory::**

    ```bash
    cd git-aicommit
    ```

3. **Make the script executable:**

    ```bash
    chmod +x git-aicommit
    ```

4. **Update the path variable in your .bashrc or .zshrc file**

    ```bash
    export PATH=$PATH:/PATH_TO_PROJECT/git-aicommit
    ```

## Usage

1. **Stage Your Changes:**

    Add your changes to the staging area:

    ```bash
    git add <files>
    ```

2. **Run aicommit**

    ```bash
    git aicommit
    ``` 

If everything is correctly configured (including the API key and required dependencies), your Git editor will open with the AI-generated commit message ready for review.


## Contributing

Contributions are welcome! If you have improvements or suggestions, feel free to open issues or submit pull requests.

