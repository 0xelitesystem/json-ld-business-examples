# LocalBusiness: Dentist

For a dental practice with licensed practitioners, services, and insurance accepted.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Dentist",
  "name": "Cole Dental Group",
  "description": "Family and cosmetic dentistry in downtown Austin. Same-day crowns, Invisalign provider, accepts most PPO insurance.",
  "url": "https://coledental.example.com",
  "telephone": "+1-512-555-0118",
  "priceRange": "$$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "1200 Congress Avenue Suite 400",
    "addressLocality": "Austin",
    "addressRegion": "TX",
    "postalCode": "78701",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 30.2722,
    "longitude": -97.7431
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday"],
      "opens": "08:00",
      "closes": "17:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Friday",
      "opens": "08:00",
      "closes": "14:00"
    }
  ],
  "medicalSpecialty": ["CosmeticDentistry", "GeneralDentistry"],
  "availableService": [
    {"@type": "MedicalProcedure", "name": "Teeth cleaning"},
    {"@type": "MedicalProcedure", "name": "Invisalign treatment"},
    {"@type": "MedicalProcedure", "name": "Same-day crowns"},
    {"@type": "MedicalProcedure", "name": "Cosmetic veneers"}
  ],
  "employee": [{
    "@type": "Person",
    "name": "Dr. Jane Cole, DDS",
    "url": "https://coledental.example.com/team/jane-cole",
    "jobTitle": "Founder, Lead Dentist",
    "alumniOf": "University of Texas School of Dentistry"
  }],
  "image": "https://coledental.example.com/images/reception.jpg",
  "sameAs": [
    "https://www.google.com/maps/place/cole-dental",
    "https://www.yelp.com/biz/cole-dental-austin",
    "https://healthgrades.com/dentist/dr-jane-cole"
  ]
}
</script>
```

## Notes

- `Dentist` is a `MedicalBusiness` and `LocalBusiness` subtype. Using it unlocks medical-specific fields.
- `employee` with individual `Person` schema gives the practitioners their own E-E-A-T weight.
- `medicalSpecialty` uses enumerated values from Schema.org; "CosmeticDentistry" is the official enum.
- `availableService` lists discrete procedures; AI engines surface specific service queries.
- `alumniOf` on the practitioner Person object is high E-E-A-T signal for medical pros.
