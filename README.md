CSS-only Animated progress-bar
===
### Animated split progress bar using CSS only, via SCSS

Simple lightweight snippet of code created for a client project. The idea was to create this piece of UI using as little JS as possible, when I realised I could do this completely in CSS, based off CSS Custom Properties containing the percentage values.


Code Style
===

I do a few things differently from the rest of the dev world, so before you :fire: me, let me explain why!

* `__` double underscores within class chains, such as `.parent-component__child-component`. I hate these personally, as underscores prevent you selecting along word boundaries in your IDE. Especially since the double underscores usually sit in the exact spot you *might* need to select on word boundaries in your templates (i.e. the child part of a class chain), to select and edit/replace part of a class name without using your mouse.  I use double dashes or `--` instead. Accomplishes the same separation of concerns as `__`, without impeding your dev workflow.
* Let's also talk about REM units. We all know they're the best units for type, but 1rem = 16px is not a useful conversion *at all*, and most of the workarounds for this that I've seen, frankly, suck. Mixins that convert pixel values in your SASS to arbitrary REM units in the compiled CSS impede dev QA because you're not tweaking the same units in the inspector. The only solution I've seen over the years that makes sense is `body, html { font-size: 62.5%; }`. This converts your REM units to **1rem = 10px**. A great starting point for sensible font size values that are identical in build and QA.


Installation
===
Instructions to work on or compile the SCSS locally.

### Requirements
* NPM
* GULP

### Getting Started
* Run `NPM Install`
* Run `gulp`
* That's it!