# Mac's Blog

> A digital garden on networking, self-hosting, cybersecurity, and whatever I'm hacking on at the moment.

This is the source code for my personal blog, powered by [Jekyll](https://jekyllrb.com) and based on the legendary [Huxpro](https://github.com/huxpro/huxpro.github.io) theme. I'm customizing it to better suit my style and projects — including posts on smart home devices, self-hosted infra, and more.

---

## Getting Started

To run the blog locally:

### 1. Install dependencies

You'll need Ruby and Bundler. Once set up:

```bash
bundle install
```

### 2. Serve the site

```bash
bundle exec jekyll serve
```

Visit [http://localhost:4000](http://localhost:4000) to preview it.

---

## Development Notes

- Jekyll templates are mostly located in `_layouts/`, `_includes/`, and `_posts/`
- Syntax highlighting is handled via [Rouge](https://github.com/rouge-ruby/rouge)
- Minimal JS/CSS customization for now — keeping it clean and performant

If you're customizing your own fork, I recommend checking:

- `_config.yml` – core site settings
- `assets/css/style.scss` – styles
- `_includes/sidebar.html` – for social links
- `_includes/header.html` – for nav

---

## Credits

- Theme: [@Huxpro](https://github.com/huxpro/huxpro.github.io)
- Based on: Clean Blog by Blackrock Digital (MIT License)
- License: Apache 2.0

---

## About Me

I'm Mac — currently studying Software Engineering with a minor in Cyber Forensics. I love self-hosting, messing with networks, building smart devices, and tinkering with tech that most people are scared to touch.
```

Let me know if you want me to include badges (like for GitHub Pages status), a lighter version, or a deployment section next!