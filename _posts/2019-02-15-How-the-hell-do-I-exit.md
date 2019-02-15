---
layout: post
title: 'How the hell do I exit:Guide to Vim'
date:   '2019-02-15'
categories: stories
tags: ['Terminal', 'Vim' ,]
comments: true
---
ESC? Nothing happens.

CTRL + C? No.

ESC ESC ESC? Nope. I'm stuck.

How to quit? 

<strong>Sound familiar?</strong>

<div class="image">
    <a href="/public/img/vim.gif">
        <img alt="'Project metrics' tab" src="/public/img/vim.gif" />
    </a>
</div>

I don't know about you, but I've been there. Until I decided to spend 10 minutes learning the very basics of Vim. 
This post is just enough to get you started and do not covers advance ! 

Vim is there by default with many operating systems (including most Linux distributions and Mac OS X), 
so , Just launch a terminal and type 'vim' to get started.

<strong>: why to use vim ?</strong>

With some learning, Vim can be more powerful than many graphical IDEs.
As it certainly doesn't eat hundreds of megs of memory just to view an empty file (like in, Eclipse).

<div class="image">
    <a href="/public/img/vim.png">
        <img alt="'Project metrics' tab" src="/public/img/vim.png" />
    </a>
</div>

<strong>The Basics</strong>

Some commands in this guide start with a colon: pressing it will display the command prompt where the subsequent command is written.

Commands written in CAPITAL LETTERS are specific keys: for example, ESC means the escape key on your keyboard.

Commands without a colon are more like hotkeys - they can be used in the Vim default mode (which is the mode Vim starts in).

All commands in Vim are case-sensitive.

<strong>EDITING TEXT</strong>

a) To start inserting text on the current cursor location:

i

b) To start inserting at the end of the current line:

A

c) To exit insert mode, and return to the default mode:

ESC

<strong>EXITING VIM</strong>

a) To quit, discarding any changes you might have made (before press ESC):

:q!   

b) To quit, saving any changes you've made(before press ESC):

:wq!

<strong>NAVIGATING THE BAR</strong>

a) To move to line 285 (before press ESC):

:285

b) To search for the word return(before press ESC):

:return

<strong>CUT COPY PASTE </strong>

a) To copy the current selection into the buffer (think of it as a clipboard):

y

b) To cut the current selection:

d

c) To copy the current line into the buffer:

yy

d) To copy 3 lines including the current line into the buffer:

3yy

e) To cut the current line and place it into the buffer:

dd

f) To cut 5 lines including the current line:

5dd

<strong>UNDO AND REDO</strong>

a) To undo the last change:

u

b) To redo the last change you just undid:

CTRL + R

<strong> SYNTAX HIGHLIGHTING AND INDENTATION</strong>

a) Turn on syntax highlighting:

:syntax on

b) Enable automatic indentation:

:set autoindent

or

:gg=G

<strong>WORKING WITH MULTIPLE FILES</strong>

a) To open new tab of terminal

CTRL+SHIFT+T

b) To open server.py in a new tab:

:tabe server.py

c) To move to the next tab on the right:

:tabn

e) To move to the previous tab on the left:

:tabp

<strong>SPLIT VIEW</strong>

a) To open templates/base.html in a vertical split screen:

:vs templates/base.html

b) To open shared.js in a horizontal split screen:

:sp shared.js

c) To move between split screens:

CTRL + W + ARROW KEYS






















