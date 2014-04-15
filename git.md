# Git

## Branch Names

- A branch name should be **30 characters or less**.
- Use lowercase only.
- Use prefixes: `add`, `remove`, `update`, `refactor`, `fix`.
- Use slashes to separate parts, e.g. `add/my-feature`, `fix/crazy-bug`.
- Use hypens to separate words.

**Caveat**: Branches are implemented as paths, so you cannot have a branch
named `add/my-feature` and another branch named `add`.

## Commit Messages

- The first line should be **50 characters or less**.
- Use the first line as a clear summary of the change.
- Subsequent lines (if any) can be fairly verbose and detailed.
- Use imperative language.
- Use prefixes: `Add`, `Remove`, `Update`, `Refactor`, `Fix`.
- Capitalize the first letter. Use spaces between words. Place dot at the end.

## Bonus for GitHub Users

- Commit with a string like `Close #123` to close issue #123, along with
referencing the commit in the issue.

- Place `#123` in the commit message for just referencing issue #123.