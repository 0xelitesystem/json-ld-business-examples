# structured-data-examples

Real-world JSON-LD schema examples for every business type. Production-grade, ready to study and adapt.

## What this repo contains

19 fully-worked JSON-LD examples covering the schema types most sites need, plus a best-practices guide and a common-mistakes catalog.

## Files

```
by-type/
  local-business-restaurant.md
  local-business-dentist.md
  local-business-law-firm.md
  software-saas.md
  software-mobile-app.md
  article-blog-post.md
  article-news-investigation.md
  person-founder.md
  person-author.md
  product-physical.md
  product-digital.md
  faq-page-saas.md
  course-online.md
  video-tutorial.md
  organization-startup.md
  event-webinar.md
  event-conference.md
  recipe-cooking.md
  review-product.md
best-practices.md
common-mistakes.md
```

## How to use

1. Find the type closest to your use case in `by-type/`.
2. Copy the JSON-LD block.
3. Replace the example values with your real values.
4. Validate at [Google Rich Results Test](https://search.google.com/test/rich-results) and [Schema.org validator](https://validator.schema.org/).
5. Drop the validated block inside `<script type="application/ld+json">` in your `<head>`.

## Why "real-world" examples

Most schema docs show minimal examples that validate but don't help your page. These examples include:

- Every field that meaningfully helps AI engines, not just the required minimum
- `sameAs` arrays with real-looking profile URLs so you remember to add yours
- `author` as a full `Person` object, not just a string
- Properly nested `address`, `geo`, `offers`, `provider`, `instructor` objects
- Multiple examples for variant scenarios (online vs in-person event, physical vs digital product)

## Pairs with

- [schema-markup-generator](https://github.com/0xelitesystem/schema-markup-generator): generate from a form, validate before publishing
- [e-e-a-t-auditor](https://github.com/0xelitesystem/e-e-a-t-auditor): audit your live pages for the schema you put in
- [geo-audit-checklist](https://github.com/0xelitesystem/geo-audit-checklist): the structured data section uses these examples as templates

## License

MIT. Free to copy, adapt, ship.
