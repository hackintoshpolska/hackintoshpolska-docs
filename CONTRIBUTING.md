# Contributing guidelines
We are very happy that you decided to contribute to our project. At the beggining we would like to thank you from the very bottom of our hearts. However there are certain rules and guidelines we would like you to follow in order to make your guide applicable for the site.

## Development environment
### Needed dependencies
You will need several packages installed in order to build and edit the site.
* [Latest package of Go](https://golang.org)
* [Hugo Extended version](https://gohugo.io)
* [NodeJS LTS](https://nodejs.org)
* Git installed
* Visual Studio Code or any other code editor

### Prepare working environment
After installing mandatory dependencies fork the repository and clone your fork locally:
```
git clone --recurse-submodules https://github.com/[yourFork]/hackintoshpolska-docs.git
cd hackintoshpolska-docs
```

Add upstream remote that points to the project repository:
```
git remote add upstream https://github.com/hackintoshpolska/hackintoshpolska-docs.git
git fetch upstream
```

Install mandatory npm modules:
```
npm install
```
For Building site (Preview) use:
```
hugo serve
```
That should be enough to set up your working environment.

## Creating new guides
Location `content/xx/` contains all the guides that are available under https://hackintoshpolska.pl/docs. for the given language. If you create the new guide section create the corresponding folder with **English lowercase** slug name, for example `getting-started-amd`. Each folder should contain the `_index.md` file with the following header:
```yaml
---
title: Page title
linkTitle: Link page title.
weight: number of the weight in structure
description: >
    Short description of the following section.
---
```

Next create the `.md` following the same name principles as the section folder, for example `getting-started-amd.md`. The chapter file should containd the given header:
```yaml
---
title: Chapter title
linkTitle: Chapter link title
weight: number of the weight in structure
authors: ["Author 1", "Author 2"]
description: >
  Short description of the chapter.
---
```
The `authors` value is your name and is optional. If you're modifying existing file please add your name in the `authors` field.

For the other basic writing guidelines please refer to official [Docsy Documentation](https://www.docsy.dev/docs/).

## Share your contribution
If you're already happy with your changes it's best to share your contribution by creating a Pull Request in [upstream repository](https://github.com/hackintoshpolska/hackintoshpolska-docs/compare). Don't forget to assign repository maintainers for review!

Before creating a pull request always remember to rebase your branch with `upstream/master` and then create a pull request:
```
git fetch upstream
git rebase upstream/master
```
If you have any conflicts please resolve them locally then merge it to your branch.

## Creating an issue
If you found any issues with the guides, site or anything else please ceate proper issue in the [Issues page](https://github.com/hackintoshpolska/hackintoshpolska-docs/issues).
