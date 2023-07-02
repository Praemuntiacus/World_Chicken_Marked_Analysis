# World_Chicken_Market_Analysis
Analysis of World chicken market with Python
## Analysis of World Chicken Market (Python: clustering, K-means, PCA, Geopandas)

- Jupyter Notebook with Puthon code and generated plots are here: [Notebook file](https://github.com/Praemuntiacus/World_Chicken_Marked_Analysis/blob/main/CROITOR_Roman_1_notebook_602022_new.ipynb)

### English version

The project aims to identify the most promising countries for exporting chicken meat, considering various factors such as political stability, GDP and GDP growth, rate of food imports, and more. Additionally, I analyzed the dynamics of urban population growth as an indicator of potential changes in local poultry production, with a potential shift towards industrial production and increased poultry imports. To assess the significance of poultry products in the population's diet, I calculated the percentage of protein derived from poultry using data provided by the [FAO](https://www.fao.org/faostat/en/#data)
. This parameter provides valuable insights into the importance of poultry products in relation to economic conditions and cultural traditions. Interestingly, my analysis revealed that countries with a strong nomadic cultural component, such as Mongolia and Kazakhstan, exhibit low consumption of poultry products, likely due to cultural traditions.The following parameters were selected for the analysis:
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

### Version française

Le projet vise à définir les pays les plus intéressants pour l'exportation de viande de poulet :rooster:, en se basant sur plusieurs facteurs tels que la stabilité politique, le PIB et la croissance du PIB, le taux d'importation de produits alimentaires, et bien d'autres. Parmi les caractéristiques prises en compte, j'ai également calculé la dynamique de croissance de la population urbaine, qui peut indiquer une diminution de la production locale de volaille et une augmentation de l'importance de la production industrielle et de l'importation de volaille. J'ai également calculé le taux de protéines d'origine aviaire dans l'alimentation de la population en utilisant les données fournies par la FAO. Ce paramètre pourrait être important pour estimer l'importance des produits avicoles dans l'alimentation de la population, ce qui peut être influencé par les conditions économiques et les traditions. Cette supposition intuitive s'est avérée très utile, car au cours de mon analyse, j'ai découvert que les pays ayant une forte composante de culture nomade (comme la Mongolie et le Kazakhstan) se caractérisent par une consommation très faible de produits avicoles, probablement en lien avec la tradition culturelle.

Les variables suivantes sont choisies pour l'analyse :
- niveau d'urbanisation de la population ("urb pop 2018, %") ;
- dynamique de la population urbaine au cours de la dernière décennie ("urb pop change, %") ;
- taux d'importation de produits d'alimentation ("import alim 2018, %") ;
- produit intérieur brut ("PIB, S") ;
- taux de variation du PIB au cours de la dernière décennie ("PIB grouth, %") ;
- indice de stabilité ("stability index") ;
- prix du poulet ("chicken 2017, S/t") ;
- surface relative des terrains agricoles ("Dens sprtagric/ha") ;
- quantité de poulets par rapport au nombre total d'animaux d'élévage ("% total UGB") ;
- consommation de protéines de volaille par personne ("poultry prod/pers, %") ;
- produits alimentaires totaux par personne ("product/pers, t").

Nous recherchons des pays en développement dynamique, leur situation sociale et politique plutôt stable, avec une urbanisation croissante et un taux élevé de consommation de volailles.


