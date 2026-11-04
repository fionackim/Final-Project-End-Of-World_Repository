# Do “End of the World” Searches Rise Around Major News Events?

## Research question

Do Google searches in the United States for “end of the world” rise around major news events?

## Project overview

This project uses Google Trends to examine monthly search interest around four events:

- The World Health Organization’s COVID-19 pandemic announcement on March 11, 2020
- Russia’s full-scale invasion of Ukraine on February 24, 2022
- The October 7, 2023 attack on Israel
- The 2024 U.S. presidential election on November 5, 2024

The project looks for changes in search interest around these events. It can show that search interest and events happened around the same time, but it cannot show that an event caused people to search.

## Data

- **Source:** [Google Trends Explore](https://trends.google.com/trends/explore)
- **Search term:** “end of the world”
- **Location:** United States
- **Category:** All categories
- **Time period:** January 2020–November 2026
- **Frequency:** Monthly
- **Records:** 83 monthly observations
- **Collected:** October 25, 2026

The November 2026 value is partial because the data was collected during that month.

Google Trends scores are normalized values from 0 to 100. They show relative search interest for the selected location and time period, not the number of searches.

## Collection and cleaning

I downloaded the chart data as a CSV from Google Trends Explore. The exported file has a month field and a search-interest score. The cleaning notebook will convert the month to a date, convert scores to numbers, check for missing values, and save a small cleaned sample for this repository.

The full downloaded CSV will stay local. This repository will contain the collection and cleaning code plus a small sample of the cleaned data.

## Analysis plan

For the Ukraine invasion, the October 2023 attack, and the 2024 election, I will compare search interest during the event month and following month with the three months before the event.

For COVID19, I will compare March and April 2020 with January and February 2020. The data begins in January 2020, so this comparison has only two months before the event.

Because the data is monthly, it cannot isolate the exact day of a search. Event/month scores may include searches from both before and after the event.

## Data dictionary

| Field | Meaning |
|---|---|
| `month` | Month represented by the observation |
| `interest_score` | Google Trends relative search interest score from 0 to 100 |

## Limitations

Google Trends uses aggregated and sampled search data. A higher score indicates greater relative interest, not a number of searches or a count of people. This analysis describes timing and association. It cannot establish why people searched or prove that a news event caused a change.
