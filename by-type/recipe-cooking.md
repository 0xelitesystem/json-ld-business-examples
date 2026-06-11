# Recipe: Cooking recipe

For a recipe page on a food blog or cooking site.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Recipe",
  "name": "Sicilian Pasta alla Norma",
  "description": "Eggplant, tomato, and ricotta salata pasta from Catania. Simple ingredients, deep flavor. Serves four.",
  "image": [
    "https://example.com/recipes/pasta-alla-norma/cover-16x9.jpg",
    "https://example.com/recipes/pasta-alla-norma/cover-4x3.jpg",
    "https://example.com/recipes/pasta-alla-norma/cover-1x1.jpg"
  ],
  "author": {
    "@type": "Person",
    "name": "Marta Russo",
    "url": "https://example.com/authors/marta-russo"
  },
  "datePublished": "2025-08-12",
  "dateModified": "2026-03-04",
  "prepTime": "PT15M",
  "cookTime": "PT35M",
  "totalTime": "PT50M",
  "recipeYield": "4 servings",
  "recipeCategory": "Main course",
  "recipeCuisine": "Sicilian",
  "keywords": "eggplant pasta, vegetarian, Sicilian",
  "nutrition": {
    "@type": "NutritionInformation",
    "calories": "520 calories",
    "carbohydrateContent": "78 g",
    "proteinContent": "16 g",
    "fatContent": "18 g"
  },
  "recipeIngredient": [
    "2 medium eggplants (about 700g)",
    "Sea salt for sweating eggplant",
    "Neutral oil for frying",
    "1 lb (450g) rigatoni or sedanini pasta",
    "3 tbsp extra-virgin olive oil",
    "3 cloves garlic, sliced thin",
    "1 28oz can whole peeled tomatoes",
    "10 fresh basil leaves",
    "1/2 cup grated ricotta salata",
    "Black pepper to taste"
  ],
  "recipeInstructions": [
    {
      "@type": "HowToStep",
      "name": "Sweat the eggplant",
      "text": "Cut eggplants into 3/4-inch cubes. Salt liberally and rest in a colander for 30 minutes. Pat dry with paper towels.",
      "image": "https://example.com/recipes/pasta-alla-norma/step1.jpg"
    },
    {
      "@type": "HowToStep",
      "name": "Fry the eggplant",
      "text": "Heat 1 inch of neutral oil to 350F in a deep skillet. Fry eggplant in batches until deep golden, about 4 minutes per batch. Drain on paper towels."
    },
    {
      "@type": "HowToStep",
      "name": "Make the sauce",
      "text": "In a separate pan, warm olive oil over medium-low. Add garlic, cook until fragrant but not brown, about 90 seconds. Crush tomatoes by hand into the pan. Simmer 20 minutes until thickened."
    },
    {
      "@type": "HowToStep",
      "name": "Cook the pasta",
      "text": "Bring 4 quarts of water to a boil. Salt heavily. Cook rigatoni to one minute less than package directions. Reserve 1 cup pasta water before draining."
    },
    {
      "@type": "HowToStep",
      "name": "Combine and serve",
      "text": "Toss drained pasta with sauce, fried eggplant, and torn basil. Loosen with pasta water if needed. Top each bowl with grated ricotta salata and black pepper. Serve immediately."
    }
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "ratingCount": "127"
  }
}
</script>
```

## Notes

- `prepTime`, `cookTime`, `totalTime` in ISO 8601 (PT15M = 15 minutes, PT1H30M = 1 hour 30 minutes).
- `recipeInstructions` as an array of `HowToStep` objects unlocks Google's step-by-step recipe rich results.
- Each step has its own `name` and `text`; images on steps are optional but powerful.
- `nutrition` is optional but rich-result-eligible.
- `recipeYield` accepts both "4 servings" and `4` (number); the string form is clearer.
- `aggregateRating` only with real reviews; recipes are heavily review-driven.
