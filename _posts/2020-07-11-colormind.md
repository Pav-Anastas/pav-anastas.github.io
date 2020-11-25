---
title: "Using Colormind to customise a website's theme"
categories:
- Web Development
- Style Sheet Language
- Design
tags:
- scss
---

### Aesthetics are important

I recently wanted a change on the feel of my website as the skins (or themes) that came with the toolbox of the template I used [(Basically-basic)](https://github.com/mmistakes/jekyll-theme-basically-basic) didn't transmit the right message. To do so successfully I broke down the task in two distinct steps. Deciding which colours to use, and applying them on the website. And thus an hour long project began!

Step 1: Deciding on the Colour pallet

Depending on how much you want to spend this step can change in complexity. If you desire to use this as a chance for growth and personal development deciding on a colour pallet is an open invitation to dwell into the depths of [colour theory](https://en.wikipedia.org/wiki/Color_theory) and the visual arts. But, if you paid attention to the title you might guess that there are tools out there that offer an easy way out, one of them being [Colormind.io](http://colormind.io/).



Step 2: What is Colormind and how I use it.

[Colormind](http://colormind.io/) is a colour scheme generator that uses [Deep learning](https://en.wikipedia.org/wiki/Deep_learning) to "learn" colour styles from external references such as photographs, movies and popular art.
> Colormind.io

In essence the algorithm collects colour schemes from lots of sources and recognises the specific colour structure of it's reference. Afterwards it creates a massive library of different pallets that are ready to be applied. Simple, right?

Well yes, but let's breakdown some of that procedure, starting with _*colour structure*_.

The palette consists of a light color, a dark color, main brand color and two highlight colors. The main color is in the center of the palette and has the largest impact on the overall look.
> Colormind.io

![Screenshot from website's palette](/assets/images/DeYork_Palette.jpg "This website's palette")

Looking at the stylesheet that this website is currently using

```c++
$base-color: #A1B7B5 !default;
$text-color: #6D88A0 !default;
$accent-color: #7DCD85 !default;
$background-color: #F5F7F8 !default;
$code-background-color: #fff !default;
$border-color: rgba($text-color, 0.5) !default;
$overlay-color: #fff !default;  
```
Thus in our case we match
+  base-color: Main brand colour
+  text-color: Dark accent
+  accent-color: Light accent
+  background-color: Light shades
+  code-background-color: Using white for clarity in code blocks
+  border-color: a variety of our selected text colour
+  overlay-color: white again

You can assign variables if they aren’t already assigned by adding the *!default* flag to the end of the value, so using Sass *!default* is like adding an “unless this is already assigned”

For further Stylesheet and Sass information look [Here :)](https://sass-lang.com)
