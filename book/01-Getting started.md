## Creating a new book

Create a new repo from the template: https://github.com/readcodebooks/hello-codebook

## Making changes

Edit a file, `git commit`, `git push`, and your changes will show up automatically 🎉 You don't even need to refresh your browser!

## Chapters

You can add chapters that show up in the sidebar:

```diff
 book/
+  01-Intro.md
   info.json
   README.md
```

![](https://i.imgur.com/YdaNSi0.png)

## Embedding commits

Wondering how the files above are shown? They're actually not hard-coded, the diffs are dynamically computed based on your git history!

To **embed a commit**, create a code fence with the tag `commit` and type the exact name of the commit:

    ```commit
    initialize book dir
    ```

CodeBook will automatically fetch the commit from the git history, compute diffs, and embed them directly into the page.

You can also click **View full code** to open a readonly Monaco editor at that point!

![](https://i.imgur.com/Xy9kdCS.png)
