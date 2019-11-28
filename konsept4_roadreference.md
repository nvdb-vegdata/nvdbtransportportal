# Road reference system

The reference system will name each and every road in Norway. 

### Version 2 vs 3 of NVDB api and Vegkart 

  * **Version 3** of [Vegkart](./vegkart.md)  and NVDB api is still under development, and some advanced features are lacking. The most important change from V2 is 
    * A major revision of the road reference system. 
    * After 1st January 2020, the new administrative areas _fylke_ (region) and _kommune_ (municipality) will be enforced
  * **Version 2** of Vegkart and NVDB api will remain avialable untill August 2021 - but with the old road reference  and administrative areas according to the year 2019. 

The main motivation for changing the road reference system is to cut the relationship between administrative units and road segments, due to the major administrative reform at 2020-01-01. 

## Road divided into _strekning, delstrekning and meters_

Each road within each road category has a unique number. The road is split into smaller parts, first into _strekning_ (section), which again is subdivided into _delstrekning_ (subsection). Along each _delstrekning_ we count meters, starting at 0 at the beginning of the next _delstrekning_. 

The life cycle of road is divided into phases, starting with the construction fase (A, for _anlegg_ = construction), followed by operational road status (V, for existing _veg_ = road). 

Together, this constitutes the complete road reference of the form **Ev6 S78D1 m768** (Europaveg 6 Strekning (section) 78 delstrekning (subsection) 1 meter 768. 

![vegkart reference](./pics/vegkart_ny.png)


 
# Old road reference system 

The old reference system is no longer in use from January 1st, 2020, but will be available through version 2 of NVDB api and vegkart untill August 2021. The components are: 

  * _Fylkesnummer_ = County number
  * _Kommunenummer_ = Municipality number. Always 00 for road category E, R and F. 
  * Road category: E, R, F, K, P or S. 
  * Road status
  * Road number
  * _hovedparsel_, Hp - Road segment
  * meters. 
  
Along each _*hovedparsel_ we count meters, starting at 0 for each new _hovedparsel_. This is not entirely unlike the new system of _delstrekning_, but the values of those two systems should not be used interchangeably. 

![vegkart reference](./pics/vegkart_ny_og_gammel.png)


