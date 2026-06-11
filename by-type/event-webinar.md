# Event: Online webinar

For a one-time or recurring online webinar.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Event",
  "name": "Q2 BYOK Pricing Audit Workshop",
  "description": "Live 90-minute workshop walking through three real BYOK pricing audits with the founders. Q&A throughout. Recording sent to all registrants.",
  "startDate": "2026-06-15T14:00:00-07:00",
  "endDate": "2026-06-15T15:30:00-07:00",
  "eventStatus": "https://schema.org/EventScheduled",
  "eventAttendanceMode": "https://schema.org/OnlineEventAttendanceMode",
  "location": {
    "@type": "VirtualLocation",
    "url": "https://example.com/workshops/q2-pricing-audit/join"
  },
  "image": "https://example.com/workshops/q2-pricing-audit-cover.jpg",
  "url": "https://example.com/workshops/q2-pricing-audit",
  "organizer": {
    "@type": "Organization",
    "name": "Cole Research",
    "url": "https://example.com"
  },
  "performer": {
    "@type": "Person",
    "name": "Jane Cole",
    "url": "https://example.com/team/jane-cole"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/workshops/q2-pricing-audit#register",
    "price": "49.00",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock",
    "validFrom": "2026-04-15T00:00:00-07:00"
  }
}
</script>
```

## Notes

- `eventAttendanceMode` values: `OnlineEventAttendanceMode`, `OfflineEventAttendanceMode`, `MixedEventAttendanceMode`.
- For online events, `location` is `VirtualLocation` with a `url` to the join link or event page.
- `eventStatus` values: `EventScheduled`, `EventPostponed`, `EventRescheduled`, `EventCancelled`, `EventMovedOnline`.
- When postponing, keep the original schema and add `previousStartDate`; do NOT delete the original event.
- `performer` for talks/workshops; `attendee` is for invite-only events.
- Always set `validFrom` on `offers` so Google knows when tickets started selling.
