# Portfolio setup guide

The whole site is one file, `index.html`. All words, dates, links and images live in one block at the top of the script, called `SITE`. The layout code below it never needs editing for normal updates.

## Where things go

| To change | Edit in `SITE` |
|---|---|
| Your photograph | `person.photo` (file path or data URI) |
| TyLora, Tava Group, Tava Table links | `ventures[n].url` (buttons stay disabled until a URL is set) |
| Venture photos (shop, menu, products) | `ventures[n].image` and `imageAlt` |
| A new venture | copy one object in `ventures` and edit it |
| Timeline entries | `timeline` |
| Jobs and roles | `experience` (dates as `YYYY-MM`, empty `end` means present). Optional: `desc`, `skills`, `logo`, `image` |
| Skills and their status | `skills` (`using`, `learning` or `exploring`) |
| Certificates | `credentials` (`verifyUrl` and `image` only show when filled in) |
| Event and activity photos | `activities[n].image` |
| Projects and case notes | `projects` (categories come from `categories`) |
| Hide all "add your photo" placeholders | `showPlaceholders: false` |

## Turn on the contact form

The form validates input and blocks simple spam, but it can only send once it is pointed at a form service.

1. Create a form on a service such as Formspree or Web3Forms and copy its endpoint URL.
2. Put it in `formEndpoint`.
3. Host the site on a normal web host and send yourself a test message.

Until `formEndpoint` is set, the form says plainly that nothing was sent and offers a copy button. It never shows a success message it has not earned.

## Turn on the CV button

Upload your PDF next to `index.html` and set `cvUrl: 'cv/Md-Mizanur-Rahman-CV.pdf'`.

## Before going live on your own domain

- Add a canonical URL, `sitemap.xml` and `robots.txt` once the domain is chosen.
- Add an Open Graph preview image (`og:image`) to the head.
- Add analytics only after you have a consent banner configured.
- This version is not connected to a CMS, analytics service or database.
