---
layout: default
title: Home
nav_order: 1
description: "Level-of-Detail 1 3D City Models for High School Learning."
permalink: /
---

# geo3D
{: .fs-9 }

[`geo3D`](https://github.com/AdrianKriger/osm_LoD1_3DCityModel) is a [python-based](https://en.wikipedia.org/wiki/Python_(programming_language)) workflow to facilitate high school learning. The tool extends the core [TeachOSM](https://teachosm.org) (Module 1-4) curriculum and is ***meant for communities with a population of 10 000 or less***.

[`geo3D`](https://github.com/AdrianKriger/osm_LoD1_3DCityModel) creates a Level-of-Detail 1 (LoD1) 3D City Model (buildings and terrain) from [OpenStreetMap (osm) contributions](https://www.openstreetmap.org/about) with elevation from a raster Digital Elevation Model (DEM). The workflow aims for simplicity.  

It takes 2D osm vector contributions (building outlines) with [`building:level`](https://wiki.openstreetmap.org/wiki/Key:building:levels) tagged and extrudes the polygon from the DEM (terrain).

 <figure><center>
  <img src="{{site.baseurl | prepend: site.url}}/img/CityJSON_Ninja_cputb.png" style="width: 800px; height: 400px; border: 0px">
  <figcaption>Fig.1 - LoD1 3D Model of the Cape Peninsula University of Technology (Bellville Campus). <em>---streets are in the pipeline; see <cite><a href="https://github.com/AdrianKriger/osm_LoD1_3DCityModel/issues/17"> issue #17</a></cite></em></figcaption>
</center></figure> 
<!-- <p align="center">
<img src="{{site.baseurl | prepend: site.url}}/img/CityJSON_Ninja_cput.png" style="width: 800px; height: 400px; border: 0px">
</p>
<p align="center">
    LoD1 3D Model of the Cape Peninsula University of Technology (Bellville Campus).
</p>
&nbsp;&nbsp;--> 

<p align="center"><b>There are two procesing strategies</b></p>

<!--| [osm_LoD1_3DCityModel](https://github.com/AdrianKriger/geo3D/blob/main/osm_LoD1_3DCityModel-walkthrough.ipynb) | [InteractivateOnly](https://github.com/AdrianKriger/geo3D/blob/main/interactiveOnly.ipynb) |
| :-----: | :-----: |
| If you need a topologically correct LoD1 3D City Model please choose [osm_LoD1_3DCityModel](https://github.com/AdrianKriger/geo3D/blob/main/osm_LoD1_3DCityModel-walkthrough.ipynb) | Please choose [InteractiveOnly](https://github.com/AdrianKriger/geo3D/blob/main/interactiveOnly.ipynb) if you do not need a LoD1 3D City Model |-->

<table>
  <tr>
    <th align="center"><a href="https://github.com/AdrianKriger/osm_LoD1_3DCityModel/tree/main/village_campus">Village/Campus</a></th>
    <th style="background: repeating-linear-gradient(-45deg, transparent, transparent 5px, rgba(0,0,0,0.2) 5px, rgba(0,0,0,0.2) 10px); text-align: center; border: 1px solid black;"><a href="https://github.com/AdrianKriger/osm_LoD1_3DCityModel/tree/main/districts">District</a> <em><strong>[This is on hold]</strong></em></th>
  </tr>
  <tr>
    <td align="center"> If your Area-of-Interest (aoi) has a population of 10 000 or less you are welcome to choose <a href="https://github.com/AdrianKriger/osm_LoD1_3DCityModel/tree/main/village_campus">village/campus</a> </td>
    <td style="background: repeating-linear-gradient(-45deg, transparent, transparent 5px, rgba(0,0,0,0.2) 5px, rgba(0,0,0,0.2) 10px); text-align: center; border: 1px solid black;">Please choose <a href="https://github.com/AdrianKriger/osm_LoD1_3DCityModel/tree/main/districts">districts</a> should you aoi have a population of more than 10 000. </td>
  </tr>
</table>

---

The purpose of this work seeks to expand the core TeachOSM modules, going beyond traditional mapping, to enrich high school learning through a constructivist approach. We drive engagement and participation by *giving students* the ability to create affordable, high-quality 3D City Models and using these as learning tools.

The primary product is a topologically correct Level of Detail 1 (LoD1) 3D City Model. Secondary products include an application of spatial data science and an HTML-based visualization. Our mission is to empower high school learning and community engagement by fostering effective communication and advocacy at the grassroots level.
 
Please see the [Discussion](https://github.com/AdrianKriger/osm_LoD1_3DCityModel/discussions/22).

---

**Input** a raster DEM. Script will call for the [osm contributions](https://www.openstreetmap.org/about#:~:text=OpenStreetMap%20is%20built%20by%20a,more%2C%20all%20over%20the%20world.).  
**Output** includes:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. a topologically correct LoD1 City Model *(information rich building models seperate from the ground; but when connected to the terrain   form a water-tight surface<sup>*</sup>)*;  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. one use case of 3D city models. Population estimation and the calculation of [Building Volume per Capita](https://www.researchgate.net/publication/343185735_Building_Volume_Per_Capita_BVPC_A_Spatially_Explicit_Measure_of_Inequality_Relevant_to_the_SDGs); and  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. an interactive .html which you can navigate, query and share.
<!--&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. a 2.75D surface mesh *(buildings connected to terrain)*;-->  

<sup>* ***the goal is a model that conforms to the ISO 19107 standard [connecting and planar surfaces, correct orientation of the surfaces and watertight volumes] I have not tested this for all possibilities. If the result you achieve is not; you are welcome to raise an [issue](https://github.com/AdrianKriger/osm_LoD1_3DCityModel/issues). I depend on you to help me improve.*** 