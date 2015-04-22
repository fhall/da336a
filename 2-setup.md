---
layout: page
title: Setup
---

This section explains how to setup an account on GitHub and how to create and clone a repository. After this section you will have a repository on GitHub with collaborators and a local clone of the repository.

## <a name="create-account"></a>Create an account

The first thing you need to do is to create an account at GitHub. If you haven't done that already you can visit the [sign up page](https://github.com/). The sign up process is simple and a free account gives you unlimited public repositories. GitHub also has a free student account with five private repositories. To request a student acount visit [GitHub education](https://education.github.com/discount_requests/new)


## <a name="create-repo"></a>Create a repository

To create a repository on GitHub you click the plus symbol in the upper right corner of the global navigation.

![Create new respitory in GitHub]({{ site.baseurl }}public/images/github-create-repo.png)

Give your repository a name and click the "Create repository" button. The repository gets created and you are presented with some instructions how to get stared with the newly created respoitory.

## <a name="gitignore"></a>Untrack files and folders

One important file in Git is the [.gitignore](http://git-scm.com/docs/gitignore) file. This file holds information about what files the version control system shouldn't track. Git works well with source code and other assets but large files (> 100 MB) [cannot be pushed to Github](https://help.github.com/articles/working-with-large-files/). Generally it's not a good idea to save compiled binaries to Git since one of the strengths of Git is the possibility to select a specific version of the source code. Git helps at solving code conflicts but when working with binaries it's almost impossible to solve them so a tip is not to track your compiled binaries. There are of course exceptions. E.g. dll files and other binaries that you use for your project should be tracked.

To stop tracking files you add the file or folder to the .gitignore. Each file or folder should be on a separate line in the file and the path is relative to the .gitignore file. Some examples are listed below.

```
foo.py      // Don't track the file foo.py
foo/        // Don't track the directory foo and it's sub directories
foo/**/bar  // Don't track the directory bar that is a sub directory of foo
```

GitHub has a [collection of templates](https://github.com/github/gitignore) that are useful for most projects. If you work in [Visual Studio](https://github.com/github/gitignore/blob/master/VisualStudio.gitignore) or [Unity](https://github.com/github/gitignore/blob/master/Unity.gitignore) it's strongly recommended that you create a .gitignore file and add the lines listed to it.

## <a name="project-members"></a>Add project members

To collaborate on a project you could add collaborators to the repository. The [GitHub workflow](https://guides.github.com/introduction/flow/index.html) is a model that is often used in GitHub projects. If you add collaborators to the project you don't have to use that model and don't have to review each request.

In the local navigation to the right you can click Settings. On the settings page you can than click Collaborators in the navigation to the left. Find your project members and add them to the project.

## <a name="clone-repo"></a>Clone a repository

To work on an existing GitHub respository you need to do clone it. Depending on wheter you use a graphical client or the command the input

### <a name="clone-repo-command-line"></a>Command line

If you prefer the command line the command to clone a repository is simple. The command requires that you know your GitHub username, password and the repository you want to clone. The URL is also available in the bottom of the local navigation to the right in the GitHub repository.

```
git clone https://github.com/<username>/<repository>.git
```

![The clone URL on GitHub]({{ site.baseurl }}public/images/github-clone-repo-url.png)

### <a name="clone-repo-github-client"></a>GitHub client

The GitHub client has a simple way of cloning repositories. When logged in to the client you have a plus in the upper left corner of the app. To clone a repository simply click the plus, select clone and clone the repository you want to clone. You are then presented with a file dialog and can select where you want to store the project files.


![Clone a repository in the GitHub client]({{ site.baseurl }}public/images/github-client-clone.png)