# Syntax Highlighting
A syntax highlighter... Currently only for HTML and JavaScript

## What Does It Do?
This function will take two parameters as input
  1. The text that you want to have syntax highlighting in an HTML page
  2. The language that the code is written in (currently only works for HTML and JavaScript)

## How It Does It Do It?
The way this function works is by using a _ton_ of `String.replace(...)` to wrap certain text bits into HTML span tags with classes. Those classes are then referenced in a CSS file and the styling is applied.

## How Does It Look?
Below is an image of what it would look like (with additional styling to the `<pre>` and `<div>` before it:  
![Syntax Highlighter Example](https://raw.githubusercontent.com/JacobHornbeck/JacobHornbeck.github.io/master/wdd330/images/Untitled.png)

The styling you see there is almost an exact replica of the VSCode Light+ theme (at least for the JavaScript highlighting), if you want the same styling code, here you go:
```css
pre .varName { color: #0471C1; }
pre .reservedWord { color: #0306FF; }
pre > .number { color: #098658; }
pre .functionName, pre .method { color: #795E26; }
pre .text { color: #A31515; }
pre .comment, pre .comment * { color: #398310; }
pre .parameter, pre .object { color: #021180; }
pre .return { color: #dd00dd; }
pre .normal { color: black; }

pre .html-tag { color: grey; }
pre .html-tag > .html-attribute { font-style: italic; color: orangered; }
pre .html-tag > .html-text { color: royalblue; }
```

If you don't want this styling, just make your own, just use the same classes and structure that I have there (not the one-line thing, but the way I am selecting the elements... it won't style correctly all the time if you don't do it like that).

## What's Next?
For now, I am happy with what it is... someday I may start adding more and more languages that it will support, but in the near future I will probably add CSS and maybe Python...
