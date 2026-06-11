# Article: Blog post

For a typical company blog post or independent blog post.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",
  "headline": "Why BYOK pricing wins for solo SaaS buyers",
  "description": "Cost analysis comparing BYOK to bundled SaaS pricing for indie builders, with data from a 2026 study of 240 solo founders.",
  "image": "https://example.com/posts/byok-pricing/cover.jpg",
  "url": "https://example.com/posts/byok-pricing-wins",
  "datePublished": "2026-03-15T08:00:00-07:00",
  "dateModified": "2026-04-20T14:30:00-07:00",
  "wordCount": 1840,
  "articleSection": "Pricing analysis",
  "keywords": ["BYOK", "SaaS pricing", "indie founders", "API cost"],
  "inLanguage": "en-US",
  "author": {
    "@type": "Person",
    "name": "Jane Cole",
    "url": "https://example.com/authors/jane-cole",
    "image": "https://example.com/authors/jane-cole.jpg",
    "jobTitle": "Research Lead",
    "sameAs": [
      "https://www.linkedin.com/in/janecole",
      "https://github.com/janecole",
      "https://twitter.com/jane_cole"
    ]
  },
  "publisher": {
    "@type": "Organization",
    "name": "Cole Research",
    "url": "https://example.com",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo-square-512.png",
      "width": 512,
      "height": 512
    }
  },
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://example.com/posts/byok-pricing-wins"
  }
}
</script>
```

## Notes

- `BlogPosting` is the subtype of `Article` for blog posts specifically. `NewsArticle` is for journalism.
- `datePublished` and `dateModified` in ISO 8601 with timezone offset. Date-only formats validate but ISO with offset is better.
- `author` MUST be a `Person` object with at least `name` and `url`. String-only authors are deprecated.
- Logo MUST be square or close to it, minimum 112x112, ideally 512x512.
- `mainEntityOfPage` with `@id` matching the URL prevents canonical confusion.
- `wordCount` is optional but helps AI engines gauge depth without parsing the body.
