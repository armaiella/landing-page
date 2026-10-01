# Alex Maiella — Landing Page

## What's in here
- `index.html` — the landing page (self-contained, no build step)
- `robots.txt` — tells search engines they can crawl the site
- `sitemap.xml` — helps Google index the page faster

## Deploy to GitHub Pages (free)
1. Create a new GitHub repo (public). If you want it at `yourusername.github.io`,
   name the repo exactly `yourusername.github.io`. Otherwise any repo name works.
2. Upload these three files to the repo (drag-and-drop works fine on github.com,
   or `git add . && git commit -m "landing page" && git push`).
3. In the repo, go to **Settings > Pages**, set the source branch to `main` and
   folder to `/ (root)`. Save.
4. GitHub gives you a live URL within a minute or two, either
   `yourusername.github.io` or `yourusername.github.io/repo-name`.

## Point a custom domain at it (optional, best for SEO)
1. Buy a domain (e.g. alexmaiella.com) from any registrar (Namecheap, Google
   Domains successor Squarespace Domains, etc.) — roughly $10-15/year.
2. In the repo, add a file named `CNAME` (no extension) containing just your
   domain, e.g. `alexmaiella.com`.
3. At your domain registrar, add these DNS records:
   - Four `A` records pointing your root domain to GitHub's IPs:
     185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - A `CNAME` record for `www` pointing to `yourusername.github.io`
4. Back in **Settings > Pages**, enter your custom domain and check
   "Enforce HTTPS" once it's available.
5. Once your domain is live, update these two things in `index.html` and
   `sitemap.xml`/`robots.txt`: replace every `https://alexmaiella.com/`
   placeholder with your real domain if it's different.

## Connect your newsletter (Kit)
1. Sign up free at kit.com (formerly ConvertKit).
2. Create a Form under **Grow > Landing Pages & Forms**.
3. Copy the Form ID from the form's embed settings.
4. Open `index.html`, find the comment block near the bottom marked
   `KIT (ConvertKit) SETUP`, and replace `YOUR_FORM_ID` in the form's
   `action` URL with your real Form ID.
5. Test it by submitting your own email and confirming it lands in your
   Kit subscriber list.

## Adding your hero photo
Your hero now uses `headshot.png` — the cutout version you sent, background
already removed. Upload `headshot.png` to the same repo folder as
`index.html`. To swap in a different photo later, upload a new file also
named `headshot.png` to replace it (keep it a PNG so the transparency
carries over), or edit the `src` in `index.html`'s `<img class="hero-photo">` tag.

## Connect a live Instagram feed
A static page can't fetch your latest posts on its own — that needs an
authenticated connection. The free fix: sign up at snapwidget.com (or
lightwidget.com / elfsight.com), connect @alexmaiella.realestate, pick a feed
layout, and copy the embed code it gives you. In `index.html`, find the
`insta-row` section near the bottom (comment marked `LIVE INSTAGRAM FEED
SETUP`) and replace the placeholder tiles with that embed code. It'll then
update automatically every time you post.

## Adding Featured Listings and Recent Transactions
Both sections in `index.html` use repeating card blocks with placeholder
photos and text — look for the HTML comments marked `FEATURED LISTINGS` and
`RECENT TRANSACTIONS` for exact instructions. In short: for each home,
duplicate one `<a class="card">...</a>` block, swap the placeholder
`.ph-image` div for a real `<img>` tag, update the link and text, and (for
transactions) keep the `.tag` text to exactly one of: Buyer Represented,
Seller Represented, Tenant Represented, or Landlord Represented.
