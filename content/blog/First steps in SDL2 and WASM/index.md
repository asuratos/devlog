+++
title = "A Foray into SDL2 and WASM in Rust #1"
date = 2023-11-26
[taxonomies]
  tags = ["rust", "webassembly", "game development"]
+++

## Day 1

### SDL2-Rust: Getting things installed

The most difficult part of this was installing SDL properly on Windows.
I had to look through quite a few of the google results before I found a tutorial I could use, and now writing this I can't find it again!
### Gray screen of life
Working with the SDL2 library in Rust was surprisingly not too complicated.
I guess it just makes sense to me to think about the flow of a program.
Also it probably helps that I've tried and failed to build several games at this point.
One of these days, I'm going to finish one.

{{ img(id="hi_earth.png", alt="I can make a blank screen, yay") }}

For now, I got a window to pop up. I can set its size, title, and the single color that will make up its entire space. I can also quit out by hitting Esc. It's not much, but it's a start.

## Webassembly

Once again, getting the required libraries and their dependencies made this a nightmare. 
By the time I was able to even attempt compiling to WASM, it was already late and my brain wasn't working at full power anymore.

...and that's it for now. Baby steps. Next one is trying to get an SDL2 window to compile into WASM, then maybe I can have something more interesting to embed onto these blog posts.