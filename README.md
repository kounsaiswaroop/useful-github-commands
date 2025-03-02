<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Git Cheat Sheet</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }
        h1, h2, h3 {
            color: #333;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 5px;
            border-radius: 3px;
            font-family: monospace;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        table, th, td {
            border: 1px solid #ddd;
        }
        th, td {
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #f4f4f4;
        }
        a {
            color: #0366d6;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

<h1>GitHub Git Cheat Sheet</h1>

<p>Git is the free and open-source distributed version control system that’s responsible for everything GitHub-related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.</p>

<h2>Installation & GUIs</h2>
<p>With platform-specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command-line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization.</p>

<ul>
    <li><strong>GitHub for Windows</strong>: <a href="https://windows.github.com" target="_blank">https://windows.github.com</a></li>
    <li><strong>GitHub for Mac</strong>: <a href="https://mac.github.com" target="_blank">https://mac.github.com</a></li>
    <li><strong>Git for All Platforms</strong>: <a href="http://git-scm.com" target="_blank">http://git-scm.com</a></li>
</ul>

<h2>Setup</h2>
<p>Configuring user information used across all local repositories.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git config --global user.name "[firstname lastname]"</code></td>
        <td>Set a name that is identifiable for credit when reviewing version history.</td>
    </tr>
    <tr>
        <td><code>git config --global user.email "[valid-email]"</code></td>
        <td>Set an email address that will be associated with each history marker.</td>
    </tr>
    <tr>
        <td><code>git config --global color.ui auto</code></td>
        <td>Set automatic command-line coloring for Git for easy reviewing.</td>
    </tr>
</table>

<h2>Setup & Init</h2>
<p>Configuring user information, initializing, and cloning repositories.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git init</code></td>
        <td>Initialize an existing directory as a Git repository.</td>
    </tr>
    <tr>
        <td><code>git clone [url]</code></td>
        <td>Retrieve an entire repository from a hosted location via URL.</td>
    </tr>
</table>

<h2>Stage & Snapshot</h2>
<p>Working with snapshots and the Git staging area.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git status</code></td>
        <td>Show modified files in the working directory, staged for your next commit.</td>
    </tr>
    <tr>
        <td><code>git add [file]</code></td>
        <td>Add a file as it looks now to your next commit (stage).</td>
    </tr>
    <tr>
        <td><code>git reset [file]</code></td>
        <td>Unstage a file while retaining the changes in the working directory.</td>
    </tr>
    <tr>
        <td><code>git diff</code></td>
        <td>Show the diff of what is changed but not staged.</td>
    </tr>
    <tr>
        <td><code>git diff --staged</code></td>
        <td>Show the diff of what is staged but not yet committed.</td>
    </tr>
    <tr>
        <td><code>git commit -m "[descriptive message]"</code></td>
        <td>Commit your staged content as a new commit snapshot.</td>
    </tr>
</table>

<h2>Branch & Merge</h2>
<p>Isolating work in branches, changing context, and integrating changes.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git branch</code></td>
        <td>List your branches. A <code>*</code> will appear next to the currently active branch.</td>
    </tr>
    <tr>
        <td><code>git branch [branch-name]</code></td>
        <td>Create a new branch at the current commit.</td>
    </tr>
    <tr>
        <td><code>git checkout</code></td>
        <td>Switch to another branch and check it out into your working directory.</td>
    </tr>
    <tr>
        <td><code>git merge [branch]</code></td>
        <td>Merge the specified branch’s history into the current one.</td>
    </tr>
    <tr>
        <td><code>git log</code></td>
        <td>Show all commits in the current branch’s history.</td>
    </tr>
</table>

<h2>Inspect & Compare</h2>
<p>Examining logs, diffs, and object information.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git log</code></td>
        <td>Show the commit history for the currently active branch.</td>
    </tr>
    <tr>
        <td><code>git log branchB...branchA</code></td>
        <td>Show the commits on branchA that are not on branchB.</td>
    </tr>
    <tr>
        <td><code>git log --follow [file]</code></td>
        <td>Show the commits that changed the file, even across renames.</td>
    </tr>
    <tr>
        <td><code>git diff branchB...branchA</code></td>
        <td>Show the diff of what is in branchA that is not in branchB.</td>
    </tr>
    <tr>
        <td><code>git show [SHA]</code></td>
        <td>Show any object in Git in human-readable format.</td>
    </tr>
</table>

<h2>Share & Update</h2>
<p>Retrieving updates from another repository and updating local repos.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git remote add [alias] [url]</code></td>
        <td>Add a Git URL as an alias.</td>
    </tr>
    <tr>
        <td><code>git fetch [alias]</code></td>
        <td>Fetch down all the branches from that Git remote.</td>
    </tr>
    <tr>
        <td><code>git merge [alias]/[branch]</code></td>
        <td>Merge a remote branch into your current branch to bring it up to date.</td>
    </tr>
    <tr>
        <td><code>git push [alias] [branch]</code></td>
        <td>Transmit local branch commits to the remote repository branch.</td>
    </tr>
    <tr>
        <td><code>git pull</code></td>
        <td>Fetch and merge any commits from the tracking remote branch.</td>
    </tr>
</table>

<h2>Tracking Path Changes</h2>
<p>Versioning file removes and path changes.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git rm [file]</code></td>
        <td>Delete the file from the project and stage the removal for commit.</td>
    </tr>
    <tr>
        <td><code>git mv [existing-path] [new-path]</code></td>
        <td>Change an existing file path and stage the move.</td>
    </tr>
    <tr>
        <td><code>git log --stat -M</code></td>
        <td>Show all commit logs with an indication of any paths that moved.</td>
    </tr>
</table>

<h2>Rewrite History</h2>
<p>Rewriting branches, updating commits, and clearing history.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git rebase [branch]</code></td>
        <td>Apply any commits of the current branch ahead of the specified one.</td>
    </tr>
    <tr>
        <td><code>git reset --hard [commit]</code></td>
        <td>Clear the staging area and rewrite the working tree from the specified commit.</td>
    </tr>
</table>

<h2>Ignoring Patterns</h2>
<p>Preventing unintentional staging or committing of files.</p>

<pre>
Logs/
*.notes
pattern*/
</pre>

<p>Save a file with desired patterns as <code>.gitignore</code> with either direct string matches or wildcard globs.</p>

<code>git config --global core.excludesfile [file]</code>
<p>System-wide ignore pattern for all local repositories.</p>

<h2>Temporary Commits</h2>
<p>Temporarily store modified, tracked files in order to change branches.</p>

<table>
    <tr>
        <th>Command</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>git stash</code></td>
        <td>Save modified and staged changes.</td>
    </tr>
    <tr>
        <td><code>git stash list</code></td>
        <td>List stack-order of stashed file changes.</td>
    </tr>
    <tr>
        <td><code>git stash pop</code></td>
        <td>Write working from the top of the stash stack.</td>
    </tr>
    <tr>
        <td><code>git stash drop</code></td>
        <td>Discard the changes from the top of the stash stack.</td>
    </tr>
</table>

<h2>GitHub Education</h2>
<p>Teach and learn better, together. GitHub is free for students and teachers. Discounts are available for other educational uses.</p>

<ul>
    <li><strong>Email</strong>: <a href="mailto:education@github.com">education@github.com</a></li>
    <li><strong>Website</strong>: <a href="https://education.github.com" target="_blank">education.github.com</a></li>
</ul>

</body>
</html>
