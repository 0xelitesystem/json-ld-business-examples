# Organization: Startup or company

For a homepage or about page representing a company (not a local storefront).

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Cole Research",
  "alternateName": "Cole Research LLC",
  "description": "Independent research firm publishing pricing analyses, market studies, and tooling guides for indie SaaS founders.",
  "url": "https://example.com",
  "logo": {
    "@type": "ImageObject",
    "url": "https://example.com/logo-square-512.png",
    "width": 512,
    "height": 512
  },
  "foundingDate": "2022-08",
  "foundingLocation": {
    "@type": "Place",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Austin",
      "addressRegion": "TX",
      "addressCountry": "US"
    }
  },
  "founder": {
    "@type": "Person",
    "name": "Jane Cole",
    "url": "https://example.com/team/jane-cole"
  },
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": 4
  },
  "email": "hello@example.com",
  "telephone": "+1-512-555-0188",
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+1-512-555-0188",
    "contactType": "customer support",
    "email": "support@example.com",
    "availableLanguage": ["English", "Spanish"]
  },
  "sameAs": [
    "https://www.linkedin.com/company/cole-research",
    "https://twitter.com/cole_research",
    "https://github.com/colelab",
    "https://www.crunchbase.com/organization/cole-research"
  ],
  "knowsAbout": [
    "SaaS pricing",
    "Subscription economics",
    "Indie founder tooling"
  ]
}
</script>
```

## Notes

- `Organization` is the right type for an online-only company. `LocalBusiness` if you have a storefront customers visit.
- `foundingDate` can be just year, year-month, or full date.
- `founder` and `numberOfEmployees` help AI engines distinguish you from a one-person shop or a 1000-person enterprise.
- `contactPoint` is preferred over inline `telephone`/`email` for multi-channel support orgs.
- `sameAs` should include LinkedIn company page, Twitter, GitHub org (if any), Crunchbase. Wikipedia entry if exists.
