# Social media manager portfolio

A plain HTML, CSS and JavaScript site. No build step, no backend, free on GitHub Pages.

## Files

| Path | What it is |
| --- | --- |
| `js/content.js` | **All your content.** Edit this file to change text, add work, or reorder it. |
| `css/style.css` | Layout and styling. You should not need to touch it for content changes. |
| `js/app.js` | Builds the pages and the image viewer. |
| `index.html` | The page shell. Change the `<title>` and description here. |
| `assets/photos`, `assets/reels`, `assets/design` | Put your images and videos here. |

## Replace the placeholders

Everything labelled `[Placeholder]` is sample content. Nothing in it is real.

1. Open `js/content.js`.
2. In `SITE`, set your name, email, social links, intro, About text and services.
3. Set `showPlaceholderNotice: false` when you are done (removes the black banner).

### Photography
Copy your image into `assets/photos/` and edit an entry in `PHOTOS`:

    { group: "Church", src: "assets/photos/service-01.jpg", w: 1600, h: 1067,
      caption: "Sunday service", role: "Photography", alt: "Congregation singing" }

- `group` creates the filter on the page (Church, Events, Portraits, or your own).
- `w` and `h` are the image's pixel width and height. They keep the page from jumping while images load.
- `alt` describes the image for screen readers. Please fill it in.
- `featured: true` shows it on the Home page.
- To reorder, move the line up or down. To add, copy a line. To remove, delete it.

### Reels
Save the video in `assets/reels/` (MP4, H.264) and add a cover image if you like:

    { title: "Event recap", role: "Filming, editing", description: "What it was and what you did.",
      video: "assets/reels/recap.mp4", poster: "assets/reels/recap.jpg", featured: true }

Videos keep their own shape. Export vertical 9:16 (for example 1080 x 1920).
To use an embed instead of a file, set `embed` to the embed URL (for example the `src` of YouTube's embed code) and leave `video` empty.

### Graphic design
Each project has a list of `images`, so a carousel is one project with several images:

    { title: "Spring campaign", role: "Concept, graphic design", description: "...",
      images: [ { src: "assets/design/spring-1.jpg", w: 1080, h: 1350 },
                { src: "assets/design/spring-2.jpg", w: 1080, h: 1350 } ] }

## Prepare your files (keeps the site fast)

- Photos: resize to about 2000 px on the long edge and export as JPEG at 75 to 85 percent quality (or WebP). Aim for under 500 KB each.
- Videos: MP4 (H.264), 1080 x 1920 or smaller, ideally under 25 MB each. GitHub rejects files over 100 MB, so use an embed for anything larger.
- Use lowercase file names with no spaces, such as `service-01.jpg`. File names are case-sensitive on GitHub Pages.

## Preview on your computer

Open `index.html` in a browser, or for the most accurate result run this in the project folder and visit http://localhost:8000:

    python3 -m http.server 8000

## Publish on GitHub Pages

1. Create a free account at https://github.com.
2. Click **New repository**. Name it (for example `portfolio`), choose **Public**, and click **Create repository**.
3. On the new repository page click **uploading an existing file**. Drag in **the contents** of this folder (`index.html`, `css`, `js`, `assets`, `README.md`, and the hidden `.nojekyll` file if your computer shows it), so `index.html` sits at the top level. Click **Commit changes**.
4. Open **Settings**, then **Pages**.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**. Set **Branch** to `main` and the folder to `/ (root)`. Click **Save**.
6. Wait one to two minutes and refresh. The site is at `https://YOUR-USERNAME.github.io/portfolio/`.

To update later, open the file in your repository, click the pencil icon, edit, and commit. For images, use **Add file, Upload files**.

### Using your own username URL
Name the repository exactly `YOUR-USERNAME.github.io` and the site appears at `https://YOUR-USERNAME.github.io/`.

### Custom domain
In **Settings, Pages, Custom domain**, enter your domain and follow GitHub's DNS instructions.

## Troubleshooting

- **Image or video missing:** check the path in `content.js` matches the file name and capitals exactly.
- **Page is blank:** a typo in `content.js` (a missing comma or quote) stops the site. Open the browser console (F12) to see the line number.
- **404 after publishing:** `index.html` must be at the repository's top level, and Pages must be enabled in Settings.
- **Old version showing:** hard refresh with Ctrl+Shift+R (Cmd+Shift+R on Mac).

All asset paths are relative and navigation uses `#` links, so the site works on both project URLs (`/portfolio/`) and username URLs.
