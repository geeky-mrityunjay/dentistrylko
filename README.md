# Dentistry Lucknow — standalone static website

25 HTML pages, separate styles.css, content.json, app.js and 12 original local photos. No framework build, secrets or database required.

## GitHub and Vercel
1. Extract the ZIP and upload all extracted files to a new GitHub repository. Keep index.html at the repository root, with images/ alongside it.
2. In Vercel choose Add New → Project and import that repository.
3. Select framework preset Other. Leave build and install commands blank; set output directory to . if requested.
4. Deploy.

GitHub Pages also works: Settings → Pages → Deploy from a branch → select your branch and / (root). All page links and photos are relative.

## Local preview
Run `python3 -m http.server 8000` in this folder and open http://localhost:8000. Use a local server rather than double-clicking HTML: the form reads content.json.

## Editing
- index.html: home. Other HTML files: individual pages, all 15 treatments and both dentist profiles.
- styles.css: shared design and phone/tablet layouts.
- content.json: full clinic data; the form reads its WhatsApp number.
- app.js: menu, date limit and WhatsApp request preparation.
- images/: all local photographs. No Lovable image hosting dependency.
- vercel.json: static hosting settings.

Displayed text is baked into HTML. Change HTML to update visible content, and also update content.json when changing clinic details. JSON changes alone do not regenerate HTML pages. Fonts load from Google Fonts with sans-serif fallbacks.

Appointments are requests, not confirmed bookings. Patients must send the prepared WhatsApp message; the clinic confirms availability. The form does not save medical information.

Clinic hours were taken from the original footer/contact page; the original header gave different hours. Please confirm hours with the clinic before publishing.

This is a standalone HTML/CSS/JSON export, not the editable React/TanStack source in Lovable. Uploading to GitHub and publishing on Vercel remain your steps.
