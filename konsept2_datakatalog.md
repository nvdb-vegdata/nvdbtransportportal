# NVDB data catalogue

The NVDB data catalogue describes approximately 400 feature types in the Norwegian Road data base (NVDB). These features are attached to the [road network](./konsept5_network.md) through linear referencing. Unfortunately, no complete English translation exists. 

All NVDB features have a list of attributes. Each 
attribute has an unique ID and a (possibly non-unique) 
name. Obviously, the data type is described (text, integer, floating number, date and so on). Some attribute types have values that are restricted to a specific set of pre-defined values, i.e. `enum`-codes. Some have units of measure.  

Futher, the feature is attached to the road 
network in a point or along it (i.e. a line). There are 
various rules for how instances of this feature type may
 or may not overlap, if the feature type is supposed to be global (i.e. covering the whole road network, such as speed limits), and so on. 
 
Finally, the feature type may have 
`1:many` relationship to other feature types (which we call _forelder - barn_, i.e. parent - child relations), or there may be a `many:1` relation to a particular instance of some other feature type _(barn - forelder_, i.e. sibling-parent relation).  `Many:many` relationship are theoretical possible, but not used so far. 

And every single piece of information (attribute type, feature type id, and so on) has a unique ID that can be used for quering or filtering the data catalogue end point (`vegobjekttyper/`) or the feature end point (`vegobjekter/`) for specifict pieces of information. 

The NVDB data catalogue has several manifestations: 

### In your browser: 

[https://datakatalogen.vegdata.no](datakatalogen.vegdata.no) is the most popular and widely used manifestation of the NVDB data catalogue. 

### Within Vegkart 

In our web application [vegkart](./vegkart.md) the data catalogue is found by toggling the book symbol situated next to the query box.

### The `vegobjekttyper/`end point of the NVDB api

Vegobjekttyper = types of NVDB features (road features, veg = road). 

[https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekttyper/](https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekttyper/) will list all NVDB feature types. Usually, you'd want to restrict the result to one particular feature type by appending the feature type ID: `https://nvdbapiles-v3.atlas.vegvesen.no/vegobjekttyper/<featureTypeID>`. Further drill-down to specific property types (by ID) is possible. 

### Java

Through [this page](https://www.vegvesen.no/fag/teknologi/nasjonal+vegdatabank/datakatalogen) you will find a link to the Datakatalogen java program (java web start) 
