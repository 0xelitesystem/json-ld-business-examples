# SoftwareApplication: Mobile app

For an iOS or Android app with download counts and real reviews.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "MobileApplication",
  "name": "QuietHours",
  "description": "Focus timer with calendar integration. Auto-blocks Slack and email notifications during scheduled deep work blocks.",
  "url": "https://quiethours.example.com",
  "applicationCategory": "ProductivityApplication",
  "operatingSystem": ["iOS 15.0+", "Android 10.0+"],
  "softwareVersion": "3.1.0",
  "datePublished": "2023-05-10",
  "dateModified": "2026-04-08",
  "downloadUrl": "https://apps.apple.com/app/quiethours/id1456789012",
  "installUrl": "https://play.google.com/store/apps/details?id=com.example.quiethours",
  "image": "https://quiethours.example.com/icon-512.png",
  "screenshot": [
    "https://quiethours.example.com/screenshots/timer.png",
    "https://quiethours.example.com/screenshots/calendar.png"
  ],
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "description": "Free with optional $4.99/month Pro subscription"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.7",
    "ratingCount": "1842",
    "bestRating": "5"
  },
  "creator": {
    "@type": "Organization",
    "name": "Quiet Tools Inc"
  }
}
</script>
```

## Notes

- `aggregateRating` here is justified because mobile apps have public review counts on the stores. Use the App Store/Play Store numbers as your truth.
- `MobileApplication` is the subtype; using it triggers mobile-specific rich results.
- List both `downloadUrl` (App Store) and `installUrl` (Play Store) when both platforms exist.
- `screenshot` accepts an array; include 2 to 4.
