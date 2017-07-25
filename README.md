# Replication data
Leone Sciabolazza, V. , Vacca, R. , Kennelly Okraku, T. , McCarty, C. (2017), Detecting and analyzing research communities in longitudinal scientific networks, Plos One.

## Union Networks

* Type of object: igraph
* Name: 
	- union_2013.rda : union network at 2013
	- union_2014.rda : union network at 2014
	- union_2015.rda : union network at 2015
* Vertex (investigator) attributes
	- name: unique id
	- dept: Department of affiliation (id)
	- college: College of affiliation (id)
	- dsr.acad.unit: Academic Unit of affiliation (id)
	- CTSI: dummy variable. It takes 1 if the investigator is affiliated to the CTSI, and 0 otherwise.
* Edge attributes
	- weigth.sum: number of times i and j co-authored a paper and were PIs or Co-PIs on the same awarded grant in year t.
	- same.floor: dummy variable. It takes 1 if i and j work on same floor, and 0 otherwise.
	- same.building: dummy variable. It takes 1 if i and j work in the same building, and 0 otherwise.

## Research communities: 
* Type of object: network
* Names: 
	- T_G_c_1.rda : Network of collaborations between Cross-sectional co-membership communities. **Note:** In one communiy, two investigators are connected by co-membership if they were in the same yearly collaborative subgroup for two (not necessarily consecutive) years.
	- T_G_c_2.rda : Network of collaborations between Cross-sectional co-membership communities. **Note:** In one communiy, two investigators are connected by co-membership if they were in the same yearly collaborative subgroup for three years.
	- T_G_y_1.rda : Network of collaborations between Inter-temporal co-membership communities. **Note:** In one communiy, two investigators are connected if they were co-members of the same inter-temporal subgroup, sharing only one circle of colleagues for two consecutive years.
	- T_G_y_2.rda : Network of collaborations between Inter-temporal co-membership communities. **Note:** In one communiy, two investigators are connected if they were co-members of the same inter-temporal subgroup, sharing only one circle of colleagues for three consecutive years.
* Vertex (community) attributes
	- bridge_mes : bridging centrality in the union network 2013-2015
	- ctsi : dummy variable. It takes 1 if at least 33% of the members are affiliated to the CTSI, and 0 otherwise.
	- dens : density of the intra-community network.
	- modal_col : Modal value of college affiliation (id).
	- modal_dep : Modal value of department affiliation (id). 
	- num_com : size of the community.
	- var_col : Generalized variance of college affiliation.
	- var_dep : Generalized variance of department affiliation.
	- vertex.names: unique community id.
* Edge attributes
	- bldg: number of pairs of investigators from community i and j working in the same building.
	- fl: number of pairs of investigators from community i and j working on the same floor.