# Creating a Pull Request

> [!TIP]
> You should commit your changes to a new branch. Committing directly to `main` can result in issues for you later on.

When you have made your changes, tested them locally, and are happy with the results, you are ready to submit a pull request.

> [!ATTENTION]
> The scope of your pull request should be as narrow as possible. When a pull is merged, the squashed commit message is used in the change log. As such, the changes a PR makes should be limited to something that can be described in a single commit message. (This does NOT mean you can only make one commit, our team will handle the squash on merge.)

## Committing Your Code

You should follow the conventional commit standard when generating your commit message. The general format is:

```txt
<type>: <description>
```

For example, a commit that adds an emote command would look like:

```txt
feat: add emote command
```

A commit that fixes a bug in the level system would look like:

```txt
fix: patch bug in level logic
```

If you need additional description, you can add it to the body of the commit:

```txt
fix: patch bug in level logic

Adjusts the flow of the level logic so the database call
is made before the notification message is sent.
```

> [!NOTE]
> You should _not_ change the package version number - this is handled by our team during deployments.

## Submitting Your Pull Request

Our repository is configured to use a pull request template:

```md
# Pull Request

<!-- Before contributing, please read our contributing guidelines https://github.com/BeccaLyria/discord-bot/blob/main/CONTRIBUTING.md -->

## Description

<!-- A brief description of what your pull request does. -->

## Related Issue

<!-- Is this related to an issue? Does it close one? If so, replace the XXXXX below with the issue number. -->

Closes #XXXXX

## Documentation

For _any_ version updates, please verify if the [documentation page](https://docs.beccalyria.com?utm_source=docs&utm_medium=creating-pr) needs an update. If it does, please [create an issue there](https://github.com/BeccaLyria/discord-documentation/issues/new?assignees=nhcarrigan&labels=%F0%9F%9A%A6+status%3A+awaiting+triage&template=update.md&title=%5BUPDATE%5D) to ensure it is not forgotten.

- [ ] My contribution does NOT require a documentation update.
- [ ] My contribution DOES require a documentation update.
```

The comments are present to help you fill out the template, but will not show up in the actual text.

Below the `Description` header, you should provide a clear description of what your pull request changes. Be as detailed as possible, as this helps our maintainers understand the purpose of your changes.

Below the `Related Issue` header, if your pull request will close an issue, replace `XXXXX` with the issue number. A pull request that closes issue 1234 would say `Closes #1234`. If your pull request is related to an issue but will not necessarily close it, change it to `Related to #1234`.

Under the `Documentation` header, determine if your changes require an update to this documentation site. Replace the appropriate `[ ]` with `[x]`. If your changes _do_ require a documentation update, create an issue on the repository (the link is provided) to help our team keep track.

## Waiting for Review

We maintain quite a number of projects, and our staff are all kindly volunteering their time to keep Becca running smoothly. We ask that you exercise patience, as we will review your pull request as soon as time allows.

If your pull request requires changes, we will leave review comments with suggested changes. We ask that changes be made within 7 days of a review, to avoid stalling the project.

Once our team are happy with your changes, we will approve and merge your pull request - the only thing left to do then is celebrate your successful contribution!
