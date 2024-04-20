## `git tag` : marking milestones 🏷️

The `git tag` command is your way to mark significant points in your project's history, like releases or major updates. This tool not only helps you create lightweight and annotated tags but also manages them efficiently.

But why tags though? Well, not only they provide very useful information to developers, as we will see when we talk about Semantic Versioning, but they also allow you to reference particular milestones in your project. These references mean you can easily compare to tags by using `git diff`, but you can also write messages associated to them that give you even another layer of overview in your project, less populated than a git tree.


In Git, lightweight tags are simple pointers to specific commits. They're akin to a bookmark, marking a specific point in the repository's history without containing any additional information or metadata. On the other hand, annotated tags are stored as full objects in the Git database. They include the tagger’s name, email, the date of the tagging, and have a tagging message, providing context about the tag's purpose. Annotated tags can also be signed and verified with GNU Privacy Guard (GPG), making them particularly useful for release management by adding a layer of security and authenticity to the tag.


- `git tag` : list all tags in the repository.
- `git tag <tag_name>` : create a new lightweight tag named `<tag_name>`.
- `git tag -a <tag_name> -m "<message>"` : create an annotated tag, using `<message>` to describe this tag.
- `git tag -d <tag_name>` : delete the tag named `<tag_name>`.
- `git tag -l "<pattern>"` : list tags that match the given pattern.
- `git tag -v <tag_name>` : verify the tag. This is useful for signed tags to check the signature.
- `git tag -f <tag_name>` : move an existing tag `<tag_name>` to the current commit. Use with caution as it affects others' clones.
- `git show <tag_name>` : show the commit and metadata that a tag points to.

## `git push` : sharing your marks 🚀

The `git push` command enables you to share tags with others, making sure your marked milestones are available to all collaborators and maintain the project's historical milestones intact.

- `git push origin <tag_name>` : push the specified tag to the remote repository.
- `git push origin --tags` : push all local tags to the remote repository.
- `git push --delete origin <tag_name>` : delete a tag from the remote repository.
- `git push origin :refs/tags/<tag_name>` : another way to delete a tag from the remote repository.

With these commands, you can effectively manage and communicate the evolution of your project through tags, enhancing collaboration and clarity within your team and we normally do it by doing semantic versioning.

## Semantic Versioning: Organizing Versions Systematically 📐

Semantic Versioning, often abbreviated as SemVer, is a versioning scheme that helps manage the release of new versions of software in a structured and predictable manner. This method uses a three-part version number format: major, minor, and patch (e.g., 1.4.2). Each number serves a specific purpose in communicating the nature of the changes made:

- **Major version** (`X.y.z`): Incremented for incompatible API changes or major alterations that require users to modify their existing code.
- **Minor version** (`x.Y.z`): Incremented for backward-compatible additions and enhancements. These updates add functionality but do not break existing features or code.
- **Patch version** (`x.y.Z`): Incremented for backward-compatible bug fixes that address incorrect behavior.

Semantic Versioning also supports pre-release versions and build metadata, which can be appended to the version number, such as `1.4.2-beta` or `2.0.0+build.1848`. These additions provide further context for developers and users, indicating developmental stages or build information.

By adhering to the SemVer principles, teams can release updates confidently, knowing that the version number itself communicates the scope and scale of changes. This clarity is crucial for maintaining dependency stability across software that relies on libraries, APIs, or frameworks adhering to Semantic Versioning.

To ensure compliance and to avoid disruption, it's recommended that projects document their versioning strategy explicitly and follow it consistently. This practice helps in managing dependencies effectively and in reducing conflicts in software environments.

## Integration with VSCode

VSCode allows you to navigate your tags in a very easy way. Just go to the source control and check the tags option. It allows you to create and delete tags in a very easy way. On the other hand, Git Graph and Gitlens also allow you to create tags at any commit by simply right clicking on the commit and adding a tag there. 

<img src="../images/spkUevg1NqMhd.jpg" alt="WindowsVenv" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=spkUevg1NqM)




