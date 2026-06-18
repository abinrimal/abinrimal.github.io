# Abin Rimal — Personal Site

## Setup (one time)
1. Create a GitHub repo named `abinrimal.github.io`
2. Push this codebase to the `main` branch
3. In repo Settings → Pages → Source: Deploy from branch → main → / (root)
4. Site goes live at https://abinrimal.github.io in ~2 minutes

## Adding a blog post
1. Create `_posts/YYYY-MM-DD-your-post-slug.md`
2. Add front matter (title, date, categories, tags)
3. Write in Markdown
4. git add, commit, push
5. Done — home page updates automatically

## Enabling comments on blog posts
1. Create a Disqus site and copy your shortname
2. Set `disqus_shortname` in `/home/runner/work/abinrimal.github.io/abinrimal.github.io/_config.yml`
3. Comments render automatically on all posts
4. Add `comments: false` in a post front matter to disable comments for that post
