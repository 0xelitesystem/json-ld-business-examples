# Article: News investigation

For investigative or news journalism with multiple sources, editors, and fact-checking.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "NewsArticle",
  "headline": "How a Houston nonprofit moved $4.2M through shell donations in 2025",
  "alternativeHeadline": "Charity investigation: shell donation network exposed",
  "description": "A six-month investigation into the Texas Generosity Foundation reveals a network of 14 shell donors moving funds to politically aligned subgroups, in violation of 501(c)(3) rules.",
  "image": [
    "https://example.com/news/charity-shell/cover-16x9.jpg",
    "https://example.com/news/charity-shell/cover-4x3.jpg",
    "https://example.com/news/charity-shell/cover-1x1.jpg"
  ],
  "url": "https://example.com/news/charity-shell-donations",
  "datePublished": "2026-04-12T05:00:00-05:00",
  "dateModified": "2026-04-12T11:20:00-05:00",
  "wordCount": 4280,
  "articleSection": "Investigations",
  "isAccessibleForFree": true,
  "author": [
    {
      "@type": "Person",
      "name": "Marcus Trent",
      "url": "https://example.com/staff/marcus-trent",
      "jobTitle": "Senior Investigations Reporter",
      "sameAs": ["https://twitter.com/marcustrent", "https://muckrack.com/marcus-trent"]
    },
    {
      "@type": "Person",
      "name": "Aisha Okonkwo",
      "url": "https://example.com/staff/aisha-okonkwo",
      "jobTitle": "Investigations Reporter"
    }
  ],
  "editor": {
    "@type": "Person",
    "name": "Daniel Ward",
    "jobTitle": "Investigations Editor"
  },
  "publisher": {
    "@type": "NewsMediaOrganization",
    "name": "The Houston Ledger",
    "url": "https://example.com",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo-square-512.png"
    },
    "ethicsPolicy": "https://example.com/ethics",
    "diversityPolicy": "https://example.com/diversity",
    "missionCoveragePrioritiesPolicy": "https://example.com/coverage-priorities"
  },
  "mainEntityOfPage": {"@type": "WebPage", "@id": "https://example.com/news/charity-shell-donations"}
}
</script>
```

## Notes

- `NewsArticle` triggers Top Stories eligibility in Google. Use for journalism, not opinion.
- `author` can be an array for multi-byline pieces.
- `editor` field exists; using it matters for ethics-policy E-E-A-T.
- Multiple images for `image` covers 16:9, 4:3, and 1:1 aspect ratios as Google recommends.
- `NewsMediaOrganization` (not just `Organization`) for the publisher unlocks news-specific schema fields.
- `ethicsPolicy`, `diversityPolicy`, `missionCoveragePrioritiesPolicy` are high-trust signals specifically for news.
- `isAccessibleForFree: true` matters; paywalled content uses `hasPart` with `cssSelector` for excerpt vs full text.
