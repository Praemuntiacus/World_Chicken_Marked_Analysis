# World_Chicken_Market_Analysis
Analysis of World chicken meat market with Python
## Analysis of World Chicken Market (Python: data extraction, cleaning and transformation, hierarchical clustering, K-means, PCA, Geopandas)

- Jupyter Notebook with Puthon code and generated plots are here: [Notebook file](https://github.com/Praemuntiacus/World_Chicken_Marked_Analysis/blob/main/CROITOR_Roman_1_notebook_602022_new.ipynb)

![image](https://github.com/Praemuntiacus/World_Chicken_Marked_Analysis/assets/125415799/2a1d2422-cab4-4d99-b737-ca419fd85372)


The project aims to identify the most promising countries for exporting chicken :rooster: meat, considering various factors such as political stability, GDP and GDP growth, rate of food imports, and more. Additionally, I analyzed the dynamics of urban population growth as an indicator of potential changes in local poultry production, with a potential shift towards industrial production and increased poultry imports. To assess the significance of poultry products in the population's diet, I calculated the percentage of protein derived from poultry using data provided by the [FAO](https://www.fao.org/faostat/en/#data)
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

To identify the most suitable country or group of countries for poultry meat export based on the selected criteria, I employed hierarchical clustering and K-means clustering algorithms. I compared the *silhouette scores* for hierarchical clustering using **scipy.cluster.hierarchy** and K-means using **silhouette_samples, silhouette_score** imported from **sklearn.metrics**. The results indicated that K-means produced more reliable outcomes. It grouped countries into four well-defined clusters.

To gain further insights, I utilized *Principal Component Analysis* (PCA) to visualize the relative positions of selected "typical" countries within each cluster, as well as their relationships with other countries worldwide. PCA helped provide a precise characteristic of each cluster and revealed shared characteristics among countries in the same cluster.

Additionally, I employed **sns.clustermap()**, a helpful visualization tool, to understand the cluster characteristics obtained through K-means across different principal components (PC1, PC2, PC3). This allowed for a better understanding of how distinct countries within the same cluster were from each other.

Thus, the combination of hierarchical clustering, K-means clustering, PCA, and visualization tools provided in my analysis valuable insights into identifying suitable countries for poultry meat export and understanding the characteristics and relationships within and between clusters.

To visualize the results obtained, I utilized **Geopandas**. In order to use **Geopandas** visualizations, I needed to add a new column containing country codes to my main dataframe. I obtained these data in French from Wikipedia and selected the "*ISO 3166-1 alpha-3*" code as it is compatible with the world countries dataset in **Geopandas**, enabling me to merge the two dataframes. This solution was necessary due to the language difference between my work dataframe (which contained country names in French) and the **Geopandas** dataset (which was in English). Using the universal "*ISO 3166-1 alpha-3*" code was the only viable option for joining the dataframes.

With the newly acquired dataframe, I was able to create choropleth maps that visualized the characteristics of the countries under consideration, providing a geographical perspective on the data. To display the country clusters on the map, I added a new column called "*clusters*" to the dataframe and assigned the values from the "*cluster*" object generated by the K-means algorithm.

For visualizing the main characteristics of the clusters, including geopolitical stability, GDP, chicken consumption, and others, I employed **sns.boxplot()**, which proved to be the most suitable visualization tool for this purpose.

By incorporating **Geopandas**, creating the necessary data associations, and utilizing appropriate visualization tools, I was able to effectively visualize the country characteristics and cluster information in a geographical context.

## Characteristics of the four groups of countries:
- **Countries with a dynamic growing market (cluster 0)**. These countries are characterized by relatively low GDP and stability index, but with a positive growth dynamic. The level of urbanization is often very high. The importation of alimentary products can be significant. These countries have moderate food production, poultry product prices aligned with global prices, and a very high consumption of poultry products. The vast and dynamic market of this category of countries may represent a particular interest for poultry importation, despite certain risks.

- **Stable countries with limited agricultural capacities (cluster 1)**. Small countries with a high level of urbanization, high GDP, high stability index, high consumption of poultry, and poultry product prices aligned with global prices. Limited resources for agriculture result in low per capita food production. Therefore, these countries seem to be of interest for chicken importation. A negative factor is the relatively small size of the market.

- **Countries with low consumption of poultry products (cluster 2)**. Some of these countries have a low GDP and low stability index and/or low urbanization, poultry product prices slightly higher than global prices, and a high rate of food product importation. The negative factors are low poultry consumption and/or geopolitical instability.

- **Countries with a saturated poultry production market (cluster 3)**. These countries are characterized by high GDP, high stability index, often low poultry production costs, poultry purchase prices lower than the average global prices (apparently due to efficient agricultural methods), relatively low food product importation, and low poultry consumption compared to other countries.

## Conclusions
The analysis shows three regions in the world with high potential for poultry importation:

- South Asia (Indonesia, Bangladesh, India, Malaysia, etc.), where poultry consumption is an ancient tradition (South Asia is historically the center of chicken domestication). South Asia is the largest and seemingly the most promising market.
- Middle East (Saudi Arabia, Kuwait, Morocco, Tunisia, etc.).
- Central and South America (Mexico, Colombia, etc.) could be an interesting area for poultry importation due to its geographical proximity to French Guiana, which is a climatic and logistical favorable zone for poultry production and exportation to Central America.


![image](https://github.com/Praemuntiacus/World_Chicken_Marked_Analysis/assets/125415799/ab739c25-fca3-4888-abce-b1bd5f80c8d9)


Le projet vise à définir les pays les plus intéressants pour l'exportation de viande de poulet :rooster:, en se basant sur plusieurs facteurs tels que la stabilité politique, le PIB et la croissance du PIB, le taux d'importation de produits alimentaires, et bien d'autres. Parmi les caractéristiques prises en compte, j'ai également calculé la dynamique de croissance de la population urbaine, qui peut indiquer une diminution de la production locale de volaille et une augmentation de l'importance de la production industrielle et de l'importation de volaille. J'ai également calculé le taux de protéines d'origine aviaire dans l'alimentation de la population en utilisant les données fournies par la [FAO](https://www.fao.org/faostat/en/#data). Ce paramètre pourrait être important pour estimer l'importance des produits avicoles dans l'alimentation de la population, ce qui peut être influencé par les conditions économiques et les traditions. Cette supposition intuitive s'est avérée très utile, car au cours de mon analyse, j'ai découvert que les pays ayant une forte composante de culture nomade (comme la Mongolie et le Kazakhstan) se caractérisent par une consommation très faible de produits avicoles, probablement en lien avec la tradition culturelle.

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

Nous recherchons donc des pays en développement dynamique, leur situation sociale et politique plutôt stable, avec une urbanisation croissante et un taux élevé de consommation de volailles.

Pour identifier le pays ou le groupe de pays les plus appropriés pour l'exportation de viande de volaille selon les critères sélectionnés, j'ai utilisé les algorithmes de regroupement hiérarchique et de regroupement K-means. J'ai comparé les scores de silhouette pour le regroupement hiérarchique en utilisant **scipy.cluster.hierarchy** et pour le regroupement K-means en utilisant **silhouette_samples**, **silhouette_score** importés de **sklearn.metrics**. Les résultats ont montré que le K-means produisait des résultats plus fiables. Il a regroupé les pays en quatre clusters bien définis.

Pour obtenir des informations supplémentaires, j'ai utilisé *l'Analyse en Composantes Principales* (PCA) pour visualiser les positions relatives des pays "typiques" sélectionnés au sein de chaque cluster, ainsi que leurs relations avec les autres pays du monde. La PCA a permis de donner une caractéristique précise à chaque cluster et de révéler les caractéristiques communes entre les pays d'un même cluster.

De plus, j'ai utilisé **sns.clustermap()**, un outil de visualisation utile, pour comprendre les caractéristiques des clusters obtenus par le K-means à travers différentes composantes principales (PC1, PC2, PC3). Cela a permis de mieux comprendre à quel point les pays d'un même cluster étaient distincts les uns des autres.

Ainsi, la combinaison du regroupement hiérarchique, du regroupement K-means, de l'ACP et des outils de visualisation utilisés dans mon analyse a fourni des informations précieuses pour identifier les pays adaptés à l'exportation de viande de volaille et comprendre les caractéristiques et les relations au sein et entre les clusters.

Pour visualiser les résultats obtenus, j'ai utilisé **Geopandas**. Pour utiliser les visualisations de **Geopandas**, j'ai dû ajouter une nouvelle colonne contenant les codes pays à mon dataframe principal. J'ai obtenu ces données en français à partir de Wikipédia et j'ai sélectionné le code "*ISO 3166-1 alpha-3*" car il est compatible avec l'ensemble de données des pays du monde dans **Geopandas**, ce qui m'a permis de fusionner les deux dataframes. Cette solution était nécessaire en raison de la différence de langue entre mon dataframe de travail (qui contenait les noms des pays en français) et l'ensemble de données de Geopandas (qui était en anglais). Utiliser le code universel "*ISO 3166-1 alpha-3*" était la seule option possible pour fusionner les dataframes.

Avec le nouveau dataframe obtenu, j'ai pu créer des cartes choroplèthes qui visualisaient les caractéristiques des pays considérés, offrant ainsi une perspective géographique des données. Pour afficher les clusters de pays sur la carte, j'ai ajouté une nouvelle colonne appelée "*clusters*" au dataframe et j'ai attribué les valeurs de l'objet "*cluster*" généré par l'algorithme K-means.

Pour visualiser les principales caractéristiques des clusters, telles que la stabilité géopolitique, le PIB, la consommation de volaille, etc., j'ai utilisé **sns.boxplot()**, qui s'est avéré être l'outil de visualisation le plus adapté à cet effet.

En incorporant **Geopandas**, en créant les associations de données nécessaires et en utilisant les outils de visualisation appropriés, j'ai pu visualiser efficacement les caractéristiques des pays et les informations sur les clusters dans un contexte géographique.

## Les caractéristiques des quatre groupes de pays :
- **Les pays avec un marché en croissance dynamique (cluster 0)**. Ces pays se caractérisent par un PIB et un indice de stabilité relativement bas, mais avec une dynamique de croissance positive. Le niveau d'urbanisation est souvent très élevé. L'importation de produits d'alimentation peut être très importante. Ces pays se caractérisent par une production d'alimentation modérée, un prix de produits avicoles aligné sur les prix mondiaux, et une très forte consommation de produits avicoles. Le vaste marché dynamique de cette catégorie de pays peut représenter un intérêt particulier pour l'importation de volailles, malgré certains risques.

- **Les pays stables aux capacités agricoles limitées (cluster 1)**. Petits pays avec un niveau d'urbanisation très élevé, un PIB élevé, un indice de stabilité élevé, un niveau élevé de consommation de volailles et les prix de produits avicoles aligné sur les prix mondiaux. Les ressources limitées pour l'agriculture sont une cause de faible production alimentaire par habitant. Il semble donc que ces pays présentent un intérêt pour l'importation de poulets. Un facteur négatif est la taille plutôt réduite du marché.

- **Les pays à faible consommation de produits avicoles (cluster 2)**. Certains de ces pays ont un faible PIB et un faible indice de stabilité, et/ou ont une faible urbanisation, les prix des produits avicoles un peu plus haut que les prix mondiaux et un taux élevé d'importation de produits alimentaires. Les facteurs négatifs sont une faible consommation de volailles et/ou une instabilité géopolitique.

- **Les pays dont le marché de la production avicole est saturé (cluster 3)**. Ces pays se caractérisent par un PIB élevé, un indice de stabilité élevé, des coûts souvent bas de production de volailles et des prix d'achats des volailles inférieurs aux prix mondiaux moyens (apparemment en raison de méthodes efficaces d'agriculture), des importations de produits alimentaires relativement faibles et une consommation peu élevée de volailles comparativement à d'autres pays.

## Conclusions
L'analyse montre trois régions du monde à fort potentiel d'importation de volailles :
* l'Asie du Sud (Indonésie, Bangladesh, Inde, Malaisie, etc.) où la consommation de volailles est une tradition ancienne (l'Asie du Sud est historiquement le centre de la domestication des poules). L'Asie du Sud est le marché le plus important et semble-t-il le plus prometteur.
* le Proche-Orient (Arabie saoudite, Koweït, Maroc, Tunisie, etc.).
* l'Amérique centrale ed du sud (Mexique, Colombie, etc.) pourraît être une zone interressante pour l'importation de volailles, en raison de sa proximité géographique avec la Guyanne française qui est une zone climatique et logistique favorable pour la production et l'exporation de volailles vers l'Amérique centrale.








