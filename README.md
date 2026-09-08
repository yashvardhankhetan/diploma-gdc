# Putting the Diploma GDC pages on dpseven.com

This folder is ready to upload as-is. It gives you:

- https://dpseven.com/ — a one-paragraph holding page (replace it when the real site is built)
- https://dpseven.com/diploma-gdc/ — the app's support page (App Store "Support URL")
- https://dpseven.com/diploma-gdc/privacy.html — the privacy policy (App Store "Privacy Policy URL")

Cloudflare Pages hosts a static folder like this for free. No code, no build step.

## Support address

The pages use diplomagdc@gmail.com. If it ever changes, edit both files here and in `gdc/web/`, then push.

## Steps in the Cloudflare dashboard (about five minutes)

1. Sign in at https://dash.cloudflare.com and open **Workers & Pages**.
2. Click **Create** → **Pages** → **Upload assets**.
3. Project name: `dpseven`. Click **Create project**.
4. Drag this whole `site-upload` folder into the upload box (or click to select it).
   Make sure the upload shows `index.html` and a `diploma-gdc` folder, then **Deploy site**.
5. When it finishes, open **Custom domains** → **Set up a custom domain**, type `dpseven.com`
   and confirm. Because the domain is already on this Cloudflare account, the DNS record
   is created for you. Repeat for `www.dpseven.com` if you want that to work too.
6. Wait a few minutes, then open https://dpseven.com/diploma-gdc/ in a browser.

## If you would rather have your other Claude account do it

Paste this to it:

> I have a Cloudflare Pages static site to publish. Create a Pages project called
> `dpseven` using direct upload, deploy the folder I attach, and attach the custom
> domain `dpseven.com` (and `www.dpseven.com`) to it. The domain is already in this
> Cloudflare account. Tell me the final URLs of `/diploma-gdc/` and
> `/diploma-gdc/privacy.html`.

and attach a zip of this folder (right-click the `site-upload` folder in Finder →
Compress).

## Updating later

Any time the pages change, go to the `dpseven` project → **Create new deployment** →
upload the folder again. Old URLs keep working.

## Then, in App Store Connect

App → App Information:
- Support URL: `https://dpseven.com/diploma-gdc/`
- Privacy Policy URL: `https://dpseven.com/diploma-gdc/privacy.html`
