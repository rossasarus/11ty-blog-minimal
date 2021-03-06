---
title: Are templates bad? 
date: 2020-04-28
author: RossD
summary: 
tags: 
- development
- efficiency
---
I'm a person who is continuously trying to find more efficient ways to write code. I'm also not a person who is great at remembering all the syntax of a given language, so I often build templates. At work we have some boilerplate functions that read and write values to the redux global state, and **writing it all from scratch in addition to the react function boilerplate every time is wildly inefficient**. 

<!-- excerpt -->
{% asset_img 'react_template.png' 'example component template' %}

An example template would be a skeleton functional component that has all of the core syntax (gif below). Generally the template is defined in my ide and uses a shortcut to paste a bunch of code with a few keystrokes. There are also a few [vscode](https://marketplace.visualstudio.com/items?itemName=xabikos.ReactSnippets) [plugins](https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-react-snippet) that offer the same functionality. Making it myself means that it contains exactly what I want and also it usually has a shortcut that's easier for me to remember.

{% asset_img 'react_component_template.gif' 'example component template in action' %}

The speed benefit is super nice, and it means I can start right on the meat of the component. I hope there isn't anyone out there that actually believes they are more productive typing `import React from 'react'` than using a shortcut. 

The reason why this isn't 100% win is because using the template means that I generally don't fully internalize the syntax. This is the kind of thing that looks bad in an interview, but I'm not totally sold that committing all of that to memory actually makes a person a better coder.

I also extrapolate this out to things beyond react components and vscode - I often build zsh shortcuts to automate repetitive multi-line commands, or even to shorten long commands into shorter abbreviations (i.e. `bundle exec rspec` -> `ber`). I do sometimes have to look the commands up in my .zsh file, but at least it's internally documented!

Here are example zsh shortcuts
```
alias berf="bundle exec rspec --format progress"
alias ber="bundle exec rspec"
alias codebase="cd ~/Codebase"
alias yl="yarn lint && /usr/bin/osascript -e \"display dialog \"sourceYarn Lint is finished.\"\""
```

One common argument against this kind of workplace specialization generally looks like 
> # **"But how are you going to be able to do this on someone else's machine?!"** 

I never gave those types of reactions much validity before covid. Especially now that the world is remote this reasoning has less reason behind it - I don't plan on touching my coworker's laptops within the next year, and even when we are fully back to work (whatever that means) 
> # **I would rather be slow 1% of the time if it allows me to be fast the other 99%.**

# Wrapping up
So I've explained my rationale. I think using templates is a good way to get down to the 'important work' faster. In my mind 'important work' is anything that can't be done by a single command. In fact - I'm thinking I need to make this go a little further. A vscode shortcut to paste in some code is nice, but that still requires you to have created the folder and the js file. It sure would be nicer to make a zsh script that builds the folder, the js and the css file all together! Hmmm... I like that - I'll get working on building it.
