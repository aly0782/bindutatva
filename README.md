# Bindutatva Website

**bindutatva.com** — Landing page and shop for original yantra art by Namita.

---

## Files in this project

```
bindutatva/
├── index.html          ← Home / landing page
├── shop.html           ← Full collection / shop page
├── assets/
│   └── images/         ← Put all your yantra photos here
└── README.md           ← This file
```

---

## How to add a new yantra to the shop

1. Take a good photo of the yantra (see photo tips below)
2. Name the file clearly, e.g. `vishnu-yantra.jpg`
3. Put it in the `assets/images/` folder
4. Open `shop.html` in any text editor (Notepad, TextEdit, or VS Code)
5. Find the comment that says:
   ```
   <!-- HOW TO ADD A NEW PIECE -->
   ```
6. Copy the entire block from `<article class="piece-card"...>` to `</article>` for any existing piece
7. Paste it just before the `<!-- END shop-grid -->` comment
8. Change these five things in your pasted block:
   - `data-price="24500"` → your actual price in rupees (no commas, just numbers)
   - `data-status="available"` → keep as `available`, or change to `sold` or `commission`
   - Replace the `<svg>...</svg>` placeholder with: `<img src="assets/images/your-filename.jpg" alt="Yantra name by Bindutatva" />`
   - Update the name, deity, subtitle, and price text
   - Update the Etsy link to the specific listing URL

**If a piece sells**, find its card in `shop.html` and:
- Change `data-status="available"` to `data-status="sold"`
- Change `class="piece-card"` to `class="piece-card sold"`
- Change `<a href="..." class="btn-etsy">Buy on Etsy</a>` to `<span class="btn-sold">Sold</span>`
- Change the badge from `badge-new` to `badge-sold` and text to `Sold`

---

## How to update prices

In `shop.html`, search (Ctrl+F) for the price you want to change.  
You'll see it in two places per card — `data-price="21000"` and `<div class="card-price">₹21,000</div>`.  
Update both.

---

## How to update the Etsy shop link

Search the file for `etsy.com/shop/bindutatva` and replace with your actual Etsy shop URL.  
It appears in multiple places — replace all of them.

---

## Photo tips for the yantras

- Photograph in natural daylight, no flash
- Place on a clean white or dark surface — both work
- Shoot directly overhead (birds-eye view), not at an angle
- Minimum 1500 × 1500 pixels
- Save as JPG, keep file size under 1MB (use squoosh.app to compress if needed)
- Name files clearly: `sri-yantra-navayoni.jpg`, `kali-yantra-shakti.jpg` etc.

---

## How to make the site live (deployment)

### First time setup (you do this once)
1. Create a free account at **netlify.com**
2. Create a free account at **github.com**
3. Create a new repository on GitHub called `bindutatva`
4. Upload all files (index.html, shop.html, assets/ folder) to that repository
5. In Netlify, click "Add new site" → "Import from Git" → connect your GitHub → select `bindutatva`
6. Netlify gives you a free URL like `bindutatva.netlify.app`

### Every time you make a change
1. Edit the file on your computer
2. Go to GitHub, open the file, click the pencil icon to edit, paste your changes, click "Commit"
3. Netlify automatically rebuilds the site within 30 seconds

### To connect a custom domain (bindutatva.com)
1. Buy the domain on **namecheap.com** or **godaddy.com**
2. In Netlify: Site settings → Domain management → Add custom domain
3. Follow Netlify's instructions to point the domain — takes about 10 minutes

---

## Etsy setup checklist for Namita

- [ ] Create Etsy account with username `bindutatva`
- [ ] Add bank account details (account number + IFSC) for INR payouts
- [ ] Add PAN card details
- [ ] Set shop location: Pune, Maharashtra, India
- [ ] Add shop banner and logo (use the same gold-on-dark aesthetic)
- [ ] Write shop bio explaining the yantra tradition and your practice
- [ ] Create first listing with good photos, description, and keywords
- [ ] Set shipping profile: flat rate for India Post, higher rate for FedEx/DHL

**Etsy listing title formula:**
`Original [Yantra Name] Art · Hand-drawn on 400 GSM Paper · Tantric Sacred Geometry · [Size]`

**Etsy tags to use on every listing:**
yantra art, sacred geometry art, original yantra, handmade spiritual art, tantric art, sri yantra, yantra painting, indian spiritual art, 400gsm art, wall art india

---

## Instagram checklist for Namita

- [ ] Create account: @bindutatva
- [ ] Bio: "Original yantra art · hand-drawn · 400 GSM archival paper · Pune 🇮🇳 · Shop link below"
- [ ] Link in bio → bindutatva.com
- [ ] Post 4–5 times a week for first 3 months
- [ ] Best content: timelapse process Reels (highest reach), finished piece photos, meaning/education posts
- [ ] Hashtags every post: #yantraart #sacredgeometry #yantra #hinduart #spiritualart #handmadeart #IndianArt #tantricart #sriyantra #originalart

---

## Handing over to another developer

Give them this README and the GitHub repository link. Everything they need to know is here.  
The site is plain HTML/CSS/JavaScript — no frameworks, no build tools, no dependencies.  
Any developer can open the files in VS Code and understand them within 10 minutes.

---

## Questions?

The site was built with help from Claude (claude.ai). If you're stuck on anything, open Claude and paste the section of code you're confused about — it will explain it or fix it for you.
