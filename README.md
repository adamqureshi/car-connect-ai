# CarConnect AI — updated MVP landing page

Updated files included:

- `index.html`
- `pricing.html`
- `thanks.html`
- `styles.css`
- `assets/icon.png`
- `assets/icon-32.png`
- `assets/icon-192.png`
- `assets/icon-512.png`
- `.nojekyll`

## What changed

- Added a **Founding Dealer Beta** pricing section on the homepage
- Added a dedicated `pricing.html` page
- Added the uploaded icon as the site brand mark and favicon
- Tightened the messaging around **starting with ChatGPT**
- Added brand equity / trust copy for **Qureshi Media LLC** and **Only Used Tesla**
- Wired the contact form to send leads to `contact@onlyusedtesla.com`

## Form / email setup

The form is currently configured for **FormSubmit** so it can work on a static GitHub Pages site without a custom backend.

Form action in `index.html`:

```html
<form action="https://formsubmit.co/contact@onlyusedtesla.com" method="POST">
```

Important:

1. The **first live submission** will trigger a FormSubmit confirmation email to `contact@onlyusedtesla.com`.
2. After that confirmation, future submissions will be forwarded there.
3. The redirect after submit is set to:

```html
<input type="hidden" name="_next" value="https://adamqureshi.com/car-connect-ai/thanks.html" />
```

If you change the domain or path later, update `_next`.

## Deployment

Because this is a simple static site, you can drop these files into the root of the GitHub Pages repo and redeploy.

## Notes

- If you want stronger spam protection later, switch to Formspree, Netlify Forms, or a custom endpoint.
- If you want a different pricing stance, adjust the two pricing cards in `index.html` and `pricing.html`.
