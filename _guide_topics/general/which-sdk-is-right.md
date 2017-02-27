---
title: Which SDK is right for me?
description: It all depends on what you want to do...
authors: ['Dan Belcher']
author_contacts: ['dan']
apis: ['General']
languages: ['All']
platforms: ['Windows', 'Mac']
categories: ['general']
origin: http://wiki.mcneel.com/developer/scriptspage
order: 4
keywords: ['developer', 'rhino', 'faq']
layout: toc-guide-page
---

**The quick answer:**

- Rhino supports commandline macros to automate very simple repetative tasks. See [Rhino Macro Guide]({{ site.baseurl }}/guides/general/rhino-macro-language) for more details.
- If you are looking to automate repetitive tasks in Rhino, writing a [Python]({{ site.baseurl }}/guides/#rhinopython) script is the way to go.  
- If you need a full-fledged plugin or Grasshopper component, we suggest the [RhinoCommon SDK]({{ site.baseurl }}/guides/rhinocommon/what-is-rhinocommon/). 
- If you are very proficient with C/C++, you should consider the native [C/C++ SDK]({{ site.baseurl }}/guides/cpp" title="C/C++ SDK for Rhino for Windows) (only supported on Rhino for Windows).

## Using Macros

You can create macros in Rhino to automate many tasks, customize your commands, and improve your workflow. Macros are a series of Rhino commands and special characters that feed directly to the Rhino commandline.  There are methods to pause, enter and select in macros in addition to the standard Rhino commands. For more details on working with macros, go to the [Rhino Macro Guide]({{ site.baseurl }}/guides/general/rhino-macro-language)

## What are Scripts?

For more complex tasks, macros are insufficient. They lack the ability to make complex calculations, store and retrieve data and make conditional decisions. For this, one needs a programming language. The simplest and most accessible of these is Python.  Python is interpreted directly from RHin o and does not require any additional compiling tools. When we talk about scripts we are usually referring to functions written with [RhinoScript]({{ site.baseurl }}/guides/rhinoscript) or [Python]({{ site.baseurl }}/guides/#rhinopython).

## What are Plugins?

Plugins are even more sophisticated tools: these are compiled computer programs that can be integrated into Rhino. These can range from simple script-like functions to complex, full blown programs for doing rendering, animation, machining, etc. Plugins require a better understanding of programming, but also can become an intergral part of the Rhino process.  Plugins can constantly watch and react to events in Rhino.  The [RhinoCommon SDK]({{ site.baseurl }}/guides/rhinocommon/what-is-rhinocommon/) is a good example of a plugin toolkit for Rhino.
