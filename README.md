# Similar Stocks

This repository will hold similar stocks based on their description through NLP models.

The methodology is described below:

1. Using FinanceDatabase package filter from companies within same Sector and Industry. We do not want to filter by Country and/or Market cap as we want to get similar companies based on what they do, regardless of their location and their market cap.

2. Pick an NLP algorithm to compare the description between these companies in the same Sector and Industry, e.g. cosine similarity.

3. Create a folder for the outputs coming from that algorithm, e.g. `cosine_similarity/`.

4. Within this folder create a folder for each of the industries, e.g. `cosine_similarity/auto_manufacturers/`

5. For each ticker within the same Sector and Industry, we will create a dictionary with the remaining tickers of the Sector and Industry and their similarity values. E.g. `cosine_similarity/auto_manufacturers/TSLA.csv` will have a dictionary such as:
```
{
    "NIO": 0.69,
    "LI": 0.420,
    ...
}
```
