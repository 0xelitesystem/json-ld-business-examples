# Product: Physical good

For a physical product in an ecommerce store.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Manhattan Portage Empire Backpack (Black)",
  "description": "Heavy-duty waterproof courier backpack made from 1000-denier Cordura nylon. 22L capacity. Padded 15-inch laptop sleeve. Lifetime warranty.",
  "image": [
    "https://example.com/products/empire-backpack-1.jpg",
    "https://example.com/products/empire-backpack-2.jpg",
    "https://example.com/products/empire-backpack-3.jpg"
  ],
  "brand": {
    "@type": "Brand",
    "name": "Manhattan Portage"
  },
  "sku": "MP-EMP-22L-BLK",
  "gtin13": "0843827019451",
  "color": "Black",
  "material": "1000-denier Cordura nylon",
  "weight": {
    "@type": "QuantitativeValue",
    "value": "1.4",
    "unitCode": "KGM"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/products/empire-backpack",
    "price": "189.00",
    "priceCurrency": "USD",
    "priceValidUntil": "2026-12-31",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition",
    "seller": {
      "@type": "Organization",
      "name": "Bag Outfitters"
    },
    "shippingDetails": {
      "@type": "OfferShippingDetails",
      "shippingRate": {
        "@type": "MonetaryAmount",
        "value": "0",
        "currency": "USD"
      },
      "deliveryTime": {
        "@type": "ShippingDeliveryTime",
        "businessDays": {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
        },
        "transitTime": {
          "@type": "QuantitativeValue",
          "minValue": 2,
          "maxValue": 5,
          "unitCode": "DAY"
        }
      }
    }
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.6",
    "reviewCount": "284",
    "bestRating": "5"
  }
}
</script>
```

## Notes

- `gtin13` (or `gtin8`, `gtin12`, `gtin14`, `mpn`) is required for Google Shopping eligibility.
- `priceValidUntil` is required for the price snippet in Google search results.
- `shippingDetails` is required for free-shipping callouts. Without it Google flags the page.
- `availability` uses the schema.org URL form: `https://schema.org/InStock`, `OutOfStock`, `PreOrder`, `LimitedAvailability`, `Discontinued`.
- `aggregateRating` only with real review counts. `reviewCount` and `ratingCount` are different fields; `reviewCount` = number of text reviews, `ratingCount` = number of star ratings including no-text.
