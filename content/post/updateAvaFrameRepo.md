---
title: "OpenNHM Migration: Update Git Remotes"
date: 2025-11-14T00:00:00+01:00
author: "Felix"
draft: false
tags:
  - openNHM
  - avaframe
description: "Update on the OpenNHM transition: Please update your git remotes to point to the new location. Read more ... "
---

# Updating Your Git Remote for AvaFrame

The AvaFrame repository has moved to a new GitHub organization. Please update your local git remote to point to the new location.

## Steps to Update

**1. Check your current remote:**

```bash
git remote -v
```

**2. Update the remote URL:**

If you're using HTTPS:

```bash
git remote set-url origin https://github.com/OpenNHM/AvaFrame.git
```

If you're using SSH:

```bash
git remote set-url origin git@github.com:OpenNHM/AvaFrame.git
```

**3. Verify the change worked:**

```bash
git remote -v
```

You should now see the new URL with `OpenNHM` as the organization.

## Additional Notes

- Your existing clone will continue to work due to GitHub's automatic redirect, but please update your remote to ensure continued functionality
- If you have multiple remotes configured (such as `upstream`), update each one that pointed to the old organization URL
- If you're unsure which format (HTTPS vs SSH) you're using, check the output of `git remote -v` - SSH URLs start with `git@github.com:`

Felix