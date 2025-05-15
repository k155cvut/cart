---
icon: material/numeric-8-box
title: Practical 8
---
# Grid maps, data binning
**Grid maps** are a type of thematic map that represent spatial data by dividing the mapped area into a regular grid of cells (squares or hexagons) and summarising information within each cell. Instead of visualising data by administrative or natural boundaries, grid maps provide a uniform spatial framework that supports consistent comparison across the entire area.

Each cell in the grid contains a value based on the data points or features that fall within it—such as counts, averages, or densities. This approach is especially useful for analysing and visualising point data, spatial distributions, or continuous phenomena, as it avoids the distortions introduced by unevenly sized administrative units. **Grid maps** are widely used in environmental studies, urban analysis, population research, and risk mapping.

Mapping technique that groups point data into a grid composed of regularly shaped areas is known as **data binning**.


<figure markdown>
  ![](../assets/cviceni8/hexbins.png){ width=500px }
</figure>




<div style="text-align: center;">
<iframe width="560" height="315" src="https://www.youtube.com/embed/JlZMGDeNpTc?si=EEaxeIcEohuU7DvA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

<br>

[Aggregate features into bins](https://pro.arcgis.com/en/pro-app/latest/help/mapping/layer-properties/aggregate-features-into-bins.htm){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
{: .button_array}

<hr class="level-1">


## Assignment 06
!!! abstract "Traffic accidents in Prague"
    **TASK:**

    Make a map using hexagonal binning techniqeue to aggregate and visualise spatial data related to traffic accidents in Prague. Within each hexagon try to visualise  following information:

      - the total length of roads,

      - the number of recorded traffic accidents,

      - the location of fatal accidents.

  

    <br>
    **DATA SOURCES:**
    
    - Input data are available on the Shares drive, in the directory ``K155\Public\155CART\Hexbins``.
    

    <br>
    **SUBMISSION FORM:**

    - 1 map in PDF format (submit by 25/05, send to <a href="mailto:petra.justova@fsv.cvut.cz">petra.justova@fsv.cvut.cz</a>)
    
    <div class="annotate" markdown>
    <br>
    **INSTRUCTIONS:**

      - Add *Prague_polygon.shp* to Map
      - Create a hexagonal grid *(Generate Tesselation)*
      - Limit the hexagonal grid to the area of Prague *(Select by Location-Have their center in)*
      - Add *Prague_roads.shp* to Map
      - Aggregate the information on the total length of roads within each hexagon *(Summarize Within)*
      - Add *accidents_202301-202412.geojson* to Map *(JSON To Features)*
      - Aggregate the information on the number of recorded traffic accidents within each hexagon *(Summarize Within)*
      - Symbolize the hexagonal grid properly to show the total length of roads *(Symbology-Graduated Colors)*, the number of recorded traffic accidents *(Symbology-Graduated Symbols)*, and the location of fatal accidents *(Symbology-Single Symbol)*
      - Finish the layout: insert *Map Title*, *Scale*, *Legend* and *Credits*. Add explanation for the abbreviations of the country names used, if any.
      - Export *Layout* in PDF Format.

      
    