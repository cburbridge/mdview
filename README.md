# mdview

A simple MarkDown text viewer that monitors a markdown file on disk
for changes and displays updates as the file is saved. The markdown is
displayed as an HTML page in a python-gtk based webkit viewer.

### Requirements
The following python dependencies:

- watchdog - for cross-platform monitoring of files for change
(inotify etc)
- webkit - for displaying HTML
- gtk2

These can be installed on Ubunu:
```
sudo easy_install watchdog
sudo apt-get install python-webkit
sudo apt-get install python-gtk2
```

or on Mac OS X (macports):

```
sudo easy_install watchdog
sudo port install py27-gtk
sudo port install py27-webkitgtk
```


To use GitHub markdown:

A markdown processor is also required. I use
[this one](https://gist.github.com/ralph/1300939).

### Usage
./mdview markdownfile.md

### To do
- Syntax colouring / GitHub style sheets
- Support links
- Faster updating (don't use glib idle to avoid thread issue)
- Swap from gtk to Qt (PySide) for native Mac UI
