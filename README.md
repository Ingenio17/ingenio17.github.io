# ingenio17.github.io

Personal site and digital garden of Saumya Shah, built with [Quartz v4](https://quartz.jzhao.xyz/)
and published at <https://ingenio17.github.io/>.

Quartz version: v4 branch at commit `d25a6ea` (v4.5.2 plus 46 commits, 2026-04-20).

## Writing

All content is Markdown under `content/`:

- `content/index.md` is the homepage, `content/about.md` the About page.
- Posts go in `content/posts/`, notes in `content/notes/` (any folder works).
- Front matter at the top of a file:

  ```yaml
  ---
  title: My post
  date: 2026-10-07
  tags: [robotics]
  draft: true # optional: drafts are not published
  ---
  ```

- Link between pages with wikilinks: `[[file-name]]` or `[[file-name|shown text]]`.
  Math with `$...$` / `$$...$$` (KaTeX), Obsidian callouts with `> [!note]`.

## Preview locally

Needs Node >= 22 (this repo was set up with Node 24 from nvm).

```bash
npm ci                       # once, installs dependencies
npx quartz build --serve     # http://localhost:8080, rebuilds on save
```

## Deploy

Pushing to `master` runs `.github/workflows/deploy.yml`, which builds the site and deploys it
to GitHub Pages. In the repo's Settings > Pages, Source must be set to "GitHub Actions".

Site settings are in `quartz.config.ts`; page layout (graph, backlinks, table of contents) is in
`quartz.layout.ts`.
