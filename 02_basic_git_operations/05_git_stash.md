## `git stash`: Saving Changes Temporarily 🛅

The `git stash` command offers a convenient way to temporarily shelve modified, tracked files in your working directory, so you can switch contexts without committing unfinished work. This is particularly useful in a busy development environment where you might need to switch branches without committing half-done work.

But why stash? Stashing is handy because it helps keep your working directory clean and your commit history neat. You can stash changes when you need to quickly switch from one task to another, then apply them later, either to the same or a different branch.

### Stash Basics:

- **Create a Stash**: Temporarily store all modified tracked files and staged changes.
  - `git stash push`: Pushes a new stash onto your stack. You can include untracked files with the `-u` or `--include-untracked` option.
  - `git stash save "<message>"`: Similar to `push`, but allows you to provide a descriptive message for the stash.

### Managing Stashes:

- **List Stashes**: View all stashes you've stored.
  - `git stash list`: Lists all stashes, which can be referenced by identifiers like `stash@{0}`, `stash@{1}`, etc.
- **Apply a Stash**: Reapply the stashed changes onto the current working directory.
  - `git stash apply`: Applies the latest stashed changes by default. You can specify a stash with `git stash apply stash@{n}`.
- **Pop a Stash**: Apply the stashed changes and then immediately drop the stash from your stack.
  - `git stash pop`: This command is useful for applying changes and cleaning up the stash list.

### More Advanced Uses:

- **Stashing Specific Files**: You can choose to stash only specific files.
  - `git stash push <file_path>`: Stashes changes of only the specified files.
- **Create Branch from Stash**: If a stash applies to a different branch, you can create a new branch and apply the stash there.
  - `git stash branch <new_branch_name>`: Creates a new branch from the commit where the stash was originally created, applies the stash, and drops it if successful.

### Cleaning Up:

- **Delete a Stash**: Remove a specific stash.
  - `git stash drop stash@{n}`: Drops the specified stash.
- **Clear All Stashes**: Remove all stored stashes.
  - `git stash clear`: This command is useful when you want to clean up all saved stashes.

Using `git stash`, you can effectively manage your work-in-progress changes, maintaining a clean working directory and a well-organized commit history. This flexibility supports an efficient workflow, especially when juggling multiple tasks or emergencies that require immediate attention without losing previous work.  

## Handling Conflicts and Best Practices with `git stash` 💡

### How to Handle Conflicts

When applying stashed changes to a different commit or branch, conflicts may arise due to overlapping changes or contextual differences. Here's how you can effectively manage these conflicts:

- **Manual Resolution**: Open the conflicted files and look for the conflict markers (`<<<<<<<`, `=======`, and `>>>>>>>`). Manually merge the changes in these sections to resolve the conflict.
- **Mark as Resolved**: After resolving the conflicts in each file, use `git add <resolved-file>` to stage the resolved files, signaling to Git that the conflicts have been addressed.
- **Complete the Stash Application**: If you used `git stash pop` and encountered conflicts, after resolving them, you need to complete the operation manually. If you were simply applying a stash, you can continue working or commit the changes as needed.

In a future section we will learn how to [solve these conflitcts](../04_working_with_branches/02_merge_conflicts.md).

### Best Practices for Using `git stash`

To minimize the potential for conflicts and to maximize the effectiveness of using `git stash`, consider the following best practices:

- **Keep Stashes Small and Contextual**: Try to stash small, logically related changes. This makes it easier to manage and reduces the likelihood of conflicts when the stash is applied later.
- **Regularly Update Branches**: Keep your branches updated with the latest changes from the main branch or any other relevant branches. This reduces the divergence between your stash context and the branch where you want to apply the stash.
- **Apply Stashes Promptly**: Apply stashed changes as soon as possible to avoid significant divergence in the codebase, which can lead to more complex conflicts.

By managing stashes carefully and following these best practices, you can enhance your workflow in Git, maintaining clean, conflict-free development environments across multiple branches.