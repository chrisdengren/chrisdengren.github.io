# How to put your website online — step by step

Your GitHub account is **[github.com/chrisdengren](https://github.com/chrisdengren)**, so your site will live at:

> **https://chrisdengren.github.io**

Everything below can be done in a web browser by clicking buttons — no Git, no terminal, no coding tools. About 10–15 minutes total the first time.

---

## What GitHub is (30-second version)

**GitHub** is a website that stores folders of files. Each folder is called a **repository** (or "repo"). Think of it like Google Drive, but for code.

**GitHub Pages** is a free feature of GitHub: if you name a repository in a specific way, GitHub automatically turns the files inside it into a live website. That's all we're using it for.

---

## Step 1 — Create the repository

1. Log in to GitHub. Top-right, click the **`+`** icon → **New repository**.
2. Fill in the form:
   - **Repository name**: type exactly `chrisdengren.github.io`. This name is what tells GitHub Pages to treat it as your personal site.
   - **Description**: optional (e.g. "Personal website").
   - Set it to **Public**. (Private repos don't work for free Pages.)
   - **Do NOT** check "Add a README file" or any of the other initialization boxes. Leave them off.
3. Click the green **Create repository** button.

You'll land on a mostly-empty page with the heading "Quick setup." Leave that tab open.

---

## Step 2 — Upload your site files

On that same page, look for the small link in the middle that says:

> **uploading an existing file**

Click it. (If you can't spot it, this is the direct URL: `https://github.com/chrisdengren/chrisdengren.github.io/upload/main`.)

1. You'll see a large drag-and-drop zone. **Drag `index.html` into it.** You can also drag `README.md` if you'd like — it won't affect the website, it just shows up on the repo's GitHub page.
2. Scroll down. In the "Commit changes" box, leave the default message or type "Initial site."
3. Click the green **Commit changes** button.

Your files are now on GitHub. The site isn't *live* yet — one more step.

---

## Step 3 — Turn on GitHub Pages

1. In the repo, click the **Settings** tab (far right of the repo's top menu).
2. In the left sidebar, click **Pages**.
3. Under **"Build and deployment"**:
   - **Source**: select **Deploy from a branch**.
   - **Branch**: pick `main` and the folder `/ (root)`.
   - Click **Save**.
4. Wait about **1–2 minutes**. Refresh the Pages settings page. A green box will appear at the top saying:

   > **Your site is live at `https://chrisdengren.github.io`**

Click that link. That's your website. It's on the open internet. 🎉

---

## Step 4 — Small polish items (optional but recommended)

Open `index.html` on GitHub (click the filename in your repo), then click the **pencil icon** at the top-right to edit it in the browser.

Things to consider updating:

- **Lab links.** In the About paragraph, the three lab names (Prigozhin Lab, Sahin Lab, High-Energy Astrophysics Group) currently link to `#`. Replace the `#` with the real lab URLs if you have them.
- **CV link.** The "CV" link in the header points to `cv.pdf`. To make it work, upload your CV PDF (see below) and name it `cv.pdf`.
- **"Last updated" line.** At the very bottom of the file, update the date when you make major changes.

When you're done editing, scroll down, type a short commit message (e.g. "Fix lab links"), and click **Commit changes**. Your live site updates in ~30 seconds.

### Adding your CV PDF

1. On your repo's main page, click **Add file** → **Upload files**.
2. Drag your CV PDF in. Rename it to `cv.pdf` (easiest option) before uploading, or rename the file in the form.
3. Commit. The "CV" link in your header now works.

---

## How to edit the site later

Any time you want to change something:

1. Go to `github.com/chrisdengren/chrisdengren.github.io`.
2. Click the file you want to edit (usually `index.html`).
3. Click the pencil icon → make changes → scroll down → **Commit changes**.
4. Wait ~30 seconds. Site updates automatically.

You can add new files (photos, PDFs, extra pages) the same way: **Add file** → **Upload files**.

---

## Common gotchas

- **Repo name must be exactly `chrisdengren.github.io`.** Lowercase, no typos. If you mistype it, Pages won't auto-deploy.
- **Repo must be public.** Private repos need a paid plan for Pages.
- **Changes take ~30–60 seconds to go live.** If you don't see an update, wait a minute and do a hard refresh (Ctrl+Shift+R / Cmd+Shift+R).
- **Only one user site per account.** `chrisdengren.github.io` is your one free personal site. (You can still make other normal repos — they just won't be the "main" site.)
- **You cannot break anything irreversibly.** Every edit is tracked, and you can always view or restore older versions from the repo's "History" button.

---

## Where things are in `index.html`

The file is organized with comments like `<!-- ============ PUBLICATIONS ============ -->` so you can use your browser's Find (Ctrl+F / Cmd+F) to jump to a section.

| To change... | Search for... |
|---|---|
| Name, affiliation, contact links | `HEADER` |
| About paragraphs | `ABOUT` |
| News / updates list | `NEWS` |
| Publications list | `PUBLICATIONS` |
| Research positions | `RESEARCH` |
| Talks and posters | `TALKS` |
| Teaching | `TEACHING` |
| Leadership / activities | `SERVICE` |
| Colors (accent, link color, background) | `:root {` (near the top, inside `<style>`) |

The link color is a muted academic red `#8b2a1f`. Change it in the `:root { }` block if you want a different accent — muted navy `#1f3a5f` or forest green `#2d5a3d` are common academic alternatives.

---

## Later, if you want

- **Add a photo.** Upload `photo.jpg` to the repo. Then, just below the `<header>` opening tag in `index.html`, paste:
  ```html
  <img src="photo.jpg" alt="Ren Deng" style="width:140px;border-radius:50%;float:right;margin-left:20px;margin-bottom:10px;" />
  ```
- **Custom domain** (e.g. `rendeng.com`). GitHub has a short setup guide: [docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
- **Learn Git properly.** Once you're comfortable with the site, learning the `git` command line makes editing faster. For a personal academic page, though, the browser workflow above is fine forever.
