---
title: "Empty Commits"
date: 2024-06-09T02:18:00-08:00
draft: false
tags:
    [
        "Software Engineering",
        "Git",
        "Version Control",
        "Command Line",
        "Commits"
    ]
categories: ["Software Engineering"]
---

## Empty Commits

You can create an Git commit without any changes by adding the `--allow-empty` flag to the commit command. It should look like the following command:
    
```bash
    git commit --allow-empty -m "Commit message"
```

## Use Cases

Empty commits can be useful for a variety of reasons, such as:
-  Triggering a CI/CD pipeline
-  Marking a point in time
-  Adding a commit message to a branch