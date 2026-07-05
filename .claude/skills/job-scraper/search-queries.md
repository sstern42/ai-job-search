# Search Queries for Job Scraper

<!-- SETUP: Customized for UK-based search. The framework's built-in portal CLI tools (jobbank-search,
     jobdanmark-search, jobindex-search, jobnet-search) are Denmark-specific and not used here. Search
     relies on the country-agnostic linkedin-search tool plus Google site: searches for Indeed. -->

## Search Sites

Primary (UK job market):
- **linkedin-search** (`.agents/skills/linkedin-search`) - country-agnostic LinkedIn jobs-guest tool; use `-l "London, England, United Kingdom"` or `-l "Remote"`
- **indeed.co.uk** - via Google `site:` searches (no dedicated CLI tool; use WebSearch/Google site-search)

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Each query should be combined with location terms ("London", "Remote", "Hybrid") where the site supports it.

### Priority 1: Product Analyst

These match the strongest and most desired career direction, with emphasis on A/B testing and experimentation.

```
linkedin-search "Product Analyst" -l "London, England, United Kingdom"
linkedin-search "Product Analyst" -l "Remote"
site:indeed.co.uk "Product Analyst" "A/B testing" London
site:linkedin.com/jobs "Product Analyst" "experimentation" London
```

### Priority 2: Experimentation & A/B Testing

These match the domain expertise directly: nine years of experimentation analysis at scale.

```
linkedin-search "Experimentation Manager" -l "London, England, United Kingdom"
linkedin-search "Experimentation Analyst" -l "Remote"
site:indeed.co.uk "Experimentation Manager" London OR Remote
site:indeed.co.uk "A/B testing" analyst London
```

### Priority 3: Adjacent Roles

Adjacent roles to widen the search net without moving off the core direction.

```
linkedin-search "Senior Data Analyst" "experimentation" -l "London, England, United Kingdom"
linkedin-search "Growth Analyst" -l "London, England, United Kingdom"
site:indeed.co.uk "Data Analyst" "A/B testing" London
```

### Priority 4: Broader Product / Growth

Wider net for roles that draw on the founder/full-stack background as a differentiator.

```
linkedin-search "Product Manager" "data-driven" -l "London, England, United Kingdom"
site:indeed.co.uk "Growth" "Product Analyst" Remote
```

## Location Filter

When evaluating results, verify the job location is within reasonable commute distance from Aldersbrook, London E12, or is remote. Define acceptable areas:
- London and Greater London: PASS
- Remote (UK-based or fully remote): PASS
- Hybrid roles requiring occasional office attendance in London: PASS
- Outside London requiring full relocation: FAIL (deal-breaker)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
