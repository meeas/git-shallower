# git-shallower

A simple tool to download (or re-download) the latest version of a git repository without the git history.

This takes up less space then `git clone --depth 1 <URL>` since git-shallower does not keep a comressed copy of HEAD in `.git/`.  This can be a big space saving feature for larger repositories when you just want a downloaded copy.

## Installation

Since this is a BASH script, you will need to be running BASH.  ;-)

Download the git-shallower script and move it to a directory in your path.  For instance, on linux, you could:

```
wget https://raw.githubusercontent.com/meeas/git-shallower/master/git-shallower
chmod +x git-shallower
sudo mv git-shallower /usr/local/bin/
```

## Usage

`git shallower <URL>`

Download the git repository from `<URL>` and place it in a new directory named after the project.
  
`git shallower <URL> <DIR>`

Download the git repository from `<URL>` and place it in the `<DIR>` directory.
  
`git shallower`

This will re-download the latest version of the git respository that you are in.
