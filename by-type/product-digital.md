# Product: Digital product (ebook, course, template pack)

For digital goods sold via download.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Indie Founder's Pricing Playbook (2026 edition)",
  "description": "240-page PDF playbook with 27 worked pricing examples from real indie SaaS launches. Includes pricing audit spreadsheet and 12 email templates.",
  "image": "https://example.com/products/pricing-playbook-cover.png",
  "brand": {
    "@type": "Brand",
    "name": "Cole Research"
  },
  "category": "Digital download",
  "sku": "PB-2026-PDF",
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/products/pricing-playbook",
    "price": "49.00",
    "priceCurrency": "USD",
    "priceValidUntil": "2026-12-31",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition",
    "seller": {
      "@type": "Organization",
      "name": "Cole Research"
    }
  },
  "isRelatedTo": [
    {
      "@type": "Product",
      "name": "Indie Founder's Marketing Playbook",
      "url": "https://example.com/products/marketing-playbook"
    }
  ]
}
</script>
```

## Notes

- No physical-product fields (`weight`, `gtin`, `color`, `shippingDetails`).
- `category` short string helps with classification.
- `isRelatedTo` for cross-sell products.
- Do not invent `aggregateRating` for a new product launch. Add it after real reviews exist.
