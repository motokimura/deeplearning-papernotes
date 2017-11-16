## [Efficient 3D Tracking in Urban Environments with Semantic Segmentation](https://www.labri.fr/perso/vlepetit/pubs/hirzer_bmvc17.pdf)

#### Key words

- 3D tracking, semantic segmentation, 2.5D maps, OpenStreetMap

#### Key points

- A 3D tracking method which additionally takes into account environmental information in terms of 2.5D maps
- Methods
	- 2.5D maps: maps for building footprints and heights
	- By applying semantic segmentation CNN to the input image, building facade, vertical edge, and horizontal edge regions are detected
	- Then, find the most likely camera pose to explain the observations (segmentation results) using the 2.5D maps as a reference

#### Thoughts

- Authors present one of the good utilizations of the OSM or imcomplete (e.g., not fully 3D) maps data for urban navigation