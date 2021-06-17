# WorldKG-Knowledge-Graph 

- [www.worldkg.org](http://www.worldkg.org/)

This repository contains code to reproduce the WorldKG knowledge graph. 
The WorldKG knowledge graph is a comprehensive large-scale geospatial knowledge graph based on OpenStreetMap that provides semantic representation of geographic entities from over 188 countries. WorldKG contains higher representation of geographic entities compared to other knowledge graph and can be used as an underlying data source for various applications such as geospatial question answering, geospatial data retrieval, and other cross-domain semantic data-driven applications.

<h3>Prerequisites</h3>
<ul>
	<li>Python >= 3.7</li>
</ul>


<h3>Setup</h3>
<p>Steps to create the WorldKG triples for the particular OSM snapshot.</p>
<ol>
    <li>Clone the repository
		git clone https://github.com/alishiba14/WorldKG-Knowledge-Graph.git<br>
		cd WorldKG-Knowledge-Graph
	</li>
    <li>Install the Python Requirements
		pip install -r requirements.txt
	</li>


<li>Download the specific OpenStreetMap snapshot, e.g., from <a href="https://download.geofabrik.de/" target="_blank">https://download.geofabrik.de/</a>. We recommend using the osm.pbf format.</li>

<li>Run the CreateTriples.py:

python3 CreateTriples.py /path-to-pbf-file /path-to-the-ttl-file-to-save-triples 

Example: python3 CreateTriples.py italy-latest.osm.pbf italyTriples.ttl</li>
</ol>

<h3>File Structure</h3>

<li>Key_List.csv - Contains list of OSM keys with valid OSM wiki page.</li>
<li>OSM_Ontology_map_features.csv - Contains tags collected from OSM map features (https://wiki.openstreetmap.org/wiki/Map_features).</li>
<li>requirements.txt - Contains versions of python libraries used.</li>
<li>CreateTriples.py - Main python file to create the WorldKG instance triples.</li>
<li>WorldKG_Ontology.ttl - WorldKG ontology triples in .ttl format.</li>
<li>Manual Annotations Sample Set - In this folder, we provide the entities and classes used for evaluation of the tag-to-class mapping in WorldKG.</li>

# License
MIT License

Copyright (c) 2021 Alishiba Dsouza

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
