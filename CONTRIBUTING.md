# Contributing to Angular Headless Hashnode

First off, thanks for taking the time to contribute! ❤️

All types of contributions are encouraged and valued. Please make sure to read the relevant section before making your contribution. It will make it a lot easier for us maintainers and smooth out the experience for all involved. The community looks forward to your contributions. 🎉

 - [Code of Conduct](#code-of-conduct)
 - [Question or Problem?](#question-or-problem)
 - [Issues and Bugs](#found-a-bug)
 - [Feature Requests](#missing-a-feature)
 - [Submission Guidelines](#submission-guidelines)
 - [Coding Rules](#coding-rules)
 - [Commit Message Guidelines](#commit-message-guidelines)

And if you like the project, but just don't have time to contribute, that's fine. There are other easy ways to support the project and show your appreciation, which we would also be very happy about:
 - Star the project
 - Tweet about it
 - Refer this project in your project's readme
 - Mention the project at local meetups and tell your friends/colleagues

## Code of Conduct

This project and everyone participating in it is governed by the
[Code of Conduct](/CODE_OF_CONDUCT.md).
By participating, you are expected to uphold this code. Please report unacceptable behavior
to [monacodelisa](https://github.com/monacodelisa).


## Question or Problem?

Do not open issues for general support questions as we want to keep GitHub issues for bug reports and feature requests.
Instead, we recommend using Discussions to ask support-related questions. 

## Found a Bug?

If you find a bug in the source code, you can help by [submitting an issue](#submitting-an-issue) to  [Angular-Headless-Hashnode](https://github.com/monacodelisa/Angular-Headless-Hashnode/issues).
Even better, you can [submit a Pull Request](#submitting-a-pull-request-pr) with a fix.


## Missing a Feature?
You can *request* a new feature by [submitting an issue](#submitting-an-issue) to our GitHub Repository.
If you would like to *implement* a new feature, please consider the size of the change in order to determine the right steps to proceed:

* For a **Major Feature**, first open an issue and outline your proposal so that it can be discussed.
  This process allows us to better coordinate our efforts, prevent duplication of work, and help you to craft the change so that it is successfully accepted into the project.

  **Note**: Adding a new topic to the documentation, or significantly re-writing a topic, counts as a major feature.

* **Small Features** can be crafted and directly [submitted as a Pull Request](#submitting-a-pull-request-pr).


## Submission Guidelines


### Submitting an Issue

Before opening an issue, please check the tracker to see if a similar issue has been raised. Existing discussions may provide useful insights or workarounds.

To expedite bug fixes, a minimal reproduction of the issue is required. This concise example helps in swiftly identifying and addressing the problem.

Providing a minimal reproduction is crucial for saving time, increasing the chances of a quick resolution, and ensuring that focus is given to the correct issue.

You can file new issues by selecting from our [new issue templates](https://github.com/monacodelisa/angular-headless-hashnode/issues/new/choose) and filling out the issue template.


### Submitting a Pull Request (PR)

Before you submit your Pull Request (PR) consider the following guidelines:

1. Search [GitHub](https://github.com/monacodelisa/angular-headless-hashnode/pulls) for an open or closed PR that relates to your submission.
   You don't want to duplicate existing efforts.

2. Be sure that an issue describes the problem you're fixing, or documents the design for the feature you'd like to add.
   Discussing the design upfront helps to ensure that we're ready to accept your work.

3. [Fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) the `monacodelisa/angular-headles-hashnopde` repo.

4. In your forked repository, make your changes in a new git branch:

     ```shell
     git checkout -b my-fix-branch develop
     ```
### The default branch is develop!

5. Create your patch, **including appropriate test cases**.

6. Follow the [Coding Rules](#coding-rules) and [Commit Message Guidelines](#commit-message-guidelines).

7. Run the full test suite, as described in the developer documentation, and ensure that all tests pass.

8. Commit your changes using a descriptive commit message.

     ```shell
     git commit --all
     ```
    Note: the optional commit `--all` command line option will automatically "add" and "rm" edited files.

9. Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```

10. In GitHub, send a pull request to `angular-headless-hashnode:develop`.

### Reviewing a Pull Request

I reserve the right not to accept pull requests from community members who haven't been good citizens of the community.


#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the develop branch:

    ```shell
    git checkout develop -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your local `develop` with the latest upstream version:

    ```shell
    git pull --ff upstream develop
    ```


## Coding Rules
To ensure consistency throughout the source code and the different app versions, keep these rules in mind as you are working:

### FILE STRUCTURE
#### Components
Store full components that can be used on their own, in the `components` folder, examples include:
- `header`, `footer`, `posts`, `series`, `post-details`, `layout`, `sidenav`

#### Partial Components
Place partial components like dialogs and other smaller reusable components, in the `partials` folder, examples:
- `follow-dialog`, `search-dialog`

### Interfaces
Keep interfaces in the `models` folder, examples:
- `blog-info.ts`, `post.ts`
- Avoid duplicating existing interfaces.

#### Services
- Place services in the `services` folder, examples:
  - `blog.service.ts`, `theme.service.ts`

#### Pipes in the `pipes` folder 
#### Directives in the `directives` folder etc.

#### Page Folder Exclusion
- Omitting a pages folder due to the current absence of an extensive component count, that would justify its introduction.

For clarification on component categorization or any other building block, cross-reference with implementations in other app versions or seek guidance through communication.


### NAMING CONVENTIONS
- For dialogs, ensure the inclusion of the term dialog in the name.
- Maintain consistency with established naming conventions in other app versions.
- Propose suggestions for improved and clearer naming in discussions or comments.

### STYLE GUIDE 
#### The project utilizes SCSS. Copying and pasting CSS from other sources would be accepted only if it is formatted correctly to comply with SCSS conventions.
#### use relative measurements in the `scss` files:
- `rem`, `%`
- `wh`, `vh`, `dvw` `dvh`
- avoid using `px`

# INDENTATION & FORMATTING
Maintain the project's indentation and formatting. Do not include formatting changes in your PRs, only include code that you have changed. It doesn't look like you have done more when you submit a PR with tons of indentation changes - we all see its just indentation and that makes it even more unpleasant to deal with.  

## Commit Message Guidelines

To maintain a clear and organized version history, we follow a standardized commit message convention. This ensures that each commit provides valuable information about the changes made. Please adhere to the following guidelines when crafting your commit messages:

### Feature:

```
feat(component): add new feature X
```

### Bug Fix:

```
fix(component): resolve issue with Y
```

### Documentation Update:

```
docs(readme): update installation instructions
```

### Code Refactor:

```
refactor(service): restructure data fetching logic
```

### Performance Improvements:

```
perf(api): optimize data retrieval for faster response
```

### Test:

```
test(component): add unit tests for feature Z
```

### Build:

```
build(pipeline): update dependencies and build scripts
```

### Chore (Release):

```
chore: prepare for version 1.0.0 release
```

### Revert 

```
revert: revert changes from commit abc123
```

## Mandatory Compliance with [Coding Rules](#coding-rules) and [Commit Message Guidelines](#commit-message-guidelines) for PR Merges

Kindly ensure that all pull requests strictly adhere to our Coding Rules and Commit Message Guidelines. Non-compliant PRs must be adjusted prior to acceptance.

## Reviewer Accountability
Reviewers who approve PRs not in alignment with the [Coding Rules](#coding-rules) and [Commit Message Guidelines](#commit-message-guidelines) may face restrictions on their approval privileges. 