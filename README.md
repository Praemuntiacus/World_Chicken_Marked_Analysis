# World_Chicken_Market_Analysis
Analysis of World chicken market with Python
## Analysis of World Chicken Market (Python: clustering, K-means, PCA, Geopandas)

- Jupyter Notebook with Puthon code and generated plots are here: [Notebook file](https://github.com/Praemuntiacus/World_Chicken_Marked_Analysis/blob/main/CROITOR_Roman_1_notebook_602022_new.ipynb)

:uk:
**Description:** The project is aimed to define the most interesting countries for chicken :rooster: meat export, basing on several factors, like political stability, PIB and PIB grouth, rate of alimentation products import, and so on. Among the characters taken into account, I also calculated the dynamics of urbam population grouth that may indicate the decrease of local production of poultry and increase of importance of industrial production of poultry and poultry import. I also calculated the rate of poultry origin proteins in the population alimentation using the data profided by [FAO] (https://www.fao.org/faostat/en/#data). This parameter could be important for estimation of importance of poultry products in population diet that could be caused by economical conditions and traditions. This intuitive assumption was very useful, since during my analysis I discovered that countried with strong nomad culture component (for instance, Mongolia, Kazachstan) are characterized by very low consumption of poultry products that is apparently related to the cultural tradition. The following parameters were selected for the analysis:
- Urbanization level of the population ("urban pop 2018, %").
- Dynamics of urban population over the past decade ("urban pop change, %").
- Rate of food imports ("import alim 2018, %").
- Gross Domestic Product ("GDP, S").
- GDP growth rate over the past decade ("GDP growth, %").
- Stability index.
- Chicken price ("chicken 2017, S/t").
- Relative area of agricultural land ("Density of agricultural land/ha").
- Quantity of chickens relative to the total number of livestock ("% total UGB").
- Poultry protein consumption per person ("poultry prod/pers, %").
- Total food products per person ("product/pers, t").

So, We are looking for dynamically developing countries with a relatively stable social and political situation, experiencing increasing urbanization, and having a high rate of poultry consumption.

:fr:
Les variables suivantes sont choisies pour l'analyse :
1) niveau d'urbanisation de la population ("urb pop 2018, %") ;
2) dynamique de la population urbaine au cours de la dernière décennie ("urb pop change, %") ;
3) taux d'importation de produits d'alimentation ("import alim 2018, %") ;
4) produit intérieur brut ("PIB, S") ;
5) taux de variation du PIB au cours de la dernière décennie ("PIB grouth, %") ;
6) indice de stabilité ("stability index") ;
7) prix du poulet ("chicken 2017, S/t") ;
8) surface relative des terrains agricoles ("Dens sprtagric/ha") ;
9) quantité de poulets par rapport au nombre total d'animaux d'élévage ("% total UGB") ;
10) consommation de protéines de volaille par personne ("poultry prod/pers, %") ;
11) produits alimentaires totaux par personne ("product/pers, t").

Nous recherchons des pays en développement dynamique, leur situation sociale et politique plutôt stable, avec une urbanisation croissante et un taux élevé de consommation de volailles.


