# XPath Demo Site (Intentional Tag Change)

This is a minimal static website intended for testing XPath / UI test self-healing PoCs.

## What's special
- The **home page** contains a "Sign In" element with `id="loginBtn"` implemented as a `<div>` (this is intentional).
- Your test baseline might expect a `<button>` or `<span>` for this element; the tag change simulates a broken XPath scenario.

## Files
- `index.html` — Home page (contains the intentionally modified element)
- `login.html` — Login form with username/password and a normal `<button>` submit
- `dashboard.html` — Small dashboard page
- `style.css` — Basic styling

## How to host on GitHub Pages
1. Create a new repository on GitHub (e.g., `xpath-demo-site`).
2. Upload these files to the repository root (or clone & push).
3. In the repo settings -> Pages, select branch `main` and folder `/ (root)`.
4. Save; the site will be available at `https://<your-username>.github.io/xpath-demo-site/`

## How to test with your PoC
- Baseline expecting a button with id `loginBtn` will fail on this site because the element is a `<div>`.
- Use your Selenium tests against `https://<your-username>.github.io/xpath-demo-site/` (after hosting).

## License
MIT
