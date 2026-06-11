# LocalBusiness: Restaurant

For a sit-down restaurant with a physical location, hours, menu, and reservations.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Restaurant",
  "name": "Casa Marta",
  "description": "Family-run Sicilian restaurant in the Mission, serving handmade pasta and wood-fired pizza since 2014.",
  "url": "https://casamarta.example.com",
  "telephone": "+1-415-555-0142",
  "priceRange": "$$",
  "servesCuisine": ["Italian", "Sicilian", "Mediterranean"],
  "acceptsReservations": true,
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "2418 Mission Street",
    "addressLocality": "San Francisco",
    "addressRegion": "CA",
    "postalCode": "94110",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 37.7589,
    "longitude": -122.4181
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Tuesday", "Wednesday", "Thursday"],
      "opens": "17:00",
      "closes": "22:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Friday", "Saturday"],
      "opens": "17:00",
      "closes": "23:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Sunday",
      "opens": "11:00",
      "closes": "21:00"
    }
  ],
  "menu": "https://casamarta.example.com/menu",
  "image": "https://casamarta.example.com/images/dining-room.jpg",
  "sameAs": [
    "https://www.instagram.com/casamarta_sf",
    "https://www.facebook.com/casamarta",
    "https://www.yelp.com/biz/casa-marta-san-francisco"
  ]
}
</script>
```

## Notes

- `Restaurant` is a `LocalBusiness` subtype; using the specific subtype is better than the generic.
- `openingHoursSpecification` is more precise than the legacy `openingHours` string format. Use it.
- `servesCuisine` is array-typed; lists improve relevance in food queries.
- `acceptsReservations: true` enables specific AI assistant features (Google Assistant booking, Apple Maps reserve buttons).
- `menu` should link to the actual menu page; AI engines parse it if the URL is fetchable.

## Variations

- Coffee shop: change `@type` to `CafeOrCoffeeShop`, drop `acceptsReservations`.
- Bar: change to `BarOrPub`, add `@type: Menu` for cocktail list.
- Food truck: drop `address`, add `areaServed` with the cities/neighborhoods served.
