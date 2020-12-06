## Creating a GitHub repository

Visit [https://github.com/new](https://github.com/new) and enter a name like `hello-codebook` and check **Add a README file**, then click **Create repository**.

Run `git clone https://github.com/<you>/hello-codebook` then `cd hello-codebook`.

## Initializing the `book/` directory

Use your favorite text editor to make the following directory structure:

```
book/
  info.json
  README.md
```

```commit
initialize
```

> You might have noticed that the directory name here is `book2/`. That's because this guide itself is written as a CodeBook, so the `book/` directory is already being used! Ignore the `2` suffix and make sure your repository has a `book/` directory.

Now commit it with `git add book ; git commit -m "initialize book dir"`.

## Publishing

Install the `readcodebooks` GitHub App on your repository and choose **Only select repositories**: [https://github.com/apps/readcodebooks](https://github.com/apps/readcodebooks)

![](https://i.imgur.com/uAChbtt.png)

Then log into [https://codebook.page](https://codebook.page) with your GitHub account. The permissions only let CodeBook read your username and email address:

![](https://i.imgur.com/0zccDZg.png)

Now you should see your CodeBook in the list: [https://codebook.page/books](https://codebook.page/books)

![](https://i.imgur.com/9AqJ3yF.png)

Clicking on it will open the book for reading.

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
