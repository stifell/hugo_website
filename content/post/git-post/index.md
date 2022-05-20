---
title: Version control. Git.
subtitle: Article about Version сontrol and Git

# Summary for listings and search engines
summary: Article about Version сontrol and Git

# Link this post with a project
projects: []

# Date published
date: '2022-05-05T00:00:00Z'

# Date updated
lastmod: '2022-05-05T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/wX2L8L-fGeA)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---

## Article:

## Version control

Version Control Systems (VCS) are used when several people work on one project. Usually, the main project tree is stored in a local or remote repository, to which access is configured for project participants. When making changes to the project content, the version control system allows you to fix them, combine changes made by different project participants, roll back to any earlier version of the project, if required.

In classical version control systems, a centralized model is used, assuming a single repository for storing files. Most version control functions are performed by a special server.
The project participant (user) receives the version of files he needs before starting work through certain commands. After making changes, the user places the new version in the repository. At the same time, previous versions are not deleted from the central repository and you can return to them at any time. The server can not to save the full version of the modified files, but to perform a so—called delta compression - to save only changes between successive versions, which reduces the amount of data stored.

Version control systems support the ability to track and resolve conflicts that may arise when several people are working on a single file. You can merge (merge) changes made by different participants (automatically or manually), manually select the desired version, cancel the changes altogether or lock files for modification. Depending on the settings, the lock is not allows other users to get a working copy or prevents changing the working copy of the file by means of the OS file system, thus providing privileged access to only one user working with the file.

Version control systems can also provide additional, more flexible functionality. For example, they can support working with multiple versions of a single file, keeping a common history of changes up to the point of branching versions and their own change histories of each branch. In addition, it is usually available information about which of the participants, when and what changes were made. Usually this kind of information is stored in the change log, access to which can be restricted. Unlike the classical ones, in distributed version control systems, a central
repository is not mandatory.

Among the classic VCS, the most famous are CVS, Subversion, and among the distributed ones — Git, Bazaar, Mercurial. The principles of their work are similar, they differ mainly
in the syntax of the commands used in the work.

## Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows.
The system is designed as a set of programs specially designed for their use in scenarios. This makes it convenient to create specialized version control systems based on Git or user interfaces. For example, Cogito is just such an example of a wrapper to Git repositories, and StGit uses Git to manage a collection of fixes (patches).

Git supports rapid separation and merging of versions, includes tools for visualization and navigation through the non-linear development history. Like Darcs, BitKeeper, Mercurial, Bazaar and Monotone, Git provides each developer with a local copy of the entire development history, changes are copied from one repository to another.

Remote access to Git repositories is provided by a git daemon, SSH or HTTP server. The git-daemon TCP service is included in the Git distribution and is, along with SSH, the most common and reliable access method. The HTTP access method, despite a number of restrictions, is very popular in controlled networks, because it allows you to use existing network filter configurations.
