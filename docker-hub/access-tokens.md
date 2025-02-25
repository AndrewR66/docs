---
title: Create and manage access tokens
description: Learn how to create and manage your personal Docker Hub access tokens to securely push and pull images programmatically.
keywords: docker hub, hub, security, PAT, personal access token
---

If you are using the [Docker Hub CLI](https://github.com/docker/hub-tool#readme){: target="_blank" rel="noopener" class="_"}
tool (currently experimental) to access Hub images from the Docker CLI, you can create personal access tokens (PAT) as alternatives to your password.

Compared to passwords, personal access tokens provide the following advantages:

- You can investigate when the PAT was last used and then disable or delete it if you find any suspicious activity.
- When using an access token, you can't perform any admin activity on the account, including changing the password. It protects your account if your computer is compromised.
  
Access tokens are also valuable for building integrations, as you can issue multiple tokens, one for each integration, and revoke them at
any time.
   > **Note**
   >
   > If you have [two-factor authentication (2FA)](2fa/index.md) enabled on
   > your account, you must create at least one personal access token. Otherwise,
   > you won't be able to sign in to your account from the Docker CLI.

## Create an access token

> **Important**
>
> Treat access tokens like your password and keep them secret. Store your tokens securely in a credential manager for example.
{: .important}

1. Sign in to [Docker Hub](https://hub.docker.com){: target="_blank" rel="noopener" class="_"}.

2. Select your username in the top-right corner and from the drop-down menu select **Account Settings**.

3. Select the **Security** tab and then **New Access Token**.

4. Add a description for your token. Use something that indicates the use case or purpose of the token.
   
5. Set the access permissions. 
   The access permissions are scopes that set restrictions in your
   repositories. For example, for Read & Write permissions, an automation
   pipeline can build an image and then push it to a repository. However, it
   can not delete the repository.

6. Select **Generate** and then copy the token that appears on the screen and save it. You won't be able
   to retrieve the token once you close this prompt.

## Use an access token

You can use an access token anywhere that requires your Docker Hub
password.

When logging in from your Docker CLI client (`docker login --username <username>`),
omit the password in the login command. Instead, enter your token when asked for
a password.

> **Note**
>
> If you have [two-factor authentication (2FA)](2fa/index.md) enabled, you must
> use a personal access token when logging in from the Docker CLI. 2FA is an
> optional, but more secure method of authentication.

## Modify existing tokens

You can rename, activate, deactivate, or delete a token as needed.

1. Access your tokens under **Account Settings > Security**.
   This page shows an overview of all your tokens. You can also view the number
   of tokens that are activated and deactivated in the toolbar.

2. Choose a token and then select **Delete** or **Edit**, or use the menu on the far right of a token row to bring up the edit screen. 
   You can also select multiple tokens to delete at once.

3. After modifying the token, select **Save**.
