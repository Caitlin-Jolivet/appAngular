4 'vercel -v' --> la version est la 21.1.0
5 'vercel -init' 'cd angular' 'vercel' 
7 'vercel list' --> angularapp-4joynsnd4.vercel.app
8 'vercel log angularapp-4joynsnd4.vercel.app' --> donne les données du déploiement
9 'vercel inspect angularapp-4joynsnd4.vercel.app' --> permet de récupérer des informations sur un déploiement
10 Les variables d'environnement sont des valeurs dynamiques "globale". 
Elles permettent d'injecter des valeurs que nous ne souhaitons pas placer directement dans notre code source et de modifier leur comportement en fonction de l'environnement dans lequel elles s'exécutent.
11 'vercel env add plain USERNAME production'
12 'vercel env ls'
13 Les secrets sont des variables d'environnement cryptées qui fournissent un moyen sûr de stocker et de partager des informations sensibles entre les déploiements. 
Ils sont utilisés pour les informations sensibles comme les mots de passe ou les jetons d'accès. Leur valeur ne peut être récupérée qu'au sein d'un déploiement
15 'vercel secrets add secret2 secret2'
16 Les environnements mis à disposition sont: Production (branche utilisée par l'environnement de production), Preview (environnement de mise en scene faisant référence à toute autre branche que la branche master), Development (branche pour développement local)
19 Une pull request permettent d'informer les autres des modifications apportées à une branche dans un dépôt sur GitHub. 
Les autres personnes travaillant sur le projet peuvent examiner discuter des changements avant qu'ils ne soient fusionnés dans la branche de base.
C'est l'environnement Preview qui est trigger
20 C'est l'environnement production qui est trigger. Versel a déployé angularapp-bdrt57qnc.vercel.app dans l'environnement Production.
21 La branche master correspond à l'environnement Production.
Les pull requests permettent à toutes les personnes de vérifier les changements et de résoudre les problèmes avant que ceux-ci soit mergé sur une autre branche.
Le workflow est le suivant:
 - création d'une nouvelle branche pour la fonctionnalité
 - réalisation de la fonctionnalité
 - merge de la branche parente (master) sur la branche de la fonctionnalité pour résoudre les éventuels conflits
 - création d'une pull request
22 Le serverless permet de déployer des fonctions sans serveur, c'est-à-dire des morceaux de code écrits avec des langages backend qui prennent une requête HTTP et y répondent.
Cela permet d'ajouter une logique côté serveur. L'interet est que  les fournisseurs de cloud computing tels que Vercels'occupent de tout, de la gestion des ressources au déploiement.




