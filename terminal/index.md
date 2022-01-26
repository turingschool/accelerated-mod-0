---
layout: page
title: Terminal
---

## Learning Goals

- Navigate through directories from the command line
- Make and remove files and directories from the command line

## Files, Directories, and Paths

On your computer, you probably have many <span class="vocab">files</span> and <span class="vocab">directories</span>. Files are things like text documents, images, videos, PDFs, etc. Directories (or folders) are the structures we use to organize these files.

In the diagram below, we would say that there's a directory called `essays` that contains three files: `life_lessons.docx`, `book_report.docx`, and `literary_analysis.docx`:

<hr>
<h4>Example #1</h4>
<div class="flex-container">
  <div>
    <img src="images/files_directories_1.png" alt="files and directories 1">
  </div>
  <div>
    A <span class="vocab">file path</span> is a way to notate where a file "lives" on your computer. This is the structure:
    <pre>directory_name/file_name.extension</pre>
    The file path for the first file in the diagram would be:
    <pre>essays/life_lessons.docx</pre>
    <p>What is the path for <code>book_report.docx</code>?</p>
    <textarea rows="1" name="" style="width:100%;"></textarea>
    <p>What is the path for <code>literary_analysis.docx</code>?</p>
    <textarea rows="1" name="" style="width:100%;"></textarea>
  </div>
</div>
<div class="things-to-note">
  <h4>Things to Note</h4>
  <ol>
    <li>A file cannot be inside of another file. This means that every part of the path <strong>before</strong> the actual file is a directory. </li>
    <li>For now, we will follow two convention rules: </li>
    <ul>
      <li>Use lower case letters when naming directories and files</li>
      <li>Use underscores (_) or hyphens (-) instead of spaces when naming directories and files. However, keep in mind that different languages and frameworks have different conventions. Rather than arguing over which approach is "correct" (you'll find a lot of this on the internet), it is more important to pick an approach and be consistent. For today's lesson, we'll use the underscore (_) approach.</li>
    </ul>
    <li>Folders do not have extensions (like <strong>.docx</strong> or <strong>.md</strong> or <strong>.csv</strong>, etc.). File names do have extensions.</li>
    <li>File extensions matter. A <strong>.md</strong> file will behave differently than a <strong>.docx</strong> file, which will also behave differently than a <strong>.rb</strong> file because the extensions help the operating system figure out which application can open the file an dhow to read it.</li>
  </ol>
</div>
<hr>
<h4>Example #2</h4>
<div class="flex-container">
  <div>
    <img src="images/files_directories_3.png" alt="files and directories 2">
  </div>
  <div>
    <p>The path for the grading.txt file is</p>
    <pre>to_do/work/grading.txt</pre>
    <p>What is the path for cleaning.txt?</p>
    <textarea rows="1" name="" style="width:100%;"></textarea>
    <p>What is the path for recurring.txt?</p>
    <textarea rows="1" name="" style="width:100%;"></textarea>
    <p>What is the path for data_entry.csv?</p>
    <textarea rows="1" name="" style="width:100%;"></textarea>
  </div>
</div>

<div class="things-to-note">
  <h4>Things to Note</h4>
  <p>We commonly refer to directories with an analogy of <span class="vocab">parent</span> and <span class="vocab">child</span>. In the above example <code>to_do</code> is the <span class="vocab">parent</span> directory of the <code>personal</code> and <code>work</code> directories. <code>projects_to_delegate</code> is a <span class="vocab">child</span> directory of the <code>work</code> directory.</p>
</div>

<hr>

## Terminal and Command Line

The <span class="vocab">Terminal</span> is what we call a command line interface. It's the program we use to give commands to the computer. We use the command line because it is a faster and more precise way to navigate our file systems, and certain tools can only be downloaded and accessed via the command line. In this lesson, you will learn 9 commonly used commands, but there are many more you'll learn throughout your time at Turing and in your career.

Your Terminal will look something like this:

<img src="images/david_terminal.png" alt="">

<div class="try-it">
  <h3>Independent Research</h3>
  <p>Take 3 minutes (max) to research each of the following Terminal commands: <code>pwd</code>, <code>touch</code>, and <code>cd ..</code>. Take note of what you learn, or questions/confusion that arises from this research</p>
</div>

<div class="things-to-note">
  <h3>Reflection</h3>
  <ul>
    <li>How did it feel to research a technical topic?</li>
    <li>Did you struggle? If so, was the struggle productive or unproductive?</li>
    <li>Did you stick to the time limits?</li>
  </ul>
</div>

### Terminal Commands

Each command has a different utility. Some find it helpful to categorize the type of utility by action, safe/informative, and destructive. Read below and follow the activities provided to learn about each of the 9 commands.

#### Action Commands

- `mkdir`
- `touch`
- `clear`
- `cd`
- `cd ..`

#### Safe/Informative Commands

- `pwd`
- `ls`

#### Destructive Commands

- `rm`
- `rm -rf`

### 1. Where am I? (`pwd`)

When you open the terminal, you will be in your home directory. Being in various directories will allow you to do different things, just like you can do different things at home vs. on vacation vs. at work.

To figure out where you are in your computer's directory structure, run `pwd`. `pwd` stands for "print working directory"

```
timo@Tims-MacBook-Pro:~$ pwd
/Users/timo
```

You'll see the path from the root of your computer to your current directory.

### 2. Make a Directory (`mkdir`)

To make a folder using the visual interface of Finder, this is what you might do:

<img src="images/mkdir.gif" alt="making a folder using finder" style="height: 250px">

We can make new directories with the `mkdir` command. Unlike `pwd` where we didn't need to run anything else, we'll need to add a name for the directory. Keep your directories lowercase with no spaces. If you need to use a space, use the underscore (\_).

For example, the following two commands will create two directories called `work_spreadsheets` and `latest_projects`:

```
timo@Tims-MacBook-Pro:~$ mkdir work_spreadsheets
timo@Tims-MacBook-Pro:~$ mkdir latest_projects
```

You won't get any confirmation that your directory was created -- you'll just see a new command prompt ready for your next command.

### 3. Listing Contents of a Directory (`ls`)

With a visual interface (as shown in the gif above), you can easily see the contents of a directory. On the command line, it's a little different.

To see what is inside of a directory, we use the `ls` command which stands for list. As an example, let's assume that we have the directories and files from this diagram on a computer:

<div class="flex-container">
  <div>
    <img src="images/files_directories_2.png" alt="files and directories 2">
  </div>
  <div>
    If I was in the essays directory and I ran <code>ls</code>, this is what I'd see:

  <pre>timo@Tims-MacBook-Pro:~/essays$ ls
  book_projects    life_lessons.docx    notes.docx</pre>

  <p>You will only see the directories and files that are directly inside of where you are. You will not see any directories or files that are nested down the path. This is why we do not see the contents of book_projects listed.</p>

  <p>Now assume we're in the book_projects directory. If I run <code>ls</code>, I'll see this:</p>

  <pre>timo@Tims-MacBook-Pro:~/essays/book_projects$ ls
  literary_analysis.docx    book_report.docx</pre>

  </div>
</div>

### 4. Go Into a Directory (`cd`)

You can move into a directory using the `cd` command, which stands for "change directory". After `cd`, type the name of the directory you want to go into.

<div class="flex-container">
  <div>
    <img src="images/files_directories_2.png" alt="files and directories 2">
  </div>
  <div>
    For example, if I was in the <code>essays</code> directory and wanted to move into the <code>book_projects</code> directory to see my documents, I would run the following:
<pre>
timo@Tims-MacBook-Pro:~/essays$ cd book_projects
timo@Tims-MacBook-Pro:~/essays/book_projects$
</pre>

We see that the second command prompt now lists the path of new directory that we're in.

From there, if I used the <code>ls</code> command, I would be able to see the contents of my folder:

<pre>
timo@Tims-MacBook-Pro:~/essays/book_projects$ ls
literary_analysis.docx    book_report.docx
</pre>
  </div>
</div>

<div class="things-to-note">
  <h4>Things to Note</h4>
  <p>You can't pick any random directory from your computer to give to the <code>cd</code> command. It has to be a directory inside wherever you currently are (or you need to use the full path to get to that directory, which we won't talk about in this lesson).</p>
</div>

### 5. Get Out of a Directory (`cd ..`)

To get out of a directory you're in, we use `cd ..` (with a space between the d and the first dot). This means "go back up one level."

If I'm in the `book_projects` directory and I want to get back to `essays`, this is what I'd run:

```
timo@Tims-MacBook-Pro:~/essays/book_projects$ cd ..
timo@Tims-MacBook-Pro:~/essays$
```

Notice that my path no longer includes `book_projects` because I'm outside of that folder now.

**Note** You never want to `cd` into a directory above your home directory. This area requires admin permissions, and there is no practical use case for being there.


<div class="try-it">
  <h3>Try It: cd and cd ..</h3>
  <p>Let's try to figure out the following scenarios together.</p>
  <div class="flex-container">
    <div>
      <img src="images/files_directories_3.png" alt="files and directories 2">
    </div>
    <div>
      <p>If I'm in the <code>work</code> directory, what do I need to run to get to <code>to_do</code>?</p>
      <textarea name="" style="width:100%;"></textarea>
      <p>If I'm in the <code>projects_to_delegate</code> directory, what <strong>commands</strong> do I need to run to get to <code>to_do</code>?</p>
      <p><small>(We'll learn how to combine these momentarily)</small></p>
      <textarea name="" style="width:100%;"></textarea>
      <p>I'm in the <code>personal</code> directory. What <strong>commands</strong> do I need to run to get to <code>projects_to_delegate</code>?</p>
      <p><small>(We'll learn how to combine these momentarily)</small></p>
      <textarea rows="3" name="" style="width:100%;"></textarea>
      <p>I'm in the <code>projects_to_delegate</code> directory. What <strong>commands</strong> do I need to run to get to <code>personal</code>?</p>
      <p><small>(We'll learn how to combine these momentarily)</small></p>
      <textarea rows="3" name="" style="width:100%;"></textarea>
    </div>
  </div>
</div>

<div class="things-to-note">
  <h4>Things to Note</h4>
  <ul>
    <li>One can combine commands to navigate multiple levels through your directory structure. </li>
    <li>For the third example in the previous <strong>Try It</strong> section, one could navigate to the <code>projects_to_delegate</code> directory as long as one knows the path:</li>
    <code>cd ../work/projects_to_delegate</code>
    <li>For the fourth and final example above:</li>
    <code>cd ../../personal</code>   
    <li>Each level in the path is spearated by a <code>/</code></li>
  </ul>
</div>

### 6. Make a File (`touch`)

We know how to make directories (or folders) using the `mkdir` command. In order to make files inside of those directories, we use `touch`. The following two commands show how I would make two new files, `chapter_1.md` and `chapter_2.md`:

```
timo@Tims-MacBook-Pro:~/latest_projects$ touch chapter_1.md
timo@Tims-MacBook-Pro:~/latest_projects$ touch chapter_2.md
```

We don't see any confirmation that the file was created, but we can use `ls` to see what's inside the directory:

```
timo@Tims-MacBook-Pro:~/latest_projects $ ls
chapter_1.md    chapter_2.md
```

### 7. Clear your Terminal (`clear`)

Sometimes when you've entered a lot of Terminal commands, your terimal can get pretty cluttered. You can always use `clear` to "clean up" your Terminal workspace! The keyboard shortcut `cmd + k` does the same thing.

### 8. Remove a File (`rm`)

In the past, you've probably gotten rid of files by using the `Move to trash` button or dragging them into the trash, like this:

<img src="images/filetotrash.gif" alt="file to trash" style="height: 250px;">

We can remove files from the command line by running the `rm` command, like this:

```
timo@Tims-MacBook-Pro:~/latest_projects $ rm chapter_1.md
```

Again, we don't get a confirmation, but if I were to run `ls` right now, nothing would appear since the directory is now empty.

```
timo@Tims-MacBook-Pro:~/latest_projects $ ls
chapter_2.md
```

<div class="things-to-note">
  <h4>Things to Note</h4>
  <ul>
    <li>A file removed using the <code>rm</code> command <strong>does not</strong> go into your trash where you could restore it later</li>
    <li>Although it may be possible to recover files deleted with <code>rm</code>, it is a difficult process requiring special tools and time. For now, assume that any file you remove using the <code>rm</code> command is gone for good</li>
  </ul>
</div>

### 9. Remove a Directory and Its Contents (`rm -rf`)

We can use `rm` to remove a file, but we use a different command when we're removing a directory. Since a directory could potentially contain other files and directories inside of it, we use `rm -rf` which stands for remove _recursively_, or go inside this directory and remove everything inside of it as well.

In order to remove a directory, you must be OUTSIDE of that directory. For example, if I'm inside a `books` directory and I want to remove it, I first need to get out of it using `cd ..`, then use the `rm -rf books`:

```
timo@Tims-MacBook-Pro:~/latest_projects/books$ cd ..
timo@Tims-MacBook-Pro:~/latest_projects$ rm -rf books
```

Now when I run `ls`, I will no longer see `books` listed.

  <div class="try-it">
    <h3>Try It: Removing files (rm) and directories (rm -rf)</h3>
    <div class="flex-container">
      <div>
        <img src="images/files_directories_3.png" alt="files and directories 2">
      </div>
      <div>
        <p>We'll work through these exercises together.</p>
        <strong>For this scenario, assume that each question is independent of the rest, and that the starting point is always the diagram to the left.</strong>
        <p>I'm in <code>to_do</code>. What do I run to remove <code>random.txt</code>?</p>
        <textarea rows="1" name="" style="width:100%;"></textarea>
        <p>I'm in <code>to_do</code>. What do I run to remove the <code>personal</code> directory?</p>
        <textarea rows="1" name="" style="width:100%;"></textarea>
        <p>I'm in the <code>work</code> directory. What command(s) do I run to remove the <code>personal</code> directory?</p>
        <textarea rows="2" name="" style="width:100%;"></textarea>
        <p>I'm in the <code>projects_to_delegate</code> directory. What <strong>two commands</strong> do I run to remove the directory I'm currently in?</p>
        <textarea rows="2" name="" style="width:100%;"></textarea>
        <p>I'm in <code>projects_to_delegate</code>. What command(s) do I need to run to remove the <code>cleaning.txt</code> file?</p>
        <textarea rows="4" name="" style="width:100%;"></textarea>
      </div>
    </div>
  </div>

<br>

## Practice

- Go to [Turing Terminal](http://learn-terminal.turing.io/challenges) to use the Playground and complete the Challenges
- In your Terminal, recreate the file structures shown in the diagrams below. 

<img src="images/practice-1.png">
<br>
<br>
<br>
<img src="images/practice-2.png">
<br>
<br>
<br>

## Check For Understanding

[Follow the directions in this Gist](https://gist.github.com/ameseee/db5de325c40100dde3d6a5ad4888fa29) and submit your fork of it in the Google Form.

<br><br>