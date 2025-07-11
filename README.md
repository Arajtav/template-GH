A repository containing a better set of labels for github issues.
The labels are split into several categories, each prefixed with a different uppercase letter.
For the rest of the Readme, Issues will be called `tasks`.

## Categories

### `P` - Priority

Labels used to indicate how important a task is.

- `P-LOW` (#ffe600) - Low priority, tasks with lower than average importance.
- `P-MEDIUM` (#ffa200) - Medium priority, the default.
- `P-HIGH` (#ff4d00) - High priority, should be done ASAP.

### `C` - Category

- `C-Bug` (#bd0948) - Tasks related to bugs and vulnerabilities.
- `C-CI/CD` (#57453a) - CI and/or CD tasks.
- `C-Docs` (#30c5f6) - Tasks related to the documentation (or project organization).
- `C-Feature` (#0df254) - Tasks related to new features.
- `C-Performance` (#20dbf6) - Tasks related to performance (generally should not be used with `C-Bug`).
- `C-Tests` (#1cd786) - Tasks related to for example unit tests.

### `A` - Additional

- `A-Breaking` (#6b75a9) - Indicates the change required by the task, may be incompatible.
  Can mean incompatibility with the current codebase, indicating the need for refactoring.

## Usage

To remove all the existing labels from the current repo using Github CLI, execute the command below.
Do **not** run the command, if the repo already uses some labels, in that case it will be easier to
just change the colors and rename the labels manually.

`gh label list --limit 1000 --json name -q '.[].name' | xargs -I{} gh label delete "{}" --yes`

Then, to clone the labels from this template, to your repository run the following command.

`gh label clone Arajtav/template-gh`
