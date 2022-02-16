# Connecting To Github With a PAT

A **P**ersonal **A**ccess **T**oken (PAT) is an alternative to SSH for authentication to Github. By default Github removes PATs after one year of inactivity.

## Verify Email Address

Before we can use a Personal Access Token we need to ensure that our email address is verified on Github. This is done by clicking on settings in Github.

![Github Settings](../assets/github-setup__github-settings.png)

Then we can go to the access section and click on **Emails**.

![Github Email Settings](../assets/github-setup__github-email-settings.png)

If our email is unverified we can click on *Resend verification email*. Then check our email to verify our email address with Github.

![Verify Email Address](../assets/github-setup__email-verify-button.png)

<!-- Image Source:   https://docs.github.com/en/get-started/signing-up-for-github/verifying-your-email-address -->

## Creating A PAT

After verifying our email address we can create a Personal Access Token by first going to Settings --> Developer Settings --> Personal Access Tokens.

![Github Settings](../assets/github-setup__github-settings.png)

![Developer Settings](../assets/github-setup__developer-settings.png)

![Personal Access Token](../assets/github-setup__personal-access-token.png)

Then we can click on *Generate new token*.

![Generate New Token](../assets/github-setup__generate-new-token.png)

Then we can give the token a note, set an expiration date and give it **repo** scope.

We can optionally grant it Gist scope as well if we want to create gists from the command line.

![Create PAT](../assets/github-setup__pat-token-settings.png)

![Generate Token](../assets/github-setup__generate-token.png)

Then we can copy the token.  **We must copy the token before leaving this page, as Github will not show the token again.**

**We should NOT close this browser tab until we finish the lesson**.

![PAT Displayed](../assets/github-setup__copy-pat-token.png)

## Using the Token in Git

We can then use the token in git by cloning a repository using HTTPS.

We can first go to the [Python Fizbuzz Repository](https://github.com/AdaGold/python-fizzbuzz).

Then click on the **Code** button and select **https** and copy the link.

![Clone Repository](../assets/github-setup__clone-repo.png)

Then we can clone the repository using the token.  We should **not** use a password, but rather the copied personal access token.  We can use `cmd-v` to paste the token into the terminal.

```
$ git clone https://github.com/AdaGold/python-fizzbuzz.git
Username: your_username
Password: your_token
```

When the repository is downloaded we know that we have successfully authenticated with Github and will no longer need to re-authenticate until the PAT expires.

## Resources

- [Github Personal Access Token Documenation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)