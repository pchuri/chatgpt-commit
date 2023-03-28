# `chatgpt-commit`
I was inspired by Markuswt's gpt-commit and made some modifications to enable it to be used through web access instead of just the chatgpt API.

Generate commit messages using ChatGPT. To use `chatgpt-commit`, simply invoke it whenever you'd use `git commit`. Git will prompt you to edit the generated commit message.

```
git add .
./chatgpt-commit.py
```

## Getting Started

Install `ygka` and clone `chatgpt-commit`.

```
pip3 install ygka
ygka 'hello'
git clone git@github.com:pchuri/chatgpt-commit.git
```

### Modify `git commit` (optional)
If you want `git commit` to automatically invoke `chatgpt-commit`, copy `chatgpt-commit.py` and `prepare-commit-msg` to the `.git/hooks` directory in any project where you want to modify `git commit`.

```
sudo -s cp chatgpt-commit.py /usr/local/bin
cp prepare-commit-msg [your-repo]/.git/hooks
```

## Privacy Disclaimer
`chatgpt-commit` uses the [OpenAI API](https://platform.openai.com/docs) to generate commit messages. Both file names and contents from files that contain staged changes will be shared with OpenAI when using `gpt-commit`. OpenAI will process this data according to their [terms of use](https://openai.com/policies/terms-of-use) and [API data usage policies](https://openai.com/policies/api-data-usage-policies). On March 1st 2023 OpenAI pledged that by default, they would not use data submitted by customers via their API to train or improve their models, and that this data will be retained for a maximum of 30 days, after which it will be deleted. 
