# CarConnect AI — copy-clean landing page

Files included:

- `index.html`
- `pricing.html`
- `thanks.html`
- `styles.css`
- `assets/icon-32.png`
- `assets/icon-192.png`

## What changed

- Removed internal strategy / instruction copy from the live pages
- Rewrote the homepage and pricing page with customer-facing dealer messaging
- Kept the founding beta pricing, icon assets, and email form setup
- Left the existing design system and layout intact

## Form / email setup

The homepage form is configured for FormSubmit so it works on a static GitHub Pages site without a custom backend.

Form action in `index.html`:

```html
<form action="https://formsubmit.co/contact@onlyusedtesla.com" method="POST">
```

Important:

1. The first live submission will trigger a FormSubmit confirmation email to `contact@onlyusedtesla.com`.
2. After that confirmation, future submissions will be forwarded there.
3. The redirect after submit is set to:

```html
<input type="hidden" name="_next" value="https://adamqureshi.com/car-connect-ai/thanks.html" />
```

If you change the domain or path later, update `_next`.

## Deployment

Upload these files to the root of the GitHub Pages repo and redeploy.
