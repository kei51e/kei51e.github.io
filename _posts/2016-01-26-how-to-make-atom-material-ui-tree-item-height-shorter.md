---
layout: post
title: How to make Atom Material UI tree item height shorter
---

I have been using [Atom Material UI](https://atom.io/themes/atom-material-ui) and 
[Atom Material Syntax](https://atom.io/themes/atom-material-syntax)
for a week, I really like it so far! 


The only thing I don't like is that it is too spacious, especially around the tree on left hand side. 

![original](/public/images/atom-material-tree1.png)

I want to make it more compact to show more info on my 13-inch MacBook Pro's screen. 
So here what I did was to choose `Open Your Stylesheet` from `Atom` menu and add following couple of lines in there.

```css
.tree-view .list-group li:not(.list-nested-item), .tree-view .list-tree li:not(.list-nested-item), .tree-view .list-group li.list-nested-item > .list-item, .tree-view .list-tree li.list-nested-item > .list-item {
    line-height: 22px;
    height: 22px;
}
.tree-view .list-group li::before, .tree-view .list-tree li::before {
    line-height: 22px;
    height: 22px;
}

``` 

Here's the result. Yeah, that's what I want! :) 

![modified](/public/images/atom-material-tree2.png)

Hope this helps!
