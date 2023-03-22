<h1 align="center">
    <a href="https://dev.brucebentley.io/" alt="Bruce Bentley's Development Portfolio">
        <code>dev.brucebentley.io/</code>
    </a>
</h1>

### Showcase Your Software Development Skills

This repository gives you the code you'll need to kickstart a personal website that showcases your work as a software developer. And when you manage the code in a GitHub repository, it will automatically render a webpage with the owner's profile information, including a photo, bio, and repositories.

Your personal website is waiting to be personalized, though. It includes space to highlight your specific areas of interest in software development, like languages or industries. And it's standing by to publish your next great blog post.

It's all possible using the combination of [Jekyll](https://jekyllrb.com/docs/) (for building your website), [GitHub Pages](https://pages.github.com/) (for hosting your website), and [GitHub's API](https://developer.github.com/v3/) (for automatically populating your website with content).

## Installation

### Fork The `github/personal-website` Repo

You'll be making your own copy of the "personal website starter" repository so you have your own project to customize. A "fork" is a copy of a repository. So select "Fork" atop [the `github/personal-website` repository](https://github.com/github/personal-website).

Once you've found a home for your forked repository, it's yours. You're the owner, so you're ready to publish, if you wish.

### Install In Your Local Development Environment

If you want to manage your website in a local web development environment, you'll be using [Ruby](https://jekyllrb.com/docs/installation/).

Once you've found a home for your forked repository, **[clone it](https://help.github.com/articles/cloning-a-repository/)**.

#### Install `Jekyll`

`Jekyll` is a [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems) that can be installed on most systems.

1. Install a full [Ruby development environment](https://jekyllrb.com/docs/installation/)
2. Install `Jekyll` and [bundler](/docs/ruby-101/#bundler) [gems](/docs/ruby-101/#gems)

   ```shell
   $ gem install jekyll bundler
   ```

3. Change into your new directory

   ```shell
   $ cd wansooseo.com
   ```

4. Build the site and make it available on a local server

   ```shell
   $ bundle exec jekyll serve
   ```

5. Now browse to [http://localhost:4000](http://localhost:4000)

### Publish

When you host your personal website's code on GitHub, you get the support of free hosting through GitHub Pages.

**The fastest approach** is to rename your repository `username.github.io`, where `username` is your GitHub username (or organization name). Then, the next time you push any changes to your repository's `master` branch, they'll be accessible on the web at your `username.github.io` address.

**If you want to use a custom domain**, however, you'll want to add it to your repository's "Custom domain" settings on github.com. And then register and/or [configure your domain with a DNS provider](https://help.github.com/articles/quick-start-setting-up-a-custom-domain/).

## Customization

It's your website, and you control the source code. So you can custom everything, if you like. But we've provided a handful of quick customizations for you to consider as you get your website off the ground.

### Quick Configuration Changes

Most customizations can be done in a matter of seconds, by revising your repository's `_config.yml` file. Just remember to restart your local server each time you save new changes so your Jekyll-powered website rebuilds correctly:

1. Shut down your server by entering the keyboard command <kbd>CTRL</kbd>+<kbd>c</kbd>
2. Restart your server: `jekyll serve`

#### Layout

By default, your website will display in a two-column layout on larger-screen devices, with your photo, name, and basic information displayed in a left-aligned "sidebar." But you can quickly switch to a "stacked" single-column layout by changing the line in your `_config.yml` file that reads `layout: sidebar` to `layout: stacked`.

#### Style

By default, your website appears with a "light" white and gray background, with dark text. But you can quickly switch to a "dark" background with white text by changing the line in your `_config.yml` file that reads `style: light` to `style: dark`.

#### Topics

Your website comes pre-configured with three topics (e.g. "Web design" and "Sass") that appear in a section titled "My Interests." These are also stored in your repository's `_config.yml` file, where you can define each topic's name and two other optional details:

- `web_url`: The web address you'd like to your topic to link to (e.g. `https://github.com/topics/sass`).
- `image_url`: The web address of an (ideally square) image that you'd like to appear with your topic.

#### Social Media

Your website supports linking and sharing to social media services you're using, including Behance, Dribbble, Facebook, LinkedIn, Medium, Stack Overflow, Twitter, and YouTube. To identify the services you use:

1. Edit your repository's `_config.yml` file.
2. Edit the `social_media` dictionary line, and represent the services you like in a simple `key: value` form:

```yaml
social_media:
  behance: your_username
  dribbble: your_username  
  facebook: your_username
  hackerrank: your_username
  instagram: your_username
  keybase: your_username
  linkedin: your_username
  medium: your_username
  stackoverflow: your_user_id
  telegram: your_username
  twitter: your_username
  unsplash: your_username
  vk: your_username
  website: http://your_website_url
  youtube: your_username
```

Links to your profile for each of the services you define will appear in the `<header>` of your website, appended to your bio. And if those services support sharing, any blog posts that you publish will include links to share that post using each social media service.

**Note**: This feature is supported by two files in your repository:

- `/_data/social_media.yml`: Defines each of the supported services, including variable name, display name, URL path, and SVG icon.
- `/_includes/social_media_share_url.html`: Outputs the share URL required for any of the supported social media services that support sharing URLs.

If you're interested in adding a social media service that's not already supported in this repo, you can edit these two files to build that support.

## Adding Pages

To **add a page** to your website (e.g. detailed resume):

1. Create a new `.html` or `.md` file at the root of your repository.
2. Give it a filename that you want to be used in the page's URL (e.g. `http://yoursite.dev/filename`).
3. At the start of your file, include the following [front matter](https://jekyllrb.com/docs/front-matter/):

   ```yaml
   ---
   layout: default
   ---
   ```

4. Save.

## Adding Blog Posts

To **add a blog post** to your website:

1. Create a new `.md` file in your repository's `/_posts/` directory.
2. Give it a filename using the following format:

   ```markdown
   YEAR-MONTH-DAY-title.md
   ```

3. At the start of your file, include the following [front matter](https://jekyllrb.com/docs/front-matter/):

   ```yaml
   ---
   title: "The title of my blog post"
   ---
   ```

Your website comes with a placeholder blog post that you can reference. Notably, its [front matter](https://jekyllrb.com/docs/front-matter/) declares `published` as `false`, so that it won't appear on your website.

While you _can_ also define a `layout` in the front matter, your website is pre-configured to assign the `post` layout to all of the posts in your `/_posts/` directory. So you don't have to declare that in your posts, if you don't want to.

Jekyll's conventions for authoring and managing blog posts is very flexible. You can [learn more in Jekyll's documentation for "Posts."](https://jekyllrb.com/docs/posts/)

## Content & Templates

To give you a sound foundation to start your personal website, your repository includes a handful of "includes" -- dynamic `.html` files that are re-used throughout your website. They're all stored in the `/_includes/` directory.

There are the usual suspects, like `header.html` and `footer.html`. But there are few more worth pointing out:

- `interests.html`: A heading and dynamic list of "My Interests," which is populated with the [topics](#topics) you list in your `_config.yml`.
- `masthead.html`: A collection of your avatar, name, bio, and other metadata that's displayed prominently on all your webpages to help identify what the website is about.
- `post-card.html`: A compact, summarized presentation of a blog post, re-used to display a listing of your latest blog posts.
- `projects.html`: A heading and dynamic list of "My Projects," which is populated with a listing of your newest GitHub repositories.
- `repo-card.html`: A compact, summarized presentation of a repository, re-used to display a listing of your GitHub repositories.
- `thoughts.html`: A heading and dynamic list of "My Thoughts," which is populated with a listing of your latest blog posts.
- `topic-card.html`: A compact, summarized presentation of a topic (defined in your `_config.yml`), re-used to display a listing of your interests.

### Layouts

Your repository comes with three layouts:

- **default**: Not used by any of the built-in pages or posts, but useful for any new pages you create.
- **home**: Used by your `index.html` homepage to display listings of your projects, interests, and (optionally) your blog posts.
- **post**: Used by default by the posts in your `/_posts/` directory.

Jekyll's convention for defining layouts is very flexible. You can [learn more about customizing your layouts in the Jekyll "Layouts" docs.](https://jekyllrb.com/docs/layouts/)

## Styles

Your website is pre-configured to use [a very flexible CSS framework called "Primer,"](https://styleguide.github.com/primer/) alongside any custom styles you write in your `/assets/styles.scss` Sass stylesheet. It's currently referenced within your `styles.scss` file, using the CSS import at-rule:

   ```scss
   @import url('https://unpkg.com/primer/build/build.css');
   ```

You are, of course, welcome to remove it or replace it with another framework. Just bear in mind that the HTML that your website came pre-packaged with references multiple Primer "utility classes" to define things like column widths, margins, and background colors.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
