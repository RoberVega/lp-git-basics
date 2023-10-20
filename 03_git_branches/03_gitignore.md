# Best practices: the `.gitignore` file 📝

Now that we understand a bit more about branching and committing, we need to talk about the `.gitignore` file. It contains a list of files and folders that the version control tracker, Git, should ignore. But why should you ignore any file? There are a couple of reasons:
#### 1. Sensitive Data 🕵️:
You might have files containing sensitive data such as configuration files with passwords or API keys. It's fundamental to exclude these files to prevent the accidental exposure of confidential information.
#### 2. Build Files 🏗️: 
Compiled code, libraries, and other build artifacts don't need to be in version control. They can be bulky and clutter your repository, making it difficult to navigate and manage. These are for example `.venv` folders.
#### 3. System Files 🖥️: 
System-generated files like cache files, log files, or any other automatically generated file should not crowd your repository. Keeping them out keeps your repository clean and focused.

In case you want to learn more details about all the possible files to ignore, [here you have an in-depth guide](https://www.atlassian.com/git/tutorials/saving-changes/gitignore). However, most of the time, you will look for specific pre-built `.gitignore` files, via tools like the one [in here](https://www.toptal.com/developers/gitignore/). We encourage you to look for the most common IDEs, operating systems or programming languages (_e.g._, VSCode, PyCharm, Linux, Python, Jupyter Notebooks, ...)

## Visual Aid 🎥

Learn more about the `.gitignore` file and see it in action in this visual tutorial. Notice specially how he uses several git commands you have already seen, including how he resets HEAD.

<img src="../images/1Qk8jrBrp9ohd.jpg" alt="" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=1Qk8jrBrp9o)


Incorporating a `.gitignore` file is not just an option; it's a necessity for maintaining the integrity and cleanliness of your codebase.


