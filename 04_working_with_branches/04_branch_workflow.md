# Branch Workflow 🔁

In general, for most projects, the following structure is a well-established workflow that ensures consistency when dealing with large projects. 

- **Main Branch**: The main project where everything is stable and finalized. This is the branch that one puts into production.
- **Hotfix Branches**: For urgent fixes.
- **Staging Branch**: A place where all new features, bugfixes and changes are storaged together before official realise to main. The purpose of this branch is to make sure everything works together and test the code in deployment before putting it into production. This branch can be further divided into **develop** and **realease** branches if the project were to be big enough.
- **Feature Branches**: For adding new features.
- **Bugfix Branches**: For fixing issues.

</br>

<img src="../images/git_workflow.svg" alt="WindowsVenv" width="800" height="auto">