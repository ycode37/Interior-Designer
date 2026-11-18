# Marcus Aurelius — Website Design Demo

A single-file demonstration website for a fictional luxury interior design studio, built to show an interior designer what their own site could look like.

> **Note:** Marcus Aurelius is a fictional brand. All projects are concept projects, not real client work. The site contains no testimonials, ratings, awards, or client logos.

## Files

| File | Purpose |
| --- | --- |
| `Marcus-Aurelius.html` | The complete website (HTML, CSS, and JavaScript in one file) |
| `README.md` | This guide |

## Quick start

1. Download `Marcus-Aurelius.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).
3. An internet connection is needed for the Tailwind CDN, Google Fonts, and Unsplash images.

No install, build step, or server is required. To host it, upload the file to any static host (Netlify, GitHub Pages, Vercel, or ordinary web hosting) and rename it to `index.html` if you like.

## Tech stack

- HTML5 with semantic landmarks
- Tailwind CSS via CDN (pinned to 3.4.17) plus custom CSS
- Vanilla JavaScript only (no frameworks, libraries, or backend)
- Fonts: Cormorant Garamond (display) and Manrope (body), from Google Fonts

## Sections (in order)

1. **Hero:** headline, two calls to action, arch-shaped image with gentle parallax, scroll indicator
2. **About:** studio philosophy, three capability highlights, captioned material photo
3. **Services:** three keyboard-accessible cards with inline SVG icons
4. **Project gallery:** six concept projects, category filters, accessible lightbox
5. **Working process:** four-step stepper (horizontal on desktop, vertical on mobile)
6. **WhatsApp enquiry:** validated form plus a direct chat button
7. **Footer:** wordmark, navigation, hours, address, contact details

## Customising

### Change the WhatsApp number
Search the file for `919999999999` and replace it (two places: the "Chat on WhatsApp" link and the form's `wa.me` URL in the script). Use the country code followed by the number, with no `+` or spaces.

### Edit project content
Projects live in the `P` array inside the `<script>` tag near the bottom. Each entry has a title, category, one-line description, Unsplash image ID, alt text, brief, design approach, and materials list. If you add a new category, also add it to the `cats` array so a filter tab appears.

### Swap images
Replace the Unsplash photo ID in the `P` array, or change the `src` URLs for the hero and about images. Keep the `?auto=format&fit=crop&w=…&q=…` parameters for fast loading. If an image fails to load, replace its photo ID.

### Change colours
The palette is set in the `tailwind.config` block near the top:

| Name | Hex |
| --- | --- |
| Warm ivory | `#F6F1EA` |
| Deep charcoal | `#171512` |
| Muted clay | `#A96F55` |
| Soft olive | `#6E7355` |
| Pale stone | `#D9D2C7` |

A deeper clay (`#8A5640`) is used for small text and active states so it meets contrast standards on ivory. The original clay is used for borders and glows.

### Edit studio details
Business hours, address, email, and phone are in the `<footer>`. The brand name and tagline appear in the nav, hero, and footer.

## Accessibility

- Skip-to-content link and visible keyboard focus states
- ARIA roles for the stepper (tabs), lightbox (dialog), and filter buttons
- Lightbox closes with the Close button, the Escape key, or a backdrop click, and traps focus while open
- Form errors are announced to screen readers
- Animations are removed or simplified when the visitor's system uses reduced motion
- Responsive from 320px to 1920px

## Known limitations

- The form does not send data to a server. It opens WhatsApp with a pre-filled message.
- Images load from Unsplash, so they need an internet connection.
- Placeholder contact details (phone, email, address) are fictional and should be replaced for a real client.

## Credits

Photography from [Unsplash](https://unsplash.com) under the Unsplash License. The Marcus Aurelius name, wordmark, and mark are original to this demo.
