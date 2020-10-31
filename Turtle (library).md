---
categories: Haskell
...

From time to time I need to automate some work on my machine. Someone other than me is writing the shell-scripts but I feel too uncomfortable writing more than ten lines of Bash. So I am using the [Turtle](https://hackage.haskell.org/package/turtle) library ([/Haskell]()). This one gives me the conciseness of shell scripts but also keeps the types under control.

The package has a pretty nice tutorial and the basic usage of Turtle is simple and fun. There are some quirks: pipe plumbing, text formatting, own regexes ­­­- these features are too opinionated (as the whole library), but overall experience I have is positive.

[Here](https://github.com/astynax/turtle-powered) I have a repo with a set of small turtle-powered tools. All the tools I use on the regular basis.