# Event: In-person conference

For a multi-day in-person conference with venue, sessions, and speakers.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Event",
  "name": "Indie SaaS Summit 2026",
  "description": "Two-day conference for indie SaaS founders. 18 talks, 4 workshops, 3 networking dinners. Capped at 200 attendees.",
  "startDate": "2026-09-22T09:00:00-05:00",
  "endDate": "2026-09-23T17:00:00-05:00",
  "eventStatus": "https://schema.org/EventScheduled",
  "eventAttendanceMode": "https://schema.org/OfflineEventAttendanceMode",
  "location": {
    "@type": "Place",
    "name": "Fairmont Austin",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "101 Red River Street",
      "addressLocality": "Austin",
      "addressRegion": "TX",
      "postalCode": "78701",
      "addressCountry": "US"
    }
  },
  "image": "https://example.com/summit/2026/cover.jpg",
  "url": "https://example.com/summit/2026",
  "organizer": {
    "@type": "Organization",
    "name": "Cole Research",
    "url": "https://example.com"
  },
  "performer": [
    {
      "@type": "Person",
      "name": "Jane Cole",
      "url": "https://example.com/team/jane-cole"
    },
    {
      "@type": "Person",
      "name": "Marcus Trent",
      "url": "https://example.com/speakers/marcus-trent"
    },
    {
      "@type": "Person",
      "name": "Aisha Okonkwo",
      "url": "https://example.com/speakers/aisha-okonkwo"
    }
  ],
  "offers": [
    {
      "@type": "Offer",
      "name": "Early bird",
      "url": "https://example.com/summit/2026/tickets",
      "price": "499.00",
      "priceCurrency": "USD",
      "availability": "https://schema.org/SoldOut",
      "validFrom": "2026-01-01T00:00:00-06:00",
      "validThrough": "2026-04-30T23:59:59-05:00"
    },
    {
      "@type": "Offer",
      "name": "Regular",
      "url": "https://example.com/summit/2026/tickets",
      "price": "799.00",
      "priceCurrency": "USD",
      "availability": "https://schema.org/InStock",
      "validFrom": "2026-05-01T00:00:00-05:00",
      "validThrough": "2026-09-21T23:59:59-05:00"
    }
  ],
  "subEvent": [
    {
      "@type": "Event",
      "name": "Pre-conference founder dinner",
      "startDate": "2026-09-21T19:00:00-05:00",
      "endDate": "2026-09-21T22:00:00-05:00",
      "location": {
        "@type": "Place",
        "name": "Fairmont Garden Room",
        "address": {"@type": "PostalAddress", "addressLocality": "Austin", "addressRegion": "TX", "addressCountry": "US"}
      }
    }
  ]
}
</script>
```

## Notes

- `Place` (not `VirtualLocation`) for in-person events. Full `address` with all fields.
- Multiple `offers` for ticket tiers; each with `validFrom`, `validThrough`, and price.
- `subEvent` array for sessions, workshops, side events. Each sub-event is its own Event object.
- `performer` array for multi-speaker events. Each is a Person object with URL.
- `eventAttendanceMode: OfflineEventAttendanceMode` (or `MixedEventAttendanceMode` for hybrid).
