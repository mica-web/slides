# Understanding git

There will be slides for this portion of the class, but they are not complete yet. Other resources that might help:

- https://www.liquidlight.co.uk/blog/article/git-for-beginners-an-overview-and-basic-workflow/
- http://rogerdudler.github.io/git-guide/
- If you prefer videos: https://www.youtube.com/playlist?list=PL5-da3qGB5IBLMp7LtN8Nc3Efd4hJq0kD
- http://pel-daniel.github.io/git-init/


# Getting started with git & GitHub

1. Go through steps 1-3 in "[Setting up Git](https://help.github.com/articles/set-up-git/#setting-up-git)"
1. Under "Next steps: Authenticating with GitHub from Git," follow the instructions for "[Connecting over SSH](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)"
    1. [Check if you have existing SSH keys](https://help.github.com/articles/checking-for-existing-ssh-keys/)
        - if you do, follow the instructions to [add your keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent)
        - if you do not, follow the directions to [generate and add ssh keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)


# Getting started with VS Code
[Basics of the VS Code interface](https://code.visualstudio.com/docs/getstarted/userinterface)

1. Sidebar
1. Activity Bar
1. Status Bar
1. Panels
1. Editor


## Updating VS Code settings

- Editor Format On Paste, Editor Format On Save = true
- Editor Word Wrap = on
- Files Insert Final New Line = true


## Adding VS Code plugins

In class, students will read about the following plugins and install them:

1. **Beautify** by HookyQR
1. **Live Server** by Ritwick Dey
1. **Live Sass Compiler** by Ritwick Dey
1. **Intellisense for CSS class names in HTML** by Zignd
1. **Path Intellisense** by Christian Kohler
1. **scss-scan** by aaronphy
1. **minify** by HookyQR
1. **Auto Rename Tag** by Jun Han
1. **Bracket Pair Colorizer** by CoenraadS


# VS Code + git

1. Create a directory called `sites`
    - If on macOS, do this via Finder within your user directory (i.e., `/Users/<YOUR_USERNAME>`); end result should be `/Users/<YOUR_USERNAME>/sites/`
    - If on Windows, do this via File Explorer directly in your `C:\` root folder; end result should be `C:\sites\`
1. Create a directory titled `gd431` inside your new `sites` directory
1. Open VS Code
1. Go to `File->Open` and open your `gd431` directory
1. Open VS Code's integrated terminal:
    - `Control` + `` ` `` (the backtick character)
    1. Note that, by default, VS Code's integrated terminal shows you as inside your project   directory: so helpful 🙌
1. Type `git init` to make your project directory (`sites/gd431`) into a git repository
1. Type `git status` in the integrated terminal to see details about your new repo and verify git is properly initialized
    - the `status` command makes no changes; it only provides info
1. Create and save a new blank file `index.html`
1. Does anyone remember the Emmet shorthand to start a new HTML file?
    - `!` then tab
    - Save `index.html`
1. Type `git status` in the integrated terminal
    - Should show that you have untracked files!
    - You'll also see a badge next to the source control icon on your activity bar
1. Click on the source control icon on your activity bar
1. Stage your changes on `index.html`; you can do this by:
    - Clicking on or hovering over the `index.html` filename and clicking on the "plus sign" icon
    - On macOS, two-finger tapping the filename and choosing "Select Changes" from the menu
    - On Windows, right clicking the filename and choosing "Select Changes" from the menu
1. You can "unstage" a file in a similar way by clicking the "minus sign" icon or choosing "Unstage Changes" from the same menu.
1. In the integrated terminal, type `git status` again to see which file(s) you've staged
1. In the "Message" input, type "Create repo" -- this is a "commit message" which will be logged in the repository's history of changes and updates
1. After you've completed your message, press `Command` + `Enter` (macOS) or `Control` + `Enter` (Windows) to post your commit message and associated changes
1. Inside your HTML file:

```
<h1>GD 431: Angelique Weger</h1>
<h2>Assignments</h2>
<ul>
    <li><a href="resume/">Resume</a></li>
    <li><a href="poster/">Poster</a></li>
</ul>
```

1. Click on the source control icon in your activity bar
1. Click on `index.html` -- a `git diff` view opens up
    - This shows you the things you've added to your file in green and what you've removed in red
1. After reviewing your changes, stage them and make a new commit: "Add project links"
1. Inside `gd431`, create two more directories: `resume` and `poster`
1. Create an `index.html` inside both the `resume` and `poster` directories. Create the boilerplate HTML and just add in an `h1` element that says "Resume" or "Poster", as appropriate
1. In your VS Code status bar (the bottom line across your editor), click "Go Live"
    - Can't find the status bar? Review the [VS Code interface](https://code.visualstudio.com/docs/getstarted/userinterface)
1. This will allow you to verify your links and understand the basics of the Live Server plugin. It's uncomplicated but oh-so helpful!
1. Stage these changes and make a new commit: "Update project structure"
1. `git log --oneline` to see history of your commits
    - Press `q` (for "quit") to close the history

## Adding your project to GitHub

- Go to GitHub.com and log in
- Follow steps 1-6 of [Create a repo](https://help.github.com/articles/create-a-repo/)
    - Name the repo "gd431" to match your project folder
- After the repo is created, scroll down to "…or push an existing repository from the command line"
- Copy the commands in that section
- Go back to VS Code and enter those commands in the integrated terminal
- After you push your code, you should go back to the repo page on GitHub and refresh it to see your content and commits 🙌

## Branches

- By default, git has created a branch for your project called "master"
- In the VS Code integrated terminal, type `git branch` to see a list of branches for your repo; right now, you should see only one: master
- You can also see what branch you're working on in the the VS Code status bar, on the far left
- Creating a new branch is like using "File save as..." on a document; it takes the current state of your repo and creates a duplicate of it
- We use branches to isolate our work, especially when working on teams, and, in this course, to get feedback on things via pull requests (which is a request to have your branch be integrated or merged into the master branch)

More info: https://guides.github.com/introduction/flow/

1. In the integrated terminal, type `git branch migrate-from-codepen`
    - This will create a new branch with the name "migrate-from-codepen"
    - Branch names can't have spaces in them
1. In the integrated terminal, type `git branch`
    - You'll see the name of your new branch, but also note that you're still *on* the master branch
1. Switch branches with a command `git checkout`
1. In the integrated terminal, type `git checkout migrate-from-codepen` to switch to your new branch
1. You'll also see the branch name update in the far left of the status bar


## Migrating your projects from CodePen to VS Code

1. Make all changes on your new branch "migrate-from-codepen" and no further changes on the master branch
1. Students should now copy their existing final/most recent HTML from the resume project over into the `resume/index.html`. They should also create a `styles` directory inside of the `resume` directory. Inside the `styles` directory, you should create a new file titled `styles.scss` and, in that, copy over your Sass from your latest resume CodePen.
1. In the VS Code status bar, click "Watch Sass" to compile your `styles.css` from `styles.scss` 👍 
1. After you've successfully moved over your resume (and previewed it in the browser), stage those changes and make a new commit.
1. Then repeat the process for your poster project.
1. When you're done, you want to push your branch to GitHub; do this by typing `git push origin migrate-from-codepen` in the integrated terminal


### Remember

- You'll need to add a link to your `styles.css` in your `index.html`:
    - Above the `title` in your `head`, type `link` and press `<tab>` to have Emmet autocomplete the link tag for you.
    - Update the `href` to your file, e.g.
```
<link rel="stylesheet" href="styles/styles.css">
```

- If you added any external stylesheets or pens to your CodePen, including  Google Fonts, you'll now need to add them to your project in VS Code.
    - You can check this by going to the CSS Settings on your CodePen and   looking under "Add External Stylesheets/Pens"


# Best practices for commit messages

- Commit early
- Commit often
- Be useful
- Be brief (~50 char)
- Start with a verb in the present tense, like giving a command:
    - Update body font to Roboto
    - Fix typo in nav
    - Note tense: not updates or fixed
- Doesn't need to mention which file you worked on; this info is tracked by git

https://thenewstack.io/getting-legit-with-git-and-github-the-art-of-the-commit-message/

