## Branch Names

- A branch name should be **30 characters or less**.
- Use lowercase only.
- Use hyphens to separate words.

When there are ten branches or more:

- Use prefixes : `add`, `remove`, `update`, `refactor`, `fix`.
- Use slashes to separate parts, e.g. `add/my-feature`, `fix/crazy-bug`.

**Caveat**: Branches are implemented as paths, so you cannot have a branch
named `add/my-feature` and another branch named `add`.

## Commit Messages

- The first line should be **50 characters or less**.
- Use the first line as a clear summary of the change.
- Subsequent lines (if any) can be fairly verbose and detailed.
- Use imperative language, e.g. `Update README.md`
- Use prefixes: `Add`, `Remove`, `Update`, `Refactor`, `Fix`.
- Capitalize the first letter. Separate words with spaces.
- Avoid dot at the end of the first line.

## Bonus for GitHub Users

- Commit with a string like `Close #123` to close issue #123, along with
referencing the commit in the issue.
- Place `#123` in the commit message for just referencing issue #123.
- Follow the guide for [Titles](english/titles.md) for Issues/Pull Requests.