# Kale

Kale is a very small web page for editing one file in a GitHub repo.

You paste:

- a GitHub personal access token
- a GitHub file link, like `https://github.com/tweedefloor/kale/blob/main/README.md`

The app loads the file, lets you edit the text, and commits the change back to the same branch.

Everything runs in your browser. There is no backend server.

## Token

Use a **fine-grained personal access token**.

1. Go to [GitHub token settings](https://github.com/settings/personal-access-tokens/new)
2. Set an expiration.
3. Under **Repository access**, select **Only select repositories**, then pick the repo you want to edit (the same as in the Github file link above)
4. Under **Repository permissions**, set:
  - **Contents**: `Read and write`
  - **Metadata**: `Read-only` should already be included
5. Generate the token and paste it into the app.

Note: the token can edit files in the repos you grant it access to, so keep the URL containing `?pat=...` as secret.

## Use

Open `index.html` in a browser or host it as a static website.

Paste the token and GitHub file link, load the file, edit it, then click commit.

