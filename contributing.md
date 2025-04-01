## Contributing

Before you start to code, please create traceability for a use case in [Tool used by the team to manage project](), open a [new issue]() to describe a bug found, or search for and continue the discussion in an [existing issue]().

Please completely fill out any templates to provide essential information about your new feature or the bug you discovered or reported.

When you are ready to code, you can find more information about opening a pull request in the [GitHub docs](https://help.github.com/articles/creating-a-pull-request/).

Whether this is your first contribution or you are already an experienced contributor, your team has your back – don't hesitate to ask for help!

### Issue vs. Pull Request

An issue will never substitute a former card in Favro, an issue is only to address bugs recognized and not solved within the app.

An issue is required to be linked in every pull request. We understand that no-one likes to create an issue for something that appears to be a simple pull request, but here is why this is beneficial for everyone:

- An issue get more visibility than a pull request as issues can be pinned and it is primarily the issue list that people browse through rather than the more technical pull request list. Visibility is a key aspect so others can weigh in on issues and contribute their opinion.
- The discussion in the issue is different from the discussion in the pull request. The issue discussion is focused on the issue and how to address it, whereas the discussion in the pull request is focused on a specific implemention. An issue may even have multiple pull requests because either the issue requires multiple implementations or multiple pull requests are opened to compare and test different approaches to later decide for one.
- High-level conceptual discussions about the issue should be still available, even if a pull request is closed because its appraoch was discarded. If these discussions are in the pull request instead, they can easily become fragmented over multiple pull requests and issues, which can make it very hard to make sense of all aspects of an issue.

## Environment Setup

### Recommended Tools

- [Tool used by the team to develop]().

### Setting up your local machine


```sh
$ git clone {{your url repository}}
$ cd my-repository-folder # go into the clone directory
```

Open Development tootl, navigate to clone directory **my-repository-folder** and select it.

### Good to Know

- Things that are good to know or commands needed in order to run the project.

## Breaking Changes

### Deprecation Policy

If you change or remove an existing feature that would lead to a breaking change, use the following deprecation pattern:

- Make the new feature or change optional, if necessary with a new Scheduling option parameter.
- Use a default value that falls back to existing behavior.
- Add the @deprecated tag for the comment of the function, for example:
  > DeprecationWarning: The System App option 'example' will be removed in a future release.

Deprecations become breaking changes after notifying developers through deprecation warnings for at least one entire previous major release. For example:

- `4.5.0` is the current version
- `4.6.0` adds a new optional feature and a deprecation warning for the existing feature
- `5.0.0` marks the beginning of logging the deprecation warning for one entire major release
- `6.0.0` makes the breaking change by removing the deprecation warning and making the new feature replace the existing feature

See the [Deprecation Plan](DEPRECATIONS.md) for an overview of deprecations and planned breaking changes.

## Naming Branches

### Create a new branch

The title of a branch needs to be written in a defined syntax. We loosely follow the [Git Naming Convention](https://tilburgsciencehub.com/building-blocks/collaborate-and-share-your-work/use-github/naming-git-branches/)

1. Use separators: When writing a branch name, using slash (/) separators to increase readability of the name
2. Start name with category word: It is recommended to begin the name of a branch with a category word, which indicates the type of task that is being solved with that branch. Some of the most used category words are:
   - `hotfix` - for quickly fixing critical issues, usually with a temporary solution
   - `bugfix` - for fixing a bug
   - `feature` - for adding, removing or modifying a feature
   - `test` - for experimenting something which is not an issue
   - `wip` - for a work in progress
3. Use the {Release version - ID} of the Favro Card or Issue addressing: Using the ID in the branch name makes it easy to identify the task and keep track of its progress. `X.Y.Z-alpha.ID`
4. Avoid Using Numbers Only: It’s not a good practice to name a branch by only using numbers, because it creates confusion and increases chances of making mistakes. Instead, combine ID of issues with key words for the respective task.
5. Avoid Long Branch Names: As much as the branch name needs to be informative, it also needs to be precise and short. Detailed and long names can affect readability and efficiency.

```
<category>/<X.Y.Z-alpha.ID>/<title>
```

## Pull Request

### Commit Message

The title of pull requests needs to be written in a defined syntax. We loosely follow the [Conventional Commits](https://www.conventionalcommits.org) specification, which defines this syntax:

```
<type>: <summary>
```

The _type_ is the category of change that is made, possible types are:

- `feat` - add a new feature or improve an existing feature
- `fix` - fix a bug
- `refactor` - refactor code without impact on features or performance
- `docs` - add or edit code comments, documentation, GitHub pages
- `style` - edit code style
- `build` - retry failing build and anything build process related
- `perf` - performance optimization
... (53 líneas restantes)