# Course: Online course

For a self-paced or scheduled online course with named instructor.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Course",
  "name": "BYOK SaaS Pricing in 14 Days",
  "description": "Two-week intensive course teaching the BYOK pricing model for indie SaaS founders. Includes 14 daily lessons, 6 pricing audit worksheets, and a private community.",
  "url": "https://example.com/courses/byok-pricing",
  "image": "https://example.com/courses/byok-pricing/cover.jpg",
  "inLanguage": "en",
  "courseCode": "BYOK-2026-Q2",
  "educationalLevel": "Intermediate",
  "audience": {
    "@type": "EducationalAudience",
    "educationalRole": "indie SaaS founders"
  },
  "provider": {
    "@type": "Organization",
    "name": "Cole Research",
    "url": "https://example.com",
    "sameAs": [
      "https://www.linkedin.com/company/cole-research",
      "https://twitter.com/cole_research"
    ]
  },
  "instructor": {
    "@type": "Person",
    "name": "Jane Cole",
    "url": "https://example.com/team/jane-cole",
    "jobTitle": "Founder and Lead Researcher",
    "sameAs": ["https://www.linkedin.com/in/janecole"]
  },
  "hasCourseInstance": [
    {
      "@type": "CourseInstance",
      "courseMode": "online",
      "startDate": "2026-06-01",
      "endDate": "2026-06-14",
      "courseSchedule": {
        "@type": "Schedule",
        "duration": "PT45M",
        "repeatFrequency": "Daily",
        "repeatCount": 14
      },
      "instructor": {
        "@type": "Person",
        "name": "Jane Cole"
      },
      "location": {
        "@type": "VirtualLocation",
        "url": "https://example.com/courses/byok-pricing/live"
      }
    }
  ],
  "offers": {
    "@type": "Offer",
    "price": "299.00",
    "priceCurrency": "USD",
    "category": "Paid",
    "url": "https://example.com/courses/byok-pricing#enroll"
  }
}
</script>
```

## Notes

- `Course` schema needs at least one `CourseInstance` to be eligible for Google course rich results.
- `courseMode` values: `online`, `onsite`, `blended`.
- `startDate`/`endDate` on the instance, not the course itself; courses can have many instances.
- `instructor` belongs on both the Course and the CourseInstance (since instructors can vary by instance).
- `Schedule` with `duration` (ISO 8601 like PT45M = 45 minutes) and `repeatCount` is the modern way; older `numberOfDays` is deprecated.
- For self-paced async courses, omit `Schedule` and just use `courseMode: online` with no startDate.
