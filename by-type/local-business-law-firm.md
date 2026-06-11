# LocalBusiness: Law firm

For a law practice with named attorneys and practice areas.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "Marquez & Hale LLP",
  "description": "Boutique employment law firm representing employees in wrongful termination, discrimination, and wage and hour disputes throughout California.",
  "url": "https://marquezhale.example.com",
  "telephone": "+1-213-555-0167",
  "priceRange": "Contingency and hourly",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "445 South Figueroa Street Suite 2900",
    "addressLocality": "Los Angeles",
    "addressRegion": "CA",
    "postalCode": "90071",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 34.0522,
    "longitude": -118.2563
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
    "opens": "09:00",
    "closes": "18:00"
  },
  "areaServed": [
    {"@type": "State", "name": "California"}
  ],
  "knowsAbout": [
    "Employment law",
    "Wrongful termination",
    "Workplace discrimination",
    "Wage and hour disputes",
    "Sexual harassment claims"
  ],
  "employee": [
    {
      "@type": "Person",
      "name": "Sofia Marquez",
      "jobTitle": "Founding Partner",
      "url": "https://marquezhale.example.com/attorneys/sofia-marquez",
      "alumniOf": [
        "UCLA School of Law",
        "Stanford University"
      ],
      "sameAs": [
        "https://www.linkedin.com/in/sofia-marquez-esq",
        "https://www.calbar.ca.gov/member/178432"
      ]
    },
    {
      "@type": "Person",
      "name": "David Hale",
      "jobTitle": "Founding Partner",
      "url": "https://marquezhale.example.com/attorneys/david-hale",
      "alumniOf": "Berkeley Law"
    }
  ],
  "sameAs": [
    "https://www.linkedin.com/company/marquez-hale-llp",
    "https://www.avvo.com/attorneys/marquez-hale.html"
  ]
}
</script>
```

## Notes

- `LegalService` is the right specific type; `Attorney` is for individual attorneys (use under `employee`).
- `knowsAbout` as an array gives AI engines a topic-cluster for "best [practice area] lawyer in [city]" queries.
- State bar profile in `sameAs` is high E-E-A-T (the official credential registry).
- `areaServed` matters for legal because lawyers are licensed by jurisdiction.
