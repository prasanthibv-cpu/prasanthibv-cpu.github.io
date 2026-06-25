# 📚 Professor Website — Setup & Maintenance Guide

## Folder Structure

```
professor-website/
├── index.html          ← Main website file (edit this)
├── resume.pdf          ← Your resume (replace this file)
├── notes/
│   ├── data-structures/    ← Upload PDF lecture notes here
│   ├── operating-systems/
│   ├── machine-learning/
│   ├── computer-networks/
│   └── dbms/
└── README.md
```

---

## ✏️ How to Customize the Website

Open `index.html` in any text editor (Notepad, VS Code, Notepad++) and look for the `✏️` comments — they mark every place you need to update:

| What to update | Where to look |
|---|---|
| Your name | `<title>`, `<h1>`, `<a class="nav-logo">` |
| Your role / department | `.hero-text .role` section |
| Your bio | `.hero-text .bio` paragraph |
| Photo / initials | `<div class="avatar">` — change `PN` to your initials |
| Stats (years, subjects etc.) | `.stats-inner` section |
| Resume PDF link | `href="resume.pdf"` |
| Work experience | `.timeline-row` blocks under Resume |
| Education / Awards | The card grid under Resume |
| Subjects & note folders | `.subject-row` blocks |
| Blog posts | `.blog-card` blocks |
| Email / LinkedIn / GitHub | Inside `#contact` section |

---

## 📂 How to Add Lecture Notes

### Option A — Direct file upload (Simplest)
1. Place your PDF / PPT files inside the relevant folder, e.g. `notes/machine-learning/lecture1.pdf`
2. In `index.html`, the "View →" link for that subject already points to that folder
3. Students can browse and download directly

### Option B — Google Drive (Recommended for large files)
1. Upload your notes to a Google Drive folder
2. Right-click the folder → "Get link" → set to "Anyone with the link can view"
3. In `index.html`, find the subject row and change `href="notes/machine-learning/"` to your Drive link

### Option C — Google Classroom / LMS
Just link directly to your existing LMS page by replacing the `href` in the subject rows.

---

## 🚀 How to Deploy (Make it Live on the Internet) — FREE

### Method 1: GitHub Pages (Recommended — Free, no ads)

1. Create a free account at [github.com](https://github.com)
2. Click **"New Repository"** → Name it `your-username.github.io`
3. Upload all your files (drag and drop)
4. Go to **Settings → Pages → Source → main branch**
5. Your website will be live at: `https://your-username.github.io`

### Method 2: Netlify (Drag & Drop — Easiest)

1. Go to [netlify.com](https://netlify.com) → Sign up free
2. Drag your entire `professor-website` folder onto the Netlify homepage
3. Done! You get a link like `https://your-name.netlify.app`
4. You can connect a custom domain later

### Method 3: Your University Web Server
Ask your IT department — many universities give faculty a web space like `faculty.university.edu/yourname`

---

## 🔄 How to Update the Website

### If using GitHub Pages:
1. Edit `index.html` on your computer
2. Go to your GitHub repo → click the file → click **Edit (pencil icon)**
3. Paste your updated content → click **"Commit changes"**
4. Site updates in ~1 minute

### If using Netlify:
1. Edit `index.html` on your computer
2. Drag the updated folder to Netlify again → it auto-updates

---

## ➕ How to Add a New Subject

In `index.html`, find the Lecture Notes section and copy-paste this block:

```html
<div class="subject-row">
  <div class="subject-left">
    <div class="subject-dot" style="background:var(--purple)"></div>
    <div>
      <div class="subject-name">YOUR SUBJECT NAME</div>
      <div class="subject-meta">X files · PDF · Updated Month Year</div>
    </div>
  </div>
  <div class="subject-right">
    <span class="pill" style="background:var(--purple-light);color:var(--purple)">Sem X</span>
    <a class="view-btn" href="notes/your-subject-folder/">View →</a>
  </div>
</div>
```

Change the colors using: `var(--purple)`, `var(--teal)`, `var(--coral)`, `var(--amber)`, `var(--pink)`

---

## ➕ How to Add a Blog Post

Copy-paste this block inside the Blog section:

```html
<div class="blog-card">
  <div class="blog-num">04</div>
  <div>
    <div class="blog-date">Month Year</div>
    <div class="blog-title">Your Blog Post Title Here</div>
    <div class="blog-desc">A short description of what the post is about.</div>
    <a class="read-link" href="link-to-your-post.html">Read more →</a>
  </div>
</div>
```

---

## 💡 Tips

- **Resume**: Replace `resume.pdf` in the folder — the download button already links to it
- **Profile photo**: Replace the initials `PN` in `.avatar` with an `<img>` tag if you want a real photo
- **Google Analytics**: Add your GA tracking code before `</head>` to see how many visitors you get
- **Custom domain** (e.g. `profyourname.in`): Buy from GoDaddy (~₹700/year) and point it to GitHub Pages or Netlify — both support custom domains for free

---

*Made for Prof. Your Name · Tamil Nadu, India*
