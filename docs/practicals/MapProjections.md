---
icon: material/numeric-2-box
title: Practical 2
---

# Map projections

## Basic terms

<div class="grid_container">
  <div class="grid_item" style="flex:1 1 300px;">
    <strong>Geographic coordinate system (GCS)</strong>
    <hr style="margin:5px 0 !important;">
    <p> A <strong>Geographic coordinate system (GCS)</strong> is a reference framework that defines the locations of features on a model of the earth. It’s shaped like a globe—spherical. Its units are angular, usually degrees. </p>
    <p><strong>GCS</strong> defines <strong>where</strong> the data is located on the model of Earth’s surface.</p>
  </div>
  <br>
  <div class="grid_item" style="flex:1 1 300px;">
    <strong>Projected coordinate system (PCS)</strong>
    <hr style="margin:5px 0 !important;">
    <p> A <strong>Projected coordinate system (PCS)</strong> is flat. It contains a GCS, but it converts that GCS into a flat surface, using math (the projection algorithm) and other parameters. Its units are linear, most commonly in meters.</p>
    <p><strong>PCS</strong> tells the data <strong>how</strong> to draw on a flat surface, like on a paper map or a computer screen.</p>
  </div>
  <br>
  <div class="grid_item" style="flex:1 1 300px;">
    <strong>Map projection</strong>
    <hr style="margin:5px 0 !important;">
    <p> A <strong>map projection</strong> is the mathematical algorithm that defines how to present the round earth on a flat map. It is one parameter in a projected coordinate system (PCS).</p>
  </div>
</div>
 <br>

![](../assets/cviceni2/CS.png){ .no-filter .off-glb}
{: align=center}

<br>
!!! note-grey "Note"

    *Projection on the fly* is what ArcGIS does to **resolve conflicts** when your data is in a different coordinate system than your map. It does this so the data can draw in the correct place on the map. *Projection on the fly* ensures that the data draws in the map’s coordinate system, even though it is still stored in other coordinate systems. ArcGIS will **always** apply *projection on the fly* when it’s needed. It can’t draw the data on your map otherwise.
<br>
**Sources:**
{: align=center }

[<span>pro.arcgis.com</span><br>Geographic vs Projected Coordinate Systems](https://www.esri.com/arcgis-blog/products/arcgis-pro/mapping/gcs_vs_pcs/){ .md-button .md-button--primary .server_name .external_link_icon_small target="\_blank"}
[<span>pro.arcgis.com</span><br>Coordinate Systems](https://www.esri.com/arcgis-blog/products/arcgis-pro/mapping/coordinate-systems-difference/){ .md-button .md-button--primary .server_name .external_link_icon_small target="\_blank"}
[<span>learn.arcgis.com</span><br>Map projections in ArcGIS Pro](https://storymaps.arcgis.com/stories/ea0519db9c184d7e84387924c84b703f){ .md-button .md-button--primary .server_name .external_link_icon_small target="\_blank"}
{: .button_array}

**Learn more:**
{: align=center }

[<span>learn.arcgis.com</span><br>Fix data when it appears on a wrong place](https://learn.arcgis.com/en/projects/fix-data-when-it-appears-in-the-wrong-place/){ .md-button .md-button--primary .server_name .external_link_icon_small target="\_blank"}
[<span>learn.arcgis.com</span><br>Choose the right projection](https://learn.arcgis.com/en/projects/choose-the-right-projection/){ .md-button .md-button--primary .server_name .external_link_icon_small target="\_blank"}
{: .button_array}

## Web Mercator distortion

The Web Mercator projection, an adapted version of the Mercator projection, has become the default map projection for web mapping. Unlike its predecessor, it employs a spherical formula consistently across all scales. Major online map providers, such as Google Maps, CARTO, Mapbox, OpenStreetMap, Esri, and others, widely employ this projection.

The primary advantage of the Mercator projection, and consequently the Web Mercator, is its preservation of direction, providing users with the valuable knowledge that north is consistently oriented upwards. Despite even distortion throughout most areas, as one moves away from the equator, distortion intensifies, causing significant stretching toward the poles. Consequently, the Web Mercator projection is unsuitable for polar displays. Due to these apparent distortions, it is not recommended for spatial analysis or area calculations.

<iframe style="filter:none !important;margin-top:.6rem;" width="100%" height="500" frameborder="0" allowfullscreen src="https://www.thetruesize.com/#?borders=1~!MTU2ODg0MjU.NDY3MTc3NQ*MzEyNTI5MDA(NjIzOTIyOA~!CONTIGUOUS_US*MTAwMjQwNzU.MjUwMjM1MTc(MTc1)MQ~!IN*NTI2NDA1MQ.Nzg2MzQyMQ)MA~!CN*OTkyMTY5Nw.NzMxNDcwNQ(MjI1)Mg"></iframe>

<iframe style="filter:none !important;margin-top:.6rem;" width="100%" height="500" frameborder="0" allowfullscreen src="https://developers.arcgis.com/javascript/latest/sample-code/client-projection/live/"></iframe>

## Assignment 01
!!! abstract "Shapes of Iceland"
    **TASK:**

    Make a map showing distortions and area of Iceland in following projections:
    
    - Goode Homolosine
    - Bonne
    - Winkel–Tripel
    - Mollweide
    - Cube
    - Spilhaus
    - Robinson
    - Fuller
    - Plate Carée
    - Mercator

    <br>
    Your map should look similar to this [map](https://blogs.egu.eu/divisions/cr/2023/06/16/it-aint-easy-being-greenland/).

    <br>
    In technical report answer following questions:
    
    - Which projection distorts the shape of Iceland the most/the less? Compare the total area of Iceland in these projections with its actual size.
    
    <br>
    **DATA SOURCES:**
    
      [:material-download: Natural Earth (States/Provinces, 1:50m) :material-layers:](https://www.naturalearthdata.com/http//www.naturalearthdata.com/download/50m/cultural/ne_50m_admin_1_states_provinces.zip){ .md-button .md-button--primary .button_smaller }
      {: .button_array style="justify-content:flex-start;"}
    
    
    **SUBMISSION FORM:**

    - technical report + 1 map in PDF format
    
    <br>
    **INSTRUCTIONS:**

    - Set the projection of Map *(Properties-Coordinate Systems)* and add *states_provinces* layer.
    - Use *Definition Query *to filter the features to work only with your area of interest.
    - Use optional symbolization of the layer.
    -	Duplicate the original map and create 9 more maps and change the projection in each map to a different one.
    - Add all map frames to layout and make sure each has the same scale (1:10,000,000).
    - In *New Layout* (A3 Portrait) insert the Map Title, Scale and Credits
    - Label each shape with the name of the map projection used.
    - Export *Layout* in PDF Format
