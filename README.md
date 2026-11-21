# Saurabh Yadav - Portfolio
Routes use hashes (#home, #work, #work-medi-user, #about, #experience, #contact), so no server rewrites are needed.

## Edit content
Everything is at the top of the `<script>` in `index.html`:
- `CONFIG`: name, links, email, resumeUrl, formEndpoint, experience, education, photo
- `PROJECTS`: each project (description, stack, capabilities, repo, accent colour)
- `MEDIA`: embedded images (base64 WebP) used by MediAdminApp, MediUserApp and Sudoku

## Add images
Projects accept `logo` and `shots:[{s:"image-url-or-data-uri",c:"alt text"}]`. On your own hosting you can use normal files, e.g. `s:"images/qr-1.webp"` (keep ~320px wide, 9:20 phone screenshots with the status bar cropped). Use `img:"images/cover.webp"` for a single full-bleed 16:10 cover instead. Portrait: `CONFIG.photo` (4:5).

## Contact form
Without `formEndpoint` the form opens Gmail / the mail app with the message pre-filled (to 09saurabh07@gmail.com).
For automatic delivery to your inbox, create a form at Formspree (or similar), then set `CONFIG.formEndpoint` to its URL. This works on your own hosting, not on claude.ai.

## Before going live
- Fill `CONFIG.experience` responsibilities and `CONFIG.education`.
- Add `resumeUrl` if you want the Resume button.
- Check each project's claims against your repos.
