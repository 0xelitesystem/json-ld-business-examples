# Person: Startup founder

For a startup founder's personal page or About page, when the founder is the public face of the brand.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Jane Cole",
  "givenName": "Jane",
  "familyName": "Cole",
  "url": "https://janecole.example.com",
  "image": "https://janecole.example.com/photo.jpg",
  "jobTitle": "Founder and CEO",
  "description": "Founder of Cole Research. Twelve years analyzing SaaS pricing. Previously a consultant at McKinsey focused on B2B subscription models.",
  "worksFor": {
    "@type": "Organization",
    "name": "Cole Research",
    "url": "https://example.com"
  },
  "alumniOf": [
    {
      "@type": "CollegeOrUniversity",
      "name": "Stanford University",
      "url": "https://www.stanford.edu"
    },
    {
      "@type": "CollegeOrUniversity",
      "name": "INSEAD",
      "url": "https://www.insead.edu"
    }
  ],
  "knowsAbout": [
    "SaaS pricing strategy",
    "B2B subscription economics",
    "Indie founder finance",
    "API-based BYOK pricing models"
  ],
  "knowsLanguage": ["English", "Spanish"],
  "sameAs": [
    "https://www.linkedin.com/in/janecole",
    "https://github.com/janecole",
    "https://twitter.com/jane_cole",
    "https://www.crunchbase.com/person/jane-cole",
    "https://en.wikipedia.org/wiki/Jane_Cole"
  ]
}
</script>
```

## Notes

- `sameAs` is the single most important field for Person schema; it links the named entity to the rest of the public web.
- Include LinkedIn, GitHub (for technical founders), Twitter/X, Crunchbase, and Wikipedia if you have an entry.
- `alumniOf` adds depth; named institutions give AI engines verifiable credentials to anchor to.
- `knowsAbout` (array) is the topic-cluster signal for "expert in X" queries.
- Avoid filler like "passionate about" or "thought leader" in `description`. Use specific years, specific roles.
- A `Person` block on the founder's page combined with `Person` as `author` in Article schema unifies the identity across the site.
