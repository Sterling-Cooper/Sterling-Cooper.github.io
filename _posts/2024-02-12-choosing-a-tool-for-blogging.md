---
layout: post
title: Choosing a Tool for Blogging
tags: github-pages jekyll
---

Choosing the medium for my reflective blog became an unexpectedly fun exercise and an interesting subject for my first post! What follows are some thoughts on the key features of my blogging tool of choice and what I learned from the activity. This post is not an exhaustive technical guide, but I discuss the practical challenges I encountered and link to more thorough documentation throughout the article.

## Picking a Host

At first glance, potential hosts like WordPress and Google Sites seem like good options for the reflective learning assignment. However, I also feel like I will never use either of these platforms beyond the completion of this assignment. I look a little further afield and, in doing so, remember [**GitHub Pages**](https://pages.github.com/):

> “GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process, and publishes a website” (About GitHub Pages n.d.).

This immediately appeals to me because I’m familiar with GitHub [&#185;](#footnotes), Markdown [&#178;](#footnotes), and I have a longstanding wish to learn more about docs-as-code [&#179;](#footnotes). GitHub Pages presents an opportunity to dabble with all three. Intrigued, I dip my toe in the water and follow the five-step introduction on [pages.github.com](https://pages.github.com/). A couple of minutes later, I have my very own website!

##### Figure 1: The Hello World stub index page:
![PNG image illustrating the Hello World stub index page](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-hello.png?raw=true)

## Feature #1: Themes

Encouraged, I venture a little further down the rabbit hole. The next item on my to-do list is to write out a full list of requirements for the site. Of course, I completely ignore this step and start giddily playing with the array of pre-built [themes](https://pages.github.com/themes/).

##### Figure 2: The pre-packaged themes for GitHub Pages:
![GIF image illustrating the pre-packaged themes for GitHub Pages](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-theme.gif?raw=true)

Mistake number one is spending far too long on this stage. The lure of unconventional colour schemes is strong! Eventually, the lectures on accessibility, usability, layout, colour, and text win out, and I settle on [Minima](https://github.com/jekyll/minima). As the name suggests, it has a simple, clean, and familiar layout that is in keeping with other popular technical writing blogs. 

## Feature #2: Simplicity

I learn that each of these themes is powered by [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll), a simple, blog-aware, static site generator (Jekyll n.d.). Simplicity is the key term here. Tom Preston-Werner (2008) created Jekyll to keep the complexity of blogging to a minimum. Jekyll takes content written in Markdown and mixes in any user-defined configuration settings to generate a static website, ready to be served. GitHub Pages serves the website directly from my GitHub repository, so I don’t have to deal with hosting.

To get this far, I only need a page for my "Hello World" markdown (`index.md`) and my own configuration file (`_config.yml`). That’s an excellent start, but it’s not much of a blog without posts!

## Feature #3: Posts

At this point, it becomes clear that blogging is not a feature of Jekyll—it’s baked into it. All I need to do to post my first blog is create a directory called `_posts` and add a new file called `2024-02-12-choosing-a-tool-for-blogging.md`. This filename format is essential for Jekyll to recognise the file as a post. There are more details [here](https://jekyllrb.com/docs/posts/), but this is what it looks like:

##### Figure 3: Blog root directory containing initial post:
```
├── _posts
    └── 2024-02-12-choosing-a-tool-for-blogging.md
├── _config.yml
├── index.md
```

## Feature #4: Comments

I notice that commenting on posts is not supported out of the box. Nor is it immediately apparent to me how to allow readers to add a comment under each article. This is potentially a dealbreaker. But, if I’m honest, I really want this to work! By now, I’ve read enough about Jekyll and GitHub Pages to feel like whatever I learn in this exercise will be helpful in the future. So, I decide to spend some time investigating my options. A little web crawling leads me to [this useful post](https://webapps.stackexchange.com/questions/165528/how-to-add-comments-in-blog-posts-on-github-pages-websites) and an open-source tool called [utterances](https://utteranc.es/). With a little trial and error, I learn that I need to add the following piece of code to each post (see [`_includes/utterances.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_includes/utterances.html)):

##### Figure 4: HTML snippet to enable comments using utterances:
```
<script src="https://utteranc.es/client.js"
        repo="Sterling-Cooper/sterling-cooper.github.io"
        issue-term="title"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
```

The inclusion of utterances allows you, dear reader, to leave a comment on each of my blog posts (with the small caveat that you must already be logged in to [GitHub](https://github.com/)). The comments appear as [issues](https://github.com/features/issues) in the GitHub repository. As the owner, I’m able to delete any issues. This effectively allows me to moderate the discussion, which I see as a bonus feature. 

##### Figure 5: How utterances comments can be managed as GitHub issues:
![GIF image illustrating how utterances comments can be managed as GitHub issues](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-comments.gif?raw=true)

## Feature #5: Header Links

Within the blog, I should be able to build up a list of links to other blogs and websites on relevant topics. I experiment with many layouts and various table positions. Each iteration seems to conflict with one of Kimball and Hawkins’ (2008) principles of design, particularly alignment and enclosure. Returning to the theme configuration in `_config.yml`, I find a setting to add a page to the permanent header (`header_pages`). This allows me to create a new page for the list of blogs (see [`follow.md`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/follow.md)) and link it in the header. This creates separation between "Blogs I Follow" and regular blog posts, while maintaining discoverability.

##### Figure 6: Adding the “Blogs I Follow” page:
![PNG image illustrating the addition of the blogs I follow page](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-following.png?raw=true)

## Feature #6: Tags

> _“Assumptions are dangerous things to make, and like all dangerous things to make, bombs, for instance, or strawberry shortcake, if you make even the tiniest mistake you can find yourself in terrible trouble.”_ – Lemony Snicket (Handler 2000)

Up to this point, I assume that adding categories or tags to organise blog posts will be trivial. I am so convinced of this assumption that I leave the task to the end. A failed attempt to simply “enable” tags is followed by an increasingly panicked web search. Eventually, I accept that GitHub Pages does not support tags. I have made mistake number two. The next ten minutes are spent calculating how many hours I’ve wasted. The blood only starts to return to my face when I discover a fantastic post on [implementing Jekyll tags on GitHub Pages](https://tainenko.github.io/jekyll-tag-on-github-pages/). From this article, I learn that a two-step process can resolve my problem. Step one is to add tags to each post’s “front matter”. Front matter is a way to set variables for each page (Deployment n.d.).

##### Figure 7: Example front matter:
```
---
layout: post
title: Choosing a Tool for Blogging
tags: github-pages
--- 
```

Step two is to collect the tags I’ve defined. I must do this by editing the HyperText Markup Language (HTML) source of the Minima theme. Here is where my coding rustiness shows. I make numerous clumsy attempts to edit the `<head>` element directly, each time breaking the site in strange and exciting ways. Eventually, I stumble upon a sequence of events that doesn’t break horrifically. A moment of smug satisfaction is interrupted when I remember I must explain what I’ve done. Which I can’t do.

As I attempt to articulate how this works, the sequence of events starts to make sense. All of the tags on my site must be collected in a list called `site.tags` (see [`_includes/collect-tags.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_includes/collect-tags.html)). The order of events is essential. I need to collect the tags before using them, so collection needs to happen early in the page construction. I re-read the [Minima help file](https://github.com/jekyll/minima) and discover the theme supports a `custom-head.html` option for precisely this type of scenario. By calling `collect-tags` from my own implementation of [`custom-head.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_includes/custom-head.html), the tag collection is neatly added to the `<head>` HTML element for each page and ensures the correct order of events. Reflective writing—it works!

##### Figure 8: Illustration of tags usage in GitHub Pages:
![GIF image illustrating the presentation of blog tags](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-tags.gif?raw=true)

## Conclusions

Mistakes one and two notwithstanding, this was actually quite a fun exercise. It was great to dust off the coding side of my brain and try to solve a few problems! I spent more time on the setup than I originally planned to, but I felt like I was learning things that will be useful to me in the future.

The most striking part of the exercise is how the act of writing forced me to grapple with the subject matter more deeply. There’s a version of this story where I cobble some pieces of code together and the site works just like it does now. But, sitting down to explain the blog’s features helped me to solidify my thoughts and ultimately led me to understand each element much better than I would have otherwise.

My second big takeaway is to always stick to the assignment brief. While the motivation for choosing this path was to explore some new aspects of documentation technology, I made a mistake in getting too sidetracked by non-essential features. Ensuring the core requirements were in place should have been my top priority.

GitHub Pages and Jekyll are powerful blogging tools, and an energetic community has developed around them. Since writing this, I’ve noticed some of their calling cards in other blogs, notably [in the code for https://idratherbewriting.com/](https://github.com/tomjoht/tomjoht.github.io).

The Continuous Integration (CI) [&#8308;](#footnotes) aspect of building GitHub Pages is fascinating, and I’ve only scratched the surface. I have a lot of experience with CI for software development and there's a lot of overlap with the docs-as-code mindset. This is something I am keen to build on beyond this assignment!

## Footnotes

&#185; GitHub is a popular code-sharing and collaboration service owned by Microsoft (Lardinois and Lunden 2018).

&#178; Markdown is a text-to-HTML conversion tool for web writers. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it has been marked up with tags or formatting instructions (Gruber 2004). 

&#179; Docs-as-code is a way to integrate development and documentation teams and produce high-quality documentation for software products (Gentle 2022).

&#8308; Continuous Integration is a software development practice where team member merges their changes into a codebase together, and all of these merges are verified by an automated build (including test) to detect integration errors as quickly as possible (Fowler 2004).

## References

_About GitHub Pages_ (n.d.) docs.github.com, available:
[https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages) [accessed 12 Feb 2024].

_Deployment_ (n.d.) jekyllrb.com, available:
[https://jekyllrb.com/docs/front-matter/](https://jekyllrb.com/docs/front-matter/) [accessed 12 Feb 2024].

Fowler, M. (2004) _Continuous Integration_, martinfowler.com, [https://martinfowler.com/articles/continuousIntegration.html](https://martinfowler.com/articles/continuousIntegration.html) [accessed 12 Feb 2024].

Gentle, A. (2022) _Docs Like Code: Collaborate and Automate to Improve Technical Documentation_, 3rd ed., Austin: Lulu.

Gruber, J. (2004) _Markdown_, Daring Fireball, available: [https://daringfireball.net/projects/markdown/](https://daringfireball.net/projects/markdown/) [accessed 12 Feb 2024].

_Jekyll_ (n.d.) github.com, available: [https://github.com/jekyll/jekyll](https://github.com/jekyll/jekyll) [accessed 12 Feb 2024].

Handler, D. (2000) _The Austere Academy_, New York: HarperCollins.

Kimball, M.A. and Hawkins, A.R. (2008) _Document Design: A Guide for Technical Communicators_, Boston: Bedford/St. Martin’s.

Lardinois, F. and Lunden, I. (2018) _Microsoft has acquired GitHub for $7.5B in stock_, TechCrunch, available: [https://techcrunch.com/2018/06/04/microsoft-has-acquired-github-for-7-5b-in-microsoft-stock/](https://techcrunch.com/2018/06/04/microsoft-has-acquired-github-for-7-5b-in-microsoft-stock/) [accessed 12 Feb 2024].

Preston-Werner, T. (2008) _Blogging Like a Hacker_, tom.preston-werner.com, available: [https://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html](https://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html) [accessed 12 Feb 2024].
