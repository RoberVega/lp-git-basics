# Best Practises: Keeping a linear git history 🌳

Linear Git history is a clean and manageable way to understand the lifecycle of a project by ensuring that commits have a consistent and clear flow, making it easier for team members to follow the progression of the project. This can be especially crucial for debugging and for understanding the evolution of project code. [In here](https://www.bitsnbites.eu/a-tidy-linear-git-history/), you will find a detailed blog on why this is so important and how to achieve it.

Let us also explore some of the key points here:

## Benefits of Keeping a Linear History 🧼

- **Easier Troubleshooting**: Simplifies the process of finding and resolving bugs or errors in the codebase.
- **Clearer Understanding**: Offers a straightforward history, helping team members and new joiners comprehend the project evolution easily.
- **Smooth Merges**: Reduces complex merge conflicts, ensuring a smoother, more efficient workflow.

## Strategies for Maintaining a Linear History 🧽

We will explain some strategies for maintaining a linear history. These concepts are better understood when visualizing, so don't dispair if you feel a bit lost, we will provide you with a video that explains the concepts. In here, we just want to summarize them for future reference, while leaving the explannation to the video.

### Avoid Merge Commits:

Use rebase to integrate changes from one branch into another, rather than creating a merge commit.

- `git rebase <branch-name>`

### Interactive Rebase:

Use interactive rebase to tidy up your commits and modify history, making the project's evolution more transparent.

- `git rebase -i <commit-hash>`

### Squash Commits:

Combine several commit messages into one, providing a clean, understandable history.

- `git rebase -i HEAD~<number-of-commits>`


### Force Push Carefully:

After rebasing, you may need to force push your changes to update the remote branch.

- `git push origin <branch-name> --force`

> 🚨 Note: Use force push cautiously to avoid overwriting changes unintentionally.

> 🚨 Important Note 🚨: In general, for large projects, you want to avoid rebasing too much, a kilometrical history for the main branch might become a nightmare. A better strategy is to keep each solution at a branch and then squash before merging into the main branch. See more [here](https://www.git-tower.com/learn/git/faq/git-squash).


<img src="../images/RwvTrSm7zEYhd.jpg" alt="" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=RwvTrSm7zEY)






## Using VSCode to Rebase & Squash:

As always, we provide how to perform all these Git methods via VSCode.

<img src="../images/3o_01F04bZ4hd.jpg" alt="" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=3o_01F04bZ4)