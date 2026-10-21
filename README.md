# Mind Crest Institute

Website for **Mind Crest Institute**, a coaching centre in Chapra, Bihar. The institute prepares students in Classes 11 and 12 for medical and non-medical streams, with coaching in Biology, Chemistry, Mathematics, and Physics.

The site is a [Hugo](https://gohugo.io/) project. The homepage is a single scrolling page, and longer writing lives in the blog.

## Contact

| | |
| --- | --- |
| **Institute** | Mind Crest Institute |
| **Address** | Civil Court Road, East From Municipality Chowk, Near Salempur Chowk, Chapra, Bihar 841301, India |
| **Phone** | +91 9934819234 |
| **Phone** | +91 7033376951 |
| **Website** | [mindcreststem.org](https://www.mindcreststem.org/) |

Visitors can also send a message from the contact form at the bottom of the homepage.

## What the site includes

The homepage is one scrolling page:

- **Home** — banner with a button into the introduction
- **About** — introduction and a link to the contact section
- **Calls to action** — short prompts that open the contact section
- **Testimonials** — quotes from the testimonial data file
- **Offer** — three session packages; each button opens the contact section
- **Blog** — articles under `/blog/`
- **Contact** — Chapra address, both phone numbers, and the enquiry form

The map block is turned off. French content is present in the project and is not published (`disableLanguages = ["Fr"]` in `exampleSite/config.toml`).

## Run it locally

Install [Hugo extended](https://gohugo.io/installation/) (the Netlify build uses Hugo 0.73.0), then from the repository root:

```bash
cd exampleSite
hugo server --themesDir ../..
```

Open the local URL Hugo prints, usually `http://localhost:1313/`.

To generate the static site into `exampleSite/public`:

```bash
cd exampleSite
hugo --gc --themesDir ../..
```

## Where to edit content

| What you want to change | File |
| --- | --- |
| Site title, description, copyright | `exampleSite/config.toml` |
| Address and phone numbers | `exampleSite/data/en/contact.yml` |
| Homepage introduction | `layouts/partials/feature.html` |
| Banner button | `exampleSite/data/en/banner.yml` |
| Offer cards | `exampleSite/data/en/pricing.yml` |
| Testimonials | `exampleSite/data/en/testimonial.yml` |
| Blog posts | `exampleSite/content/english/blog/` |
| Navigation labels | `exampleSite/i18n/en.yaml` |

Page sections are assembled in `layouts/index.html`. Shared chrome (header, footer, contact popup) is in `layouts/partials/`.

## Deploy

`netlify.toml` builds with:

```bash
cd exampleSite && hugo --gc --themesDir ../..
```

The published folder is `exampleSite/public`. Netlify sets `HUGO_BASEURL` to `/` and `HUGO_VERSION` to `0.73.0`.
