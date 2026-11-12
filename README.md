# VLC Logistics website

Website for Valence Logistics and Clearing Ltd (VLC Logistics), built by Ivula Technologies.
A one-page static site (HTML, CSS, JS) with a PHP quote form. No build step, no database.

## Layout
- `site/` is everything that goes into the domain's `public_html`.
- `site/contact.php` emails quote requests to `valencelogisticsandclearing@gmail.com` (change `TO_EMAIL` at the top). It sends from `noreply@<site domain>`, so create that mailbox in cPanel.
- `site/assets/media/` is empty on purpose. Drop `hero.mp4` and `road.mp4` here to serve the videos from the client's hosting; until then they stream from Mixkit.

## Deploy (cPanel)
1. Download the `vlc-logistics-website` zip from the latest "Build cPanel zip" run in the Actions tab (or zip the `site/` folder yourself).
2. cPanel > File Manager > `public_html` > Upload > Extract.
3. Run AutoSSL, create the `noreply@` mailbox, and send one test quote.

## Media credits
Video from Mixkit (clips 31019 and 52447) and photos from Unsplash, both free for commercial use without attribution.
