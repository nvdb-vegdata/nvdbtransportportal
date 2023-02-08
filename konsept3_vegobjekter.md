# NVDB features

All features from the NVDB data cataloge (except for [a few that we aren't able to share freely](https://www.vegdata.no/bruk-av-data/objekttyper-vi-ikke-publiserer/)) are available for download through the [/vegobjekter/featureTypeID](https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekter) end point 

The feature type ID is found in the [NVDB data cataloge](./konsept2_datakatalog.md). 

The default response is a list with the NVDB feature ID and link of the objects matching your query, and a metadata-element with details needed for [pagination](./README.md). 

Obviously, you will find all relevant details for each road object by following the href link. But for many usecases, you would want to include more details about the individual features with the response. This is controlled using the `inkluder` (= include) parameter. 

```json
{
  "objekter": [
    {
      "id": 78697179,
      "href": "https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekter/105/78697179/1"
    },
    {
      "id": 78697180,
      "href": "https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekter/105/78697180/1"
    },
    {
      "id": 78697181,
      "href": "https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekter/105/78697181/1"
    }
  ],
  "metadata": {
    "antall": 874921,
    "returnert": 3,
    "sidestørrelse": 3,
    "neste": {
      "start": "7KZjpAnmxcNjmSt3bfGHgWowDsciKGkE4gYbfFBRAHudhjGQUHziCQq8K55aBtZPKseXih8zbx2FGZuPT3P96q7NYjNgo42m4SsChxHn",
      "href": "https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekter/105?antall=3&start=7KZjpAnmxcNjmSt3bfGHgWowDsciKGkE4gYbfFBRAHudhjGQUHziCQq8K55aBtZPKseXih8zbx2FGZuPT3P96q7NYjNgo42m4SsChxHn"
    }
  }
}
```

### Syntax for for including more details about road objects

```
inkluder=alle
inkluder=metadata,egenskaper,relasjoner,lokasjon,vegsegmenter,geometri

https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekter/105?inkluder=alle&antall=3
```

# Filters

NVDB api has extensive filter capabilities, including [road reference](./konsept4_roadreference.md), [road network](./konsept5_network.md) link sequence ID and position, feature properties, administrative areas and bounding box (the _kartutsnitt_ parameter).  [Documentation with examples](https://nvdbapiles-v3.atlas.vegvesen.no/dokumentasjon/). 


