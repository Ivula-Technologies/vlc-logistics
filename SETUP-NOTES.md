# VLC Logistics website: setup notes

Client: Valence Logistics and Clearing Ltd (VLC Logistics). Built by Ivula Technologies from the company profile.

## What it is
A one-page site with a looping port video behind the hero, sections for About, Customs, Transport and transit corridors (custom route map), Warehousing, fleet and HSSE, Why VLC with the 4-step workflow, Leadership, and a quote form. Plain HTML/CSS/JS, so it runs on any cPanel plan. No database, no build step.

## Upload to cPanel
1. cPanel > File Manager > `public_html` of the client's domain.
2. Upload `vlc-logistics-website.zip`, then Extract. The files sit at the top of the zip, so they land straight in `public_html`.
3. Run AutoSSL (SSL/TLS Status) so the site opens on https. The `.htaccess` sends visitors to https.
4. Create a mailbox `noreply@<their domain>` in cPanel Email Accounts. The quote form sends from it to valencelogisticsandclearing@gmail.com. To send to another inbox, change `TO_EMAIL` at the top of `contact.php`.
5. Test: submit the quote form once and check the Gmail inbox (and its spam folder the first time).

## Video and photos
- Hero video: Mixkit clip 31019 "Container cranes unloading a cargo ship"; transport band: Mixkit 52447 (trucks from the air). Photos: Unsplash. Both licences allow free commercial use with no credit.
- They currently stream from the Mixkit and Unsplash servers. To serve the videos from the client's own hosting (faster and safer long term), download the two clips and upload them as `assets/media/hero.mp4` and `assets/media/road.mp4`. The page uses local files automatically when they exist.
  - https://assets.mixkit.co/videos/31019/31019-720.mp4 -> `assets/media/hero.mp4`
  - https://assets.mixkit.co/videos/52447/52447-720.mp4 -> `assets/media/road.mp4`
- If any photo ever fails to load, its frame shows a navy branded panel instead of a broken image.

## Still needed from the client
1. Logo as PNG with a transparent background or SVG. The header uses a typed VLC wordmark until then; the footer uses the logo from the profile.
2. Real photos: their truck, the team at work, the office at Repen Complex. These replace stock photos and build trust fastest.
3. Domain name, and whether they want a domain email (e.g. info@).
4. Full office address or Google Maps pin for Repen Complex.
5. Company registration number, KRA PIN, customs licence and KIFWA/KPA membership if they want a compliance block on the site (left out because the profile has them blank).
6. Social media links, if any.

## Files
- `vlc-logistics-website.zip`: the `site/` folder, ready to upload.
- Source: GitHub Ivula-Technologies/vlc-logistics (main). The Actions tab builds the upload zip on every change.
