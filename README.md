# Adalah Council website: how to add articles and videos

You never edit code to add content. You use a form in your browser.

## One-time setup (about 5 minutes)
1. Make sure the new files are in your GitHub repo (see "Uploading" below).
2. Go to https://app.pagescms.org and click **Sign in with GitHub**.
3. When asked, **install the GitHub App** on your account and allow it to access this repository
   (choose "Only select repositories" and pick the site's repo).
4. Open the repository in Pages CMS. You will see two items on the left: **Articles** and **Videos**.
   (If it asks you to create a `.pages.yml` file, the file from this package is already in the repo;
   if it is missing, create it and paste in the contents of `.pages.yml` from this package.)

## Adding an article
1. Pages CMS -> **Articles** -> **Add an entry**.
2. Fill in: Title, Summary, Date, Type (Essay / Research / Statement / Announcement), and the Article text.
3. In the article text, use the **Heading** style for section titles (these become the contents list on the
   side). Normal paragraphs, bold, italics, links, quotes and images all work.
4. Click **Save**. Wait about a minute. The article appears on the Writing page, gets its own web address,
   and is added to the sitemap automatically.

To hide something: turn **Published** off (it stays saved as a draft). To remove it: delete the entry.
To fix a typo: open the entry, edit, Save.

## Adding a video
Pages CMS -> **Videos** -> add an item: title, speaker, year, length, topic, and paste the full YouTube link.
Topic buttons on the Media page appear automatically from the topics you use.
Videos at the top of the list appear first.

## Uploading these files to GitHub (browser)
1. Unzip the package. In your repo click **Add file -> Upload files**.
2. Drag in everything from inside the folder, including the folders `_articles`, `_data`, `_layouts`,
   `assets`, and the file `.pages.yml` (hidden files: on Mac press Cmd+Shift+. in the file picker to show them).
3. **Delete these old files from the repo** if they exist: `article.html`, `article-template.html`, `.nojekyll`.
   (`.nojekyll` MUST be deleted. It turns off the automatic page building this setup depends on.)
   To delete: click the file -> trash icon -> Commit.
4. Settings -> Pages should still say "Deploy from a branch" (main, / root).
5. After uploading, open the repo's **Actions** tab. A green check means the build worked.

## Things to know
- Do not rename the folders that start with an underscore (`_articles`, `_data`, `_layouts`).
- Images you add inside an article are stored in `assets/uploads`.
- The preview copy of the site (project address like username.github.io/adalah-preview) uses its own
  `_config.yml` with the line `baseurl: "/adalah-preview"`. If you named the preview repo something else,
  change that line to match. The live-site version has `baseurl: ""`.
- Writing pull quotes and footnotes is possible but needs a little extra markup; the form covers everything else.
