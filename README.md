# Yummly (yummly)

Yummly is a recipe and food discovery platform ([yummly.com](https://www.yummly.com)) offering semantic and visual recipe search, personalized recommendations, shopping lists, and guided cooking. Founded in 2009 in Redwood City, CA, Yummly was acquired by **Whirlpool Corporation** in May 2017 and operated as a wholly owned subsidiary tied to Whirlpool's smart-kitchen strategy.

> **API status: DEPRECATED.** Yummly historically ran a well-known public Recipe API at `developer.yummly.com` (REST base `http://api.yummly.com/v1/api`). That developer program stopped accepting new signups and was wound down (commonly cited end date of **September 30, 2019**). As of this cataloging (2026-07-03), the `developer.yummly.com` hostname does not resolve and the `api.yummly.com` endpoints are unreachable. **There is no publicly available Yummly developer API accepting new registrations today.** The APIs documented here are recorded as historical / modeled for archival and migration reference only.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/yummly/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/yummly/refs/heads/main/apis.yml)

## Tags

- Recipes
- Food
- Cooking
- Recipe Search
- Food Discovery
- Deprecated
- Historical

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## Historical APIs (Deprecated)

The following three logical surfaces made up the historical Yummly Recipe API. All were request/response REST over HTTP, returned JSON, and were authenticated with `_app_id` and `_app_key` query parameters. **None are live.**

### Yummly Recipe Search API (Historical)

`GET http://api.yummly.com/v1/api/recipes` — returned recipe matches with optional filters combined via AND: free-text query (`q`), `maxResult`/`start` paging, and facets such as `allowedIngredient`/`excludedIngredient`, `allowedCuisine`, `allowedCourse`, `allowedAllergy`, `allowedDiet`, `allowedHoliday`, `maxTotalTimeInSeconds`, and nutrition/taste ranges.

- **Historical Documentation:** [https://developer.yummly.com/documentation.html](https://developer.yummly.com/documentation.html)

### Yummly Recipe Details API (Historical)

`GET http://api.yummly.com/v1/api/recipe/{recipe-id}` — returned the full detail for a single recipe by its Yummly recipe id: ingredient lines, nutrition estimates, flavor/taste profile, total cooking time, source attribution, and image URLs.

- **Historical Documentation:** [https://developer.yummly.com/documentation.html](https://developer.yummly.com/documentation.html)

### Yummly Metadata API (Historical)

`GET http://api.yummly.com/v1/api/metadata/{key}` — returned the controlled vocabularies used to build search filters. Keys included `ingredient`, `allergy`, `diet`, `cuisine`, `course`, `holiday`, `technique`, `source`, `brand`, and `restriction`.

- **Historical Documentation:** [https://developer.yummly.com/documentation.html](https://developer.yummly.com/documentation.html)

## Historical Plans

Before the developer program was retired, Yummly offered (all requiring Yummly Attribution):

| Plan | Allowance | Overage |
| --- | --- | --- |
| Free (Evaluation) | ~500 calls total | — |
| Lite | ~250,000 calls/month (14-day trial) | ~$0.002 per additional call |
| Plus | ~4,000,000 calls/month (14-day trial) | ~$0.001 per additional call |
| Custom / Enterprise | negotiated | from ~$75,000/year |

See [`plans/yummly-plans-pricing.yml`](plans/yummly-plans-pricing.yml) and [`rate-limits/yummly-rate-limits.yml`](rate-limits/yummly-rate-limits.yml). These figures are historical and no longer offered.

## Migration Notes

Developers who relied on the Yummly API were, by community consensus, pointed to replacements such as EatID and RapidAPI-hosted recipe APIs after Yummly's program shut down. No first-party Yummly replacement API has been published.

## Common Properties

- [Website](https://www.yummly.com)
- [LinkedIn](https://www.linkedin.com/company/yummly)
- [Documentation (historical)](https://developer.yummly.com/documentation.html)
- [Plans](plans/yummly-plans-pricing.yml)
- [Rate Limits](rate-limits/yummly-rate-limits.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
