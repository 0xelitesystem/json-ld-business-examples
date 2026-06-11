# Person: Blog author

For a contributor's author page on a multi-author publication.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Marcus Trent",
  "url": "https://example.com/authors/marcus-trent",
  "image": "https://example.com/authors/marcus-trent-photo.jpg",
  "jobTitle": "Senior Investigations Reporter",
  "description": "Investigative journalist covering nonprofit finance and political donations. Reporter at The Houston Ledger since 2021. National Magazine Award finalist 2024.",
  "worksFor": {
    "@type": "NewsMediaOrganization",
    "name": "The Houston Ledger",
    "url": "https://example.com"
  },
  "alumniOf": {
    "@type": "CollegeOrUniversity",
    "name": "Columbia Journalism School"
  },
  "award": [
    "National Magazine Award finalist (2024)",
    "Texas APME First Place Investigative Reporting (2023)"
  ],
  "knowsAbout": [
    "Nonprofit financial reporting",
    "Political donation transparency",
    "501(c)(3) compliance",
    "Public records investigation"
  ],
  "sameAs": [
    "https://twitter.com/marcustrent",
    "https://www.linkedin.com/in/marcus-trent-reporter",
    "https://muckrack.com/marcus-trent"
  ]
}
</script>
```

## Notes

- `award` field is array-typed; useful for credentialed authors (journalists, academics, attorneys, doctors).
- `Muck Rack` is the journalist-specific registry, useful in `sameAs` for reporters.
- For doctors use `medicalSpecialty`; for attorneys use bar association URLs in `sameAs`.
- A short, fact-specific bio in `description` beats a long flowery one.
