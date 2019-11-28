# Road network data for navigation 

The NVDB road network and relevant feature types (such as restrictions and speed limits) are joined into products suitable for route planning. These products are equivalent, but not identical. They are updated approximately 10 times each year. 

### Elveg and Elveg 2.0 

Elveg has been the official route planning product since mid-1990's, although with several modifications. The format is [Norwegian SOSI](https://www.kartverket.no/en/geodataarbeid/SOSI-Standard-in-English/SOSI-Standard-in-English/). Elveg is distributed through the Norwegian mapping authority [metadata and distribution portal](https://kartkatalog.geonorge.no/?text=elveg). 

From 2020, the major revised Elveg 2.0 can be downloaded as GML through the Norwegian mapping authority [metadata and distribution portal](https://kartkatalog.geonorge.no/?text=elveg). A test version of Elveg 2.0 can be downloaded from December 2020. 

### Data for NVDB route planning application

The Norwegian Road Administration willingly shares the road network data that we use in our own route planning application. For historical reasons, we've had to produce these data in both esri file geodatabase and spatiaLite formats. At some point, we will scrap support for the esri file geodatabase. There is some rather [crude and rudimentary documentation here](https://www.vegdata.no/2013/08/08/hvor-finner-jeg-vegnettsdata-til-navigasjon/). 

Currently, we publish these data through two parallell channels: 
  * The Norwegian Mapping authority [metadata and distribution channel](https://kartkatalog.geonorge.no/metadata?text=ruteplan)
  * Our [FTP server](ftp://vegvesen.hostedftp.com/~StatensVegvesen/vegnett/) 

We've had some minor quirks with the first one, as soon as we feel confident the quirks are gone for good we'll drop support for ftp. 

## NVDB road network data model

Node-link structure 

Unique, persistent ID and position. 

