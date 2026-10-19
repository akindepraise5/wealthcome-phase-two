# Wealthcome homepage — phase two

Independent redesign concept by Praise Akinde. Not approved by or affiliated with Wealthcome.

## Run

Open `index.html` in a modern browser. No installation or build step is required, and there are no external font, script or package dependencies. CSS, JavaScript and the interface icons ([Heroicons](https://heroicons.com) v2, 24px outline) are inlined in `index.html`. The page also loads these local files, which must be deployed alongside it:

- `Dark background version.svg` — header logo
- `Wealthcome logo.svg` — footer logo
- `Logos/Container*.svg` — the 18 logos in the marquee under the hero
- `favicon.svg`, `favicon.png` — browser and touch icons
- `wealthcome-social-preview.png` — Open Graph / Twitter share image

The share metadata points at `https://wealthcome-phase-two.vercel.app/`.

## Structure

`index.html` contains everything: styles, markup, the French/English translation dictionaries (`translations`), the product map used by the product dialog (`products`), and the page behaviour. All visible text is set from the dictionaries through `data-i18n` and `data-i18n-aria` attributes; a missing key throws. `?lang=en` opens the English version.

Sections: concept banner, header, hero with a fictional WealthPro dashboard, logo marquee, products (#produits), Binom (#binom), evaluation questions, FAQ (#questions), testimonials, closing call to action, footer.

## Changes

- French/English switching for page content, product examples, form options, dialog results, accessible labels and document metadata.
- Responsive navigation, narrow-screen dashboard layout, text wrapping, touch targets and footer spacing.
- Visible keyboard focus, native dialog focus management and reduced-motion support.
- Section headings stand alone, with no eyebrow or kicker labels above them. Each product tile has an "Open details" button that opens a product dialog, plus a separate link to the product's official page (WealthPro, WealthConnect, WealthLab, WealthTreet, WealthOne, and the Binom announcement article).
- Logo marquee and testimonial carousel (tabs, arrows, swipe, auto-advance with pause; auto-advance is disabled with reduced motion).
- Footer links to Wealthcome's legal notice, privacy policy and terms of use.
- Interface icons replaced with Heroicons.
- Preserved the original visual direction, single-file architecture and independent-concept disclosures.

## Demo behaviour

The demo dialog has three steps: profile, priority, then a choice of time slot (the next three working days at 09:00, 11:00 and 14:00, generated in the browser). Choosing a slot shows a confirmation that says an expert will be in touch within 24 hours.

Nothing is sent or booked: there is no form submission, booking integration or data collection, as the footer states. The 24-hour statement is listed in the comment at the top of `index.html` as needing confirmation from Wealthcome before the page is shared. Binom's example is static illustrative content, not connected AI. External links open in a new tab, indicated by an arrow.

## To confirm with Wealthcome

See the comment at the top of `index.html`:

- authorization to display each marquee logo, and whether the brands are current clients;
- the "expert within 24 hours" statement in the demo confirmation;
- that the testimonials and attributions are authentic, approved and accurate in both languages.

## Checks completed

- Embedded JavaScript passes Node's syntax checker.
- Every `data-i18n` / `data-i18n-aria` key exists in both languages; both dictionaries have the same keys.
- No duplicate HTML IDs; all buttons have explicit types.
- In headless Chrome: no console errors; product details open from the keyboard and focus returns to the button on close; arrow keys move between product tiles; the testimonial pause/play icon switches; the English version updates the title, labels and legal links; no horizontal overflow at 390 and 320 CSS pixels.
- All official product and legal URLs returned HTTP 200 on 19 October 2026.

## Verification still required

Full browser checks at every supported width, 200% zoom, automated accessibility auditing, screen-reader testing and reduced-motion verification remain outstanding.

Before release, test both languages at 320, 390, 768, 1024 and 1440 CSS pixels, including 200% zoom. Check navigation opening/closing, all demo routes, product dialogs, the testimonial carousel, keyboard order, native dialog Tab containment, Escape dismissal and focus restoration. Check contrast in the rendered page and screen-reader announcements. Reconfirm outbound destinations and current product availability directly with Wealthcome.
