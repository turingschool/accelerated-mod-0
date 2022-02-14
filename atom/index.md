---
layout: page
title: Atom & Markdown
---

## Learning Goals

- Open a specific project in Atom from the command line
- Navigate the Atom interface, using some keyboard shortcuts
- Write valid Markdown files in Atom

## Atom

Atom is where we write the code that powers our applications. It offers features like syntax highlighting and line numbers (and many more!) that make it easier for developers to write code efficiently.

We will open the Atom application _from_ the Terminal. Since you'll have so many files and directories on your machine, you'll want to get into the habit of only opening the project you are currently working on.

To open Atom from the Terminal, navigate to the directory you want to open, and run:

```bash
atom .
```

**Practice this right now.** If Atom does not open, make sure Atom is in the Applications folder, not the Downloads folder. If it is still not working, DM your Mod 0 Lead.

<div class="try-it">
  <h3>Install Auto-Save</h3>
  <p>Either through exploring the options in the menu or Googling, figure out to install auto-save in Atom. Having this installed will save you a ton of headaches in the future!</p>
</div>

## Markdown Files

Markdown is a lightweight markup language that converts to HTML and can be displayed on the web. It is used widely in the tech industry for documentation. You'll use it in various ways at Turing - most commonly, to document and showcase your projects.

Your task is to create a "Plan for Mod 0" **documenting your gameplan for success in Mod 0**, using Markdown. You'll do this in a GitHub Gist.

Using [this markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), create a new Gist in GitHub of your own by clicking the New Gist button in the upper right-hand corner of the screen.

Images can be a little tricky in gists and Github - be sure to check out the [drag-n-drop shortcut from the first answer on this Stack Overflow post](https://stackoverflow.com/questions/16425770/gist-how-are-images-uploaded-to-a-gist)! 

In the box to title your Gist, follow this format: firstName_lastName_mod_0_plan.md

**NOTE: Remember to add a .md file extension to filename of your new Gist. Otherwise it will not register as markdown.**

In addition to documenting your gameplan for success in Mod 0, incorporate each of the following features into your Gist:

- at least two headings of different sizes
- at least one numbered list
- at least one bullet point list
- at least one bold word/phrase
- at least one italic word/phrase
- at least one Ruby code block
- at least one inline code block (greyed text)
- at least one image
- at least one link to a resource (technical or not) that you've used or plan to use

## Terminal & Atom Practice

Complete the challenges below to continue to build fluency with using your Terminal and Atom:

### Challenge #1

1. Run `cd` to get to your home directory (you’ll probably already be here, but do it just to be sure)
1. Make a new directory called `my_first_projects`
1. Make another new directory called `my_other_projects`
1. List the contents of your directory (you should see these two directories you just made in the list)
1. Remove the `my_other_projects` directory
1. Navigate into the `my_first_projects` directory
1. Make a file called `ruby.md`
1. Make a file called `javascript.md`
1. Add a list of things you already know about Ruby in the `ruby.md` file
1. List the contents of your directory (you should see the three files you just created)
1. Delete the `javascript.md` file
1. Get back out of the `my_first_projects` directory
1. List the contents of your directory (you should see `my_first_projects`)
1. Remove the `my_first_projects` directory

### Challenge #2

1. Run `cd` to get to your home directory (you’ll probably already be here, but do it just to be sure)
1. Make a new directory called `practice`
1. Move into the `practice` directory
1. Print the path to your current directory
1. Make a file called `terminal.md`
1. List the contents of your directory (you should see the `terminal.md` file you just created)
1. In the `terminal.md` file, write 1-3 sentences explaining what the Terminal is and does, in your own words. Add an appropriate title/header
1. Get back out of the `practice` directory
1. Remove the `practice` directory

## Check For Understanding

- Self Evaluation
- Lingering Questions
- Submit Markdown Gist in Google Form
- Record yourself doing a challenge of your choice - do it as if you are teaching someone who doesn't know what this, explaining what each step does using technical vocabulary