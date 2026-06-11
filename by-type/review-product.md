# Review: Product review

For a single review of a product, service, business, book, movie, etc.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Review",
  "itemReviewed": {
    "@type": "SoftwareApplication",
    "name": "SignalForge",
    "url": "https://signalforge.example.com",
    "applicationCategory": "BusinessApplication",
    "operatingSystem": "Web"
  },
  "reviewRating": {
    "@type": "Rating",
    "ratingValue": "4",
    "bestRating": "5",
    "worstRating": "1"
  },
  "author": {
    "@type": "Person",
    "name": "Marcus Trent",
    "url": "https://example.com/staff/marcus-trent"
  },
  "datePublished": "2026-04-08",
  "reviewBody": "SignalForge gets the core invoice-generation workflow right: open a tab, fill in the fields, download a clean PDF, no login wall. The 24 Pro templates are genuinely varied (I counted 9 distinct visual styles, not just color swaps). Two issues kept this from 5 stars: the multi-tax feature is Pro-only, which feels like an upsell rather than a genuine feature gate, and the iPad version misaligns the logo upload preview in Safari. For freelancers in a single-tax jurisdiction the free tier is enough. For agencies juggling combined federal/state tax, the Pro upgrade pays for itself the first invoice.",
  "publisher": {
    "@type": "Organization",
    "name": "The Houston Ledger"
  }
}
</script>
```

## Notes

- `itemReviewed.@type` matches the type of thing being reviewed: `Product`, `SoftwareApplication`, `Book`, `Movie`, `LocalBusiness`, `Restaurant`, etc.
- Include the full `itemReviewed` object so the review is connected to the entity, not just the name.
- `reviewBody` 100 to 300 words. Specific observations, not opinions.
- `bestRating` and `worstRating` clarify the scale (4/5 vs 4/10 are very different signals).
- For multi-reviewer roundups, use multiple `Review` objects, each with its own author.
- Do not generate fake reviews. Search engines and AI engines flag patterns.
