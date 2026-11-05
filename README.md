# IdealForms

Static marketing site for IdealForms, a done-for-you online forms service.
No build step: one `index.html` plus a favicon. Vercel serves it as-is.

## Deploy

1. Create a new GitHub repo and copy these files into the root.
2. In Vercel, choose **Add New > Project**, import the repo.
3. Framework preset: **Other**. Leave the build command and output directory empty.
4. Deploy, then add your domain under **Settings > Domains**.

## Connect the "Start your form" section to Tally

The contact section shows a placeholder form until you add a Tally form ID.

1. Build the intake form in Tally and publish it.
2. Copy the ID from its share link (`tally.so/r/ABC123` means the ID is `ABC123`).
3. In `index.html`, search for `TALLY_FORM_ID` and paste it between the quotes.

The page then loads Tally's embed script and swaps the placeholder for your live form.

## Editing

- **Pricing:** search for `id="pricing"`. The quick-quote widget in the hero has its own prices in the `result()` function in the script at the bottom, so update both together.
- **Examples:** search for `id="examples"`. Each `<article class="ex">` is one card. Change the tag text from `COMING SOON` to `LIVE` and point the link at the real form.
- **Colours and fonts:** the tokens at the top of the `<style>` block. The page follows the visitor's light or dark setting.
