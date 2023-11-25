Source repository for my portfolio/blog.

# Objectives
Primary objectives for this project are to skill up and get used to working
with web development tools like JS, and to have some place to showcase my other
little projects.

# Overview/Toolkit
This blog is built with Zola, a static site generator written in Rust, mainly because
I like Rust, and am more comfortable with using it. It the Tera template engine,
which is similar to Jinja2, Django, Liquid, etc.

Deployment is done using the [zola-deploy-action](https://github.com/shalzz/zola-deploy-action) GitHub Action.

The theme uses [anemone](https://github.com/Speyll/anemone) as a base, with some
modifications to account for my needs and a bug fix or two:
* Added a "projects" taxonomy
* Fixed a bug that causes the default theme to be set incorrectly
