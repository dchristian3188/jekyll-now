---
layout: post
title: Tools Module Authors Should Leverage
---

Writing a PowerShell module is hard.
A lot harder than it used to be.
Honestly it's your fault.
Not just you, but the whole PowerShell community.
Apparently we're a mature language now and everybody is demanding more.
I mean I was just starting to accept that fact that I have to include Pester tests, but now I need documentation too?
What else does it take to write a professional quality module these days?

**The Good Stuff:**
The skills you should be investing in to take your modules to the next level.

<!-- more -->

# Pester

[Pester](https://github.com/pester/Pester) is the testing framework chosen not only by the community but the PowerShell team.
In fact, Pester's adoption has been so wide spread, it was the first open source project to actually ship with Windows.
Pester allows you to define scriptblocks that ensure your code is working as expected.
The idea is every time you make a change, you run the Pester tests.
When you find new bugs, you create tests to ensure your code fixes worked.
Pester does have its own DSL, but still feels and reads much like PowerShell.
# Git

[Git](https://github.com/) is an open source version control system.
Some of the biggest names in the industry use Git, such as Google, Facebook, Microsoft and Netflix.
If you're not using source control, you should be.
It's an absolute must if you're working on large projects, coding on multiple machines, or developing in a group.
Git provides all the features you expect from source control and has a healthy ecosystem of apps.
This comes with the cost of introducing a whole suite of utilities and new commands to learn.
Unfortunately, since its cross platform and been around forever, it feels nothing like PowerShell syntax.

# Invoke-Build

[Invoke-Build](https://github.com/nightroman/Invoke-Build) is a powerful, build automation system written in PowerShell created by [Roman Kuzmin.](https://github.com/nightroman)
As of late it has been generally accepted by the community as the go to tool, replacing psake.
Using ```Invoke-Build``` gives us a lot of neat features including: task groups,  incremental and parallel builds and an easy way to define conditions or dependencies.
Using ```Invoke-Build``` is straight forward, every task is essentially a script block and looks close to vanilla PowerShell.

# Plaster

[Plaster](https://github.com/powershell/plaster) is a PowerShell scaffolding module and a must for module creators.
Think of the new project wizard from Visual Studio, but written in PowerShell where you control all the options.
Plaster's wizard process is all driven by an XML manifest, with a little bit of PowerShell sprinkled throughout.
It also provides a custom syntax to template files based on PowerShell.
While this does present a learning curve, the investment is well worth it to avoid the duplication of work.

# PSGraph

[PSGraph](https://github.com/KevinMarquette/PSGraph) is a wrapper for Graphiz created by [Kevin Marquette.](https://kevinmarquette.github.io/)
If you haven't seen Graphiz before, it's an open source library for creating diagrams and flow charts.
Thanks to [Kevin's](https://twitter.com/kevinmarquette) module, creating graphs in PowerShell is a breeze.
For example, a new addition to all my modules, is a Graphiz diagram that'll detail how the functions in the module call each other.
Most of the time, these visualizations can provide powerful insights (the rest are just cool spaghetti monsters).
PSGraph does have its own DSL but follows PowerShell very closely.

# PlatyPS

Sorry but you need to document your code.
I know it sucks, but until we all learn to read minds it's a necessity.
The goal of [PlatyPS](https://github.com/PowerShell/platyPS) is to make this process a little less painful.
PlatyPS does this by letting you define your cmdlet based help in Markdown.
To get you started, PlatyPS will inspect your module and create the help for what it can.
This includes the skeleton of the help document for each function, information about the parameters and a place to put the examples.
You still have to do the hard part and write them, but now you have an easier way to do it.
Once done with the Markdown, PlatyPS will package all the files up into an xml document to distribute with the module.

# Wrapping UP

So what did I miss?
Are there any new projects that every module author should be using?
Drop a comment and let me know what's making your writing a little bit easier.