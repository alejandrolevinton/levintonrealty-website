# Levinton Realty — website

The new levintonrealty.com: a one-page site (Home, Services, About, Our Office, Find a Property, Contact) in plain HTML, ready for Netlify. There is no build step and nothing to install.

```
index.html        the homepage (English)
thanks.html       page shown after someone sends a form (English)
es/index.html     the homepage in Spanish
es/gracias.html   thank-you page in Spanish
privacy.html      privacy policy (English)
es/privacidad.html  privacy policy (Spanish)
404.html          page shown when an address doesn't exist (English and Spanish)
sitemap.xml       list of pages for Google (both languages)
robots.txt        tells search engines where the sitemap is
favicon.ico       browser-tab icon
netlify.toml      Netlify settings (caching, redirects from the old Squarespace addresses)
assets/           logo, hero photo, favicon, link-preview image (share.jpg)
```

## Publish it with Netlify (one time)

1. Sign in at app.netlify.com with GitHub.
2. Click **Add new site → Import an existing project → GitHub** and pick `levintonrealty-website`.
3. Leave the build command empty and the publish directory as `.`, then click **Deploy**.
4. Netlify gives you a temporary address like `something.netlify.app`. Check the site there first.

From then on, every change committed to this repository goes live on Netlify automatically.

## Turn on the forms

The "Start your search" and "Let's talk" forms use Netlify Forms.

1. In Netlify, open the site and go to **Forms**. Turn on **form detection** if Netlify asks you to, then redeploy once (**Deploys → Trigger deploy**).
2. Four forms will appear: `property-request` and `contact` (English pages), and `property-request-es` and `contact-es` (Spanish pages). Each language has its own form name so visitors get the thank-you page in their language.
3. Under **Forms → Form notifications**, add an email notification to info@levintonrealty.com for **any form** (or one for each of the four forms) so new messages reach your inbox.

## Point levintonrealty.com to Netlify

Only do this once you're happy with the site on the temporary address. Until then the domain keeps pointing to Squarespace.

1. In Netlify, go to **Domain management → Add a domain** and enter `levintonrealty.com`.
2. Netlify shows the DNS records to set. Change them wherever the domain is managed (Squarespace Domains if you bought it there).
3. Netlify turns on HTTPS automatically once the domain points to it. After that you can cancel the Squarespace website plan, but keep the domain registration.

## Editing text

The English and Spanish pages are separate files. When you change wording on one, make the same change on the other (`index.html` and `es/index.html`).

## Changing photos

The hero photo is `assets/hero-2400.jpg`, with a smaller `assets/hero-1200.jpg` for phones. To change it, open the `assets` folder here, click **Add file → Upload files**, and upload new files with the same names.
