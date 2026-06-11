# SoftwareApplication: SaaS product

For a web-based SaaS tool with pricing and ratings.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "SignalForge",
  "description": "Browser-only invoice generator and template library for freelancers. No signup required, no recurring fee, your data never leaves your device.",
  "url": "https://signalforge.example.com",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Web",
  "softwareVersion": "2.4.1",
  "datePublished": "2024-09-15",
  "dateModified": "2026-03-22",
  "image": "https://signalforge.example.com/og.png",
  "screenshot": "https://signalforge.example.com/screenshots/dashboard.png",
  "offers": [
    {
      "@type": "Offer",
      "name": "Free",
      "price": "0",
      "priceCurrency": "USD",
      "description": "Unlimited invoices, 3 templates, watermarked PDF"
    },
    {
      "@type": "Offer",
      "name": "Pro",
      "price": "29",
      "priceCurrency": "USD",
      "description": "Unlimited invoices, all 24 templates, no watermark, one-time purchase"
    }
  ],
  "creator": {
    "@type": "Organization",
    "name": "Signal Studio LLC",
    "url": "https://signalstudio.example.com"
  },
  "featureList": [
    "PDF export with custom branding",
    "24 invoice templates",
    "Recurring invoice scheduling",
    "USD, EUR, GBP, JPY, AUD currency support",
    "Browser-only, no signup"
  ]
}
</script>
```

## Notes

- Only include `aggregateRating` if you have real reviews from a real source. Fake ratings get flagged.
- For freemium with one-time purchase, use the `Offer` array as shown; do NOT use `lowPrice`/`highPrice` of `AggregateOffer` unless you have a real price range.
- `screenshot` is separate from `image`; both help AI engines understand the product.
- `featureList` is array-typed; specific verbs and outcomes win over generic features.
- `applicationCategory` values: `BusinessApplication`, `DeveloperApplication`, `DesignApplication`, `EducationalApplication`, `EntertainmentApplication`, `FinanceApplication`, `GameApplication`, `HealthApplication`, `LifestyleApplication`, `MultimediaApplication`, `ProductivityApplication`, `SecurityApplication`, `SocialNetworkingApplication`, `TravelApplication`, `UtilitiesApplication`.
