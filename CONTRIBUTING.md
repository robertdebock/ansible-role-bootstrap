# [Please contribute](#please-contribute)

You can really make a difference by:

- [Making an issue](https://help.github.com/articles/creating-an-issue/). A well described issue helps a lot. (Have a look at the [known issues](https://github.com/search?q=user%3Arobertdebock+is%3Aissue+state%3Aopen).)
- [Making a pull request](https://services.github.com/on-demand/github-cli/open-pull-request-github) when you see the error in code.

I'll try to help and take every contribution seriously.

It's a great opportunity for me to learn how you use the role and also an opportunity to get into the habit of contributing to open source software.

## [Step by step](#step-by-step)

Here is how you can help, a lot of steps are related to GitHub, not specifically my roles.

### [1. Make an issue.](#1-make-an-issue)

When you spot an issue, [create an issue](https://github.com/robertdebock/ansible-role-bootstrap/issues).

Making the issue help me and others to find similar problems in the future.

### [2. Fork the project.](#2-fork-the-project)

On the top right side of [the repository on GitHub](https://github.com/robertdebock/ansible-role-bootstrap), click `fork`. This copies everything to your GitHub namespace.

### [3. Make the changes](#3-make-the-changes)

In you own GitHub namespace, make the required changes.

I typically do that by cloning the repository (in your namespace) locally:

```shell
git clone git@github.com:YOURNAMESPACE/ansible-role-bootstrap.git
```

Now you can start to edit on your laptop.

### [4. Optionally: test your changes](#4-optionally-test-your-changes)

Install [molecule](https://molecule.readthedocs.io/en/stable/) and [Tox](https://tox.readthedocs.io/):

```shell
pip install molecule tox ansible-lint docker
```

And run `molecule test`. If you want to test a specific distribution, set `image` and optionally `tag`:

```shell
image=centos tag=7 molecule test
```

Once it start to work, you can test multiple version of Ansible:

```shell
image=centos tag=7 tox
```

### [5. Optionally: Regenerate all dynamic content](#5-optionally-regenerate-all-dynamic-content)

You can use [Ansible Generator](https://github.com/robertdebock/ansible-generator) to regenerate all dynamic content.

If you don't do it, I'll do it later for you.

### [6. Make a pull request](#6-make-a-pull-request)

[GitHub](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork) on pull requests.

In the comment-box, you can [refer to the issue number](https://help.github.com/en/github/writing-on-github/autolinked-references-and-urls) by using #123, where 123 is the issue number.

### [7. Wait](#7-wait)

Now I'll get a message that you've added some code. Thank you, really.

CI starts to test your changes. You can follow the progress on Travis.

Please consider [sponsoring me](https://github.com/sponsors/robertdebock).
