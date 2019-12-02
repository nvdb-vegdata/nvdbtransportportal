# NVDB features

All features from the NVDB data cataloge (except for [a few that we aren't able to share freely](https://www.vegdata.no/bruk-av-data/objekttyper-vi-ikke-publiserer/)) are available for download through the [/vegobjekter/featureTypeID](https://www.vegvesen.no/nvdb/api/v3/vegobjekter) end point 

The feature type ID is found in the [NVDB data cataloge](./konsept2_datakatalog.md). 

The default response is a list with the NVDB feature ID and link of the objects matching your query. This can be expanded 

```json
{
  "objekter": [
    {
      "id": 78697179,
      "href": "https://www.vegvesen.no/nvdb/api/v3/vegobjekter/105/78697179/1"
    },
    {
      "id": 78697180,
      "href": "https://www.vegvesen.no/nvdb/api/v3/vegobjekter/105/78697180/1"
    },
    {
      "id": 78697181,
      "href": "https://www.vegvesen.no/nvdb/api/v3/vegobjekter/105/78697181/1"
    }
  ],
  "metadata": {
    "antall": 874921,
    "returnert": 3,
    "sidestørrelse": 3,
    "neste": {
      "start": "7KZjpAnmxcNjmSt3bfGHgWowDsciKGkE4gYbfFBRAHudhjGQUHziCQq8K55aBtZPKseXih8zbx2FGZuPT3P96q7NYjNgo42m4SsChxHn",
      "href": "https://www.vegvesen.no/nvdb/api/v3/vegobjekter/105?antall=3&start=7KZjpAnmxcNjmSt3bfGHgWowDsciKGkE4gYbfFBRAHudhjGQUHziCQq8K55aBtZPKseXih8zbx2FGZuPT3P96q7NYjNgo42m4SsChxHn"
    }
  }
}
```

# Include more data with the response

```
inkluder=alle
inkluder=metadata,egenskaper,relasjoner,lokasjon,vegsegmenter,geometri
```

