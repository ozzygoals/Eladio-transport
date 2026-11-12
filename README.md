# Eladio Transport — Public Demonstration

This is an interactive **prototype**, not a real transportation booking service.

## Files
- `index.html` — Spanish-first introduction / explanation for Eladio (homepage).
- `demo.html` — interactive role switcher, weekly calendar, booking board and demonstration tools.
- `README.md` — these upload directions.

## Publish on GitHub Pages
1. Create a **public** repository at https://github.com/new (e.g. `eladio-transport`).
2. Extract the ZIP on your computer. Upload **`index.html`, `demo.html`, and `README.md` individually to the repository root** — not the parent folder or the ZIP itself. Commit your files.
3. In the repository open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**; choose **main**, folder **/(root)**, and Save.
5. Open the **Visit site** link when GitHub finishes publishing. Expected format: `https://YOUR-USERNAME.github.io/eladio-transport/`.
6. Send the **homepage URL** to Eladio. He can select **Explorar la demo**.

If this repository already has an old `index.html` version, replace it and add `demo.html`. Remove/ignore the previous `overview.html` if it exists, since this package uses the landing page as `index.html`.

## Safety and limitations
- Fictional bookings; no real shared database or secure role-based accounts.
- Changes in the demo are local to a browser, not synchronized across users.
- WhatsApp only supports manual drafting / opening links, not inbox syncing or automatic sending.
- No real fare calculation, live map routing, conflict guarantees, or payments.
- **Do not use real passenger, child, phone number, or payment data.** GitHub Pages is a public static website.

## Test before sharing
1. Open homepage in Spanish and choose the demo.
2. Try role switching (Manager/Rider/Driver) and English/Spanish language toggling.
3. In Manager, check the built-in weekly ride calendar and navigation.
4. Try a fictional booking and assignment; verify it appears in the appropriate views.
5. Reset the demo after experimentation, if needed.
