---
layout: post
title: Choosing a Tool for Blogging
tags: github-pages jekyll
---

Choosing the medium for my reflective blog became an unexpectedly fun exercise and an interesting subject for my first post! What follows are some thoughts on how the prototype version of the blog evolved and what I learned from the activity. This post is not an exhaustive technical guide, but I discuss some of the practical challenges I encountered and link to more thorough documentation throughout the article.

## Picking a Host

At first glance, potential hosts like WordPress and Google Sites fulfilled all the requirements. However, I also had a feeling that I would never use either of these platforms beyond the completion of the assignment. I decided to look a little further afield and in doing so remembered **GitHub Pages**:

> "GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process, and publishes a website" (About GitHub Pages n.d.).

This immediately appealed to me because I’m familiar with GitHub [&#185;](#footnotes), Markdown [&#178;](#footnotes), and I have a longstanding wish to learn more about the docs-as-code [&#179;](#footnotes) mindset. GitHub Pages presented an opportunity to dabble with all three. Intrigued, I decided to dip my toe in the water and follow the five-step introduction on [pages.github.com](https://pages.github.com/). A couple of minutes later, I had my very own website!

![PNG image illustrating the Hello World stub index page](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-hello.png?raw=true)

## Selecting a Theme

Encouraged, I ventured a little further down the rabbit hole. The next item on my to-do list was to write out a full list of requirements for the site. Of course, I completely ignored this step and started giddily playing with the array of pre-built [themes](https://pages.github.com/themes/).

![GIF image illustrating the pre-packaged themes for GitHub Pages](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-theme.gif?raw=true)

An unspecified amount of time disappeared before I settled on [Minima](https://github.com/jekyll/minima). As the name suggests, it has a simple, clean, and familiar layout in keeping with other popular technical writing blogs. 

## Building with Jekyll

Each of these themes is powered by [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll), a simple, blog-aware, static site generator (Jekyll n.d.). Simplicity is the key term here. Tom Preston-Werner (2008) created Jekyll to keep the complexity of blogging to a minimum. Jekyll takes content written in Markdown and mixes in any user-defined configuration settings to generate a complete static website, ready to be served. GitHub Pages serves the website directly from my GitHub repository so I don’t have to deal with hosting.

To get this far, I only needed a page for my "Hello World" markdown (`index.md`) and my own configuration file (`_config.yml`).

##### Blog root directory:
```
├── _config.yml
├── index.md
```

Now, about those requirements! By setting my repository to be “public”, the website is viewable on the open internet. And the `index.md` serves as a home page for the blog.

> **&#9745; Requirement:** The blog needs to be accessible to my instructor.

> **&#9745; Requirement:** The blog needs to have a landing page.

That’s a nice start, but it’s not much of a blog without posts!

## Creating a Blog Post

At this point it became clear to me just how much blogging is baked into Jekyll, because all I needed to do to post my first blog was create a directory called `_posts` and add a new file to it called `2024-02-06-choosing-a-tool-for-blogging.md`. This filename format is important for Jekyll to recognise the file as a post. More details [here](https://jekyllrb.com/docs/posts/).

##### Blog root directory:
```
├── _posts
    └── 2024-02-06-choosing-a-tool-for-blogging.md
├── _config.yml
├── index.md
```

## Comments

Next, I noticed that commenting on posts is not supported out-of-the-box. Nor was it immediately apparent to me how to allow readers to add a comment under each article. Some webcrawling led me to [this helpful post](https://webapps.stackexchange.com/questions/165528/how-to-add-comments-in-blog-posts-on-github-pages-websites) and an open-source tool called [utterances](https://utteranc.es/). With a little trial and error, and a **lot** of help from the aforementioned helpful post, I learned that I needed to add a little bit of code to each post (see [`_includes/utterances.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_includes/utterances.html)):
```
<script src="https://utteranc.es/client.js"
        repo="Sterling-Cooper/sterling-cooper.github.io"
        issue-term="title"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
```
Rather than add this block of code to each individual page (and risk forgetting to do so), I wanted to enable these comments on all blog posts. The Minima theme's default scaffolding is specified in the [`_layouts` directory](https://github.com/jekyll/minima#layouts). By creating my own version of `post.html` in `_layouts`, I was able to define a default arrangement for each post that includes this code.

##### Blog root directory:
```
├── _includes
    └── utterances.html
├── _layouts
    └── post.html
├── _posts
    └── 2024-02-06-choosing-a-tool-for-blogging.md
├── _config.yml
├── index.md
```

This allows the user to leave a comment on each post, with the small caveat that they must already logged be into GitHub. The comments appear as issues in the GitHub repository. The owner is able to delete any issues, effectively allowing me to moderate the discussion, which I see as a plus. 

![GIF image illustrating how utterances comments can be managed as GitHub issues](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-comments.gif?raw=true)

> **&#9745; Requirement:** One of the characteristics of a blog is that readers can comment on blog entries.

## Blogs I follow

Within the blog, I should be able to build up a list of links to other blogs and websites on relevant topics. I experimented with adding this list as its own blog post, and alternatively as a table in the landing page, but neither result felt natural. Going back to the theme configuration in `_config.yml`, I found a setting to add a page to the permanent header (`header_pages`). Creating a new page for the list of blogs (see [`follow.md`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/follow.md)) and linking it in the header gives the list its own space and keeps it discoverable.

![PNG image illustrating the addition of the blogs I follow page](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-following.png?raw=true)

##### Blog root directory:
```
├── _includes
    └── utterances.html
├── _layouts
    └── post.html
├── _posts
    └── 2024-02-06-choosing-a-tool-for-blogging.md
├── _config.yml
├── index.md
├── follow.md
```

## Tags and Regrets

> _“Assumptions are dangerous things to make, and like all dangerous things to make, bombs, for instance, or strawberry shortcake, if you make even the tiniest mistake you can find yourself in terrible trouble.”_ – Lemony Snicket (Handler 2000)

Up to this point I assumed that adding categories or tags to organise blog posts would be trivial. A failed attempt to simply "enable" tags was followed by an increasingly panicked websearch, and eventually the inescapable conclusion that tags are not supported by GitHub Pages. The blood only started to return to my face when I discovered a wonderful post on [how to implement Jekyll tags on GitHub Pages](https://tainenko.github.io/jekyll-tag-on-github-pages/). From this I learned that I needed to add the tags for each blog to the post's "front matter". Front matter is a way to set variables for each page (Deployment n.d.).

##### Example front matter:
```
---
layout: post
title: Choosing a Tool for Blogging
tags: github-pages
--- 
```

All of the tags in my site must be collected into a list called `site.tags` (see [`_includes/collect-tags.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_includes/collect-tags.html)). The order of events is important. The tags must be collected before they can be used, so this needs to happen early in the page construction. By calling `collect-tags` from my own [`custom-head.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_includes/custom-head.html), this collection is neatly added to the `<head>` HTML element for each page and ensures the correct order of events. This was where my coding rustiness really showed. I made numerous clumsy attempts to edit `<head>` directly, occasionally breaking the site in strange and exciting ways. It was only through the act of writing this blog post that I really came to understand the correct sequence of events. It also forced me to re-read the [Minima help file](https://github.com/jekyll/minima) where I learned about the `custom-head.html` option. Reflective writing, it works!

Now that the list of tags is known, they can be displayed at the bottom of each post by once again editing the default post layout in [`_layouts/post.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_layouts/post.html). I chose to enclose the tags between two square brackets (`[ tag ]`) for clarity. Each tag needs a corresponding markdown file, and these are collected in the `tag` directory.

When a user clicks the link on a tag, they will expect a different layout to a regular post. [`_layouts/tag-page.html`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_layouts/tag-page.html) describes a clean page with a list of tagged blog posts, without the extra bells and whistles of a regular blog post. This is essentially a form of "Blog Archive", and its content is defined in [`archive.md`](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/archive.md).

![GIF image illustrating the presentation of blog tags](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/pages-tags.gif?raw=true)

> **&#9745; Requirement:** Include a Categories or Tags widget to organise blog posts.

The final root directory for the prototype blog looks like this:

##### Blog root directory:
```
├── _includes
    └── collect-tags.html
    └── custom-head.html
    └── utterances.html
├── _layouts
    └── post.html
    └── tag-page.html
├── _posts
    └── 2024-02-06-choosing-a-tool-for-blogging.md
├── css
    └── override.css
├── tag
├── _config.yml
├── archive.md
├── follow.md
├── index.md
```

## Conclusions

Final scare notwithstanding, this was actually quite a fun exercise. In an existence increasingly dominated by meetings, it was great to dust off the coding side of my brain and try to solve a few problems!

The most striking part for me was how the act of writing forced me to grapple with the subject matter more deeply. There's a version of this story where I cobble some pieces of code together and the site works about the same as it does now. But sitting down to explain the blog's evolution forced me to solidify my thoughts and ultimately led me to understand each element much better than I would have otherwise.

My second big takeaway is to always stick to the assignment brief. While the motivation for choosing this path was to explore some new aspects of documentation, I made a mistake in getting too sidetracked by non-essential features. Making sure the core requirements of tags and comments were in place should have been my top priority.

GitHub Pages and Jekyll are powerful blogging tools and a really interesting community has developed around them. Since writing this I've noticed some of the calling cards in other blogs, notably [in the code for https://idratherbewriting.com/](https://github.com/tomjoht/tomjoht.github.io).

The Continuous Integration [&#8308;](#footnotes)  aspect of building GitHub Pages is really interesting, and I've only just scratched the surface. This is definitely something I will keep building on beyond this assignment!

## Footnotes

&#185; GitHub is a popular code sharing and collaboration service owned by Microsoft (Lardinois and Lunden 2018).

&#178; Markdown is a text-to-HTML conversion tool for web writers. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it has been marked up with tags or formatting instructions (Gruber 2004). 

&#179; Docs-as-code is a way to integrate development and documentation teams and produce high-quality documentation for software products (Gentle 2022).

&#8308; Continuous Integration is a software development practice where each member of a team merges their changes into a codebase together, and all of these merges are verified by an automated build (including test) to detect integration errors as quickly as possible (Fowler 2004).

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

Lardinois, F. and Lunden, I. (2018) _Microsoft has acquired GitHub for $7.5B in stock_, TechCrunch, available: [https://techcrunch.com/2018/06/04/microsoft-has-acquired-github-for-7-5b-in-microsoft-stock/](https://techcrunch.com/2018/06/04/microsoft-has-acquired-github-for-7-5b-in-microsoft-stock/) [accessed 12 Feb 2024].

Preston-Werner, T. (2008) _Blogging Like a Hacker_, tom.preston-werner.com, available: [https://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html](https://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html) [accessed 12 Feb 2024].
