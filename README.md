# youtube_reporting

Ce git contient le code qui a permis de faire une restitution de données sur les caractéristiques des vidéos youtubes populaires.

Dataset :
1. Le jeu de données :
Ce dataset est issu des données récoltées par l’API YouTube.
Ce dataset propose une liste des vidéos qui ont été en tendance sur la plateforme de 2017 à 2018 dans plusieurs pays comme le Canada, l’Allemagne, la France, la Grande Bretagne, l’Inde, le Mexique, la Russie et les Etats-Unis.
Afin de sélectionner ces vidéos tendances, YouTube utilise une combinaison de facteurs, notamment la mesure des interactions des utilisateurs (nombre de vues, partages, commentaires et j'aime).


2. Détail du contenu :
Ce dataset possède de nombreuses données intéressantes à l’analyse, chaque fichiers de données (par pays) possèdent 16 colonnes de données :
- Id de la vidéo
- Date d’ajout de la vidéo
- Titre de la vidéo
- Titre de la chaîne postant la vidéo
- Id de la catégorie
- Heure de publication
- Mots clés
- Nombre de vues
- Nombre de likes
- Nombre de dislikes
- Nombre de commentaires
- Miniature
- Commentaires désactivés ou non (booléen)
- Évaluations/notes de la vidéo désactivées ou non (booléen) - Vidéo supprimée/bannie ou non (booléen)
- Description de la vidéo


Contexte et hypothèses :
Les vidéos à succès sur Youtube sont certes multiples mais présentent toutes certaines similitudes. L'objectif de beaucoup de "Youtubers" est de voir ses vidéos faire partie du Top Tendance.
Toutefois, cela demande une certaine popularité et un grand succès de la vidéo. Mais est-ce que ce succès est uniquement dû au contenu de la vidéo, ou bien à l'identité du Youtuber?
Il est certains que ces facteurs sont prédominants dans le succès de ces vidéos, mais sont-ils seuls paramètres; ou bien y a t-il d'autres facteurs permettant d'aider à la récompense de se retrouver dans ce top?
Tout ces questionnements nous ont donc amenés à l'hypothèse suivante:
Les vidéos top tendances cachent en réalité des facteurs de réussite autre que son contenu


Talend :
Nos données sont séparées en plusieurs fichiers (par pays), nous avons donc créé un job Talend qui permet de rassembler toutes les données en un seul CSV. Avec ce job on ajoute également plusieurs colonnes comme le pays où la vidéo a été en tendance, le taux en % de like / dislike et neutre d'une vidéo ainsi que convertir l'id catégorie par le nom de la catégorie.
Avec ce job le CSV final facilitera notre création de visuel ainsi que son implémentation dans d'autres algorithmes.

Power BI :
Nous avons utilisé le logiciel Power BI pour effectuer un premier set de graphiques qui vont nous servir dans exploration de données. Une fois un graphique validé et qui répond à notre problématique nous le mettons en forme sur CANVA (un site de création de design).

Algorithme Text Mining :
Disposant de données textuelles, nous avons réalisé un travail pointilleux de Text Mining sur les titres des vidéos qui semblaient être porteuses d'informations. Nous avons déterminer l'impact des mots présents dans le titre sur le nombre de likes/vues des vidéos et avons gardé l'impact sur les likes qui semblait bien plus révélatrice d'information.
Pour être étudiées, les données devaient d'abord être normalisées, puis nous étudions leurs impacts que ce soit bénéfique ou néfaste à la popularité de la vidéo.

Conclusion :
Cette restitution de données nous permet de constater que notre hypothèse s'est avérée juste et que la popularité d'une vidéo youtube ne repose pas uniquement sur son contenu vidéo mais aussi sur ses caractéristiques. C'est pourquoi il faut soigneusement préparer sa vidéo et l'adapter au public visé.
En effet, les vidéos tendances entre différents pays présentent de grandes disparités que ce soit au niveau des catégories, des heures de publications, ainsi que des mots à utiliser.
Certains mots sont à privilégier selon certaines catégories et pays; il faut donc minutieusement analyser le public souhaité pour savoir comment optimiser les chances de succès de la vidéo.
