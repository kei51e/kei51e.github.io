---
layout: post
title: How to disalbe Remove Trailing Whitespace feature in Atom editor
---

By default, when you save a file on the Atom editor,
Atom kindly removes all the trailing whitespaces in each line.
Sometimes it's really helpful,
but sometimes it's too much because it makes a lot of diffs
especially if you work on something source controlled.


Here's how to disable that feature.

- Open "Preference" from the menu.
- Click "Packages" on the left.
- Type in "whitespace" at "Installed Packages" textbox
- Click "Settings" of the "whitespace" package

![screenshot1](images/atom-trailing-whitespace1.png)


- Uncheck "Remove Trailing Whitespace" checkbox.

![screenshot2](images/atom-trailing-whitespace2.png)


That's it! Hope this helps you.


[[ images/atom-trailing-whitespace2.png | width = 500px ]]
