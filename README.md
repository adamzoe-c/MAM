# Casa Alba

Bilingual (Italian / English) website for **Casa Alba**, a family-run café, cocktail bar and bistro in Borgo Sereno. Plain HTML, CSS and JavaScript: no build step, no framework, no dependencies to install.

## Features

- **Bilingual:** IT/EN switch in the header. The choice is saved in the browser (localStorage, key `casa-alba-lang`) and defaults to Italian.
- **Responsive:** desktop, tablet and mobile layouts, with a slide-in mobile menu.
- **Hero:** split layout with an arch-framed photo, an "open today" chip and a rating chip. If the photo is missing, an illustrated placeholder shows instead.
- **Gallery:** 3-column grid on desktop, swipeable carousel on mobile, with a full-screen lightbox (arrow keys, swipe and Esc supported).
- **Reviews:** TripAdvisor rating bar, review cards and a "leave a review" call to action.
- **Scroll-reveal animations** and a sticky header with an announcement bar.

## Project structure

- index.html - Home page (contains all CSS and JS)
- chi-siamo.html - About us
- bistro.html - Bistro menu
- caffetteria.html - Café menu
- cocktail.html - Cocktail menu
- eventi.html - Events
- dove-siamo.html - Location
- recensioni.html - Reviews
- privacy-policy.html - Privacy policy
- cookie-policy.html - Cookie policy
- hero.jpg - Hero photo (portrait or square, 900px wide or more)
- 1.jpg to 6.jpg - Gallery photos
- a.jpg - Team / guests photo (TripAdvisor bar)
- r1.jpg to r3.jpg - Reviewer avatars
- m.jpg - Photo of Borgo Sereno

Keep all images in the same folder as index.html. Any missing image falls back to a styled placeholder.

## Running locally

Open index.html in a browser, or serve the folder:

    python3 -m http.server 8000

Then visit http://localhost:8000

## Things to replace before going live

- Booking link: the href="#" on the "Book a table" button
- TripAdvisor profile and "write a review" links: href="#" in the rating bar and review button
- Rating and review count (4,8 / 120): sample figures in the rating bar and hero chip
- Reviews: three sample review cards
- Google Maps embed: the .map-placeholder block
- Phone, email, Facebook link: footer
- Address and opening hours: hero, location section and footer
- City description: sample text in "The city" section
- Photos: see project structure

## Editing content in two languages

Every text exists twice, once per language:

    <p class="lang-it">Testo in italiano</p>
    <p class="lang-en">Text in English</p>

The html element carries lang-it or lang-en, and CSS hides the other language. When you change a text, update both versions.

## Customising the look

Colours are CSS variables at the top of the style block:

    :root{
      --gold:#4F8577;
      --gold-soft:#BFE0D6;
      --espresso:#2E2E2E;
      --wine-2:#F3FAF8;
    }

Fonts: Fraunces (headings) and Manrope (body), loaded from Google Fonts.

## Deploying

The site is static, so it can be hosted anywhere: Netlify, Vercel, GitHub Pages, Cloudflare Pages or any standard host. Upload the whole folder with index.html at the root.

## Before launch checklist

- [ ] All href="#" placeholders replaced
- [ ] Real photos added and checked on mobile
- [ ] Sample reviews and sample text replaced
- [ ] Google Maps embed added
- [ ] Privacy and cookie policies reviewed for your region (GDPR)
- [ ] Page title and meta description checked on every page

## License

All rights reserved © 2026 Casa Alba.
