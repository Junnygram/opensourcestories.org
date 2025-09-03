---
title: 'Joe Beda sur l'open source comme un jeu à somme positive'
date: 2021-10-21T19:11:04-05:00
summary: 'Joe Beda partage avec julia et amanda son histoire familiale multigénérationnelle avec les ordinateurs, son expérience changeante avec l'open source depuis la soumission du premier commit à Kubernetes, et comment l'avenir de l'open source contient à la fois "danger et opportunité".'
storyteller: 'Joe Beda'
storycorps: '85873754'
bio: 'Joe Beda est un Ingénieur Principal chez VMware. Joe organise la direction technique de Kubernetes à travers VMware et VMware Tanzu. Joe est arrivé chez VMware via l'acquisition d'Heptio, un leader du mouvement cloud native et une entreprise qu'il a co-fondée. Auparavant, chez Google, Joe a co-créé Google Compute Engine et a soumis le tout premier commit du projet Kubernetes. Joe a commencé sa carrière chez Microsoft en travaillant sur Internet Explorer et Windows. Joe détient un B.S. du Harvey Mudd College et vit à Seattle, Washington avec sa femme Rachel (médecin et également diplômée HMC) et leurs deux enfants.'
facilitators: ['julia ferraioli', 'amanda casari']
story_audio: 'https://media.blubrry.com/1466155/content.blubrry.com/1466155/Joe_Beda_on_open_source_as_a_positive_sum_game.mp3'
explicit: 'no'
bytes: 42813202
draft: 'false'
tags:
  - Kubernetes
  - Ownership
  - BDFL
  - Community
  - Governance
---

**amanda casari :** Bonjour, je m'appelle amanda casari. Mes pronoms sont elle/elle. Aujourd'hui, c'est le 21 octobre 2021. Je parle avec julia ferraioli et avec Joe Beda. julia, je la connais de notre projet, _opensourcestories.org_ et puis Joe, c'est la première fois que je rencontre, je suppose "en personne" en ligne. Nous enregistrons cette conversation pour Open Source Stories et je suis actuellement dans, ça ressemble à une grotte mais je promets que c'est un bureau, en Nouvelle-Angleterre qui a juste besoin d'un meilleur éclairage. Mon premier souvenir d'un ordinateur -- alors Joe, nous faisons toujours une question d'échauffement -- mon premier souvenir d'un ordinateur c'est quand mon oncle, qui travaillait pour IBM au début des années 1980, a donné à tout le monde dans la famille un PC pour Noël, et nous avons eu un IBM PC Jr. dans notre salon.

**Joe Beda :** J'avais aussi un PC Jr. à l'époque. Voilà. Jouer à King's Quest dessus, tu te souviens ?

**julia ferraioli :** Oh mon dieu, King's Quest ? Ouais.

**amanda casari :** Oui, absolument. julia, aimerais-tu passer en suivant ?

**julia ferraioli :** Bien sûr. Je m'appelle julia ferraioli. Mes pronoms sont elle/elle, et j'enregistre ceci depuis mon bureau. C'est la fin de ma journée et c'est charmant. C'est une excellente façon de conclure. Mon premier souvenir d'un ordinateur était, je pense, jouer à un jeu MS DOS et penser qu'ils étaient corrects. Mais tu sais, qu'est-ce qui était vraiment cool ? L'économiseur d'écran. Et j'aime les fractales depuis.

**Joe Beda :** Tu portes le nom d'une fractale, ou vice versa, non ?

**julia ferraioli :** Je pense que je vais adopter ça comme mon histoire d'origine. Oui. Joe, aimerais-tu te présenter ?

# La programmation informatique comme tradition familiale

**Joe Beda :** Ouais ! Je m'appelle Joe Beda. Voyons, aujourd'hui c'est le 21 octobre 2021, je parle avec amanda et julia ici. Je connais amanda depuis longtemps, nous avons travaillé ensemble chez Google. Et je veux dire, je connais julia depuis longtemps ! Alors amanda, c'est agréable de te rencontrer aujourd'hui. Voyons. Donc je suis dans mon bureau ici à Seattle. J'ai un écran vert derrière moi parce que mon bureau est un peu comme un placard. Tu vois, c'est comme des étagères de stockage et des porte-manteaux et des trucs comme ça, quand je lève l'écran vert.

Mon premier souvenir d'un ordinateur est, je ne sais pas, pour être honnête, parce que mon père était programmeur informatique. Il travaillait sur des mainframes IBM à l'époque quand je grandissais. Ce qui est bizarre, parce que ma plus jeune est programmeuse. Et elle est -- elle est une programmeuse informatique de troisième génération, ce qui est bizarre à penser. Mais je me souviens, je pense l'impact des ordinateurs plus que tout, mon père ramenait à la maison des cartes perforées, et nous les utilisions comme listes de courses et imprimions sur des imprimantes à chaîne, qui sont cette technologie d'imprimante folle, des bannières qui disaient Joyeux Noël ou peu importe. Mais je me souviens qu'il travaillait la nuit, parce que c'était quand le temps informatique était bon marché et il dormait pendant la journée. Je me souviens grimper sur lui comme un petit enfant et le garder éveillé. Il était probablement épuisé après avoir passé une nuit au centre de données. Donc, c'est ma première exposition aux ordinateurs, père épuisé.

**julia ferraioli :** Je pense que c'est quelque chose qui est un peu sorti de la mémoire récente à propos du temps informatique bon marché.

**Joe Beda :** Eh bien, je veux dire, nous avons des instances spot dans le cloud, non ? C'est vrai.

**julia ferraioli :** C'est vrai.

**Joe Beda :** Ce qui est vieux est nouveau.

**amanda casari :** Penses-tu -- Eh bien, je veux dire, penses-tu que c'est vraiment la différence là, alors ?

**Joe Beda :** Je suis désolé, tu as coupé une seconde, peux-tu répéter ? Penses-tu ?

**amanda casari :** Penses-tu que la planification est vraiment la différence alors, parce que je sais que pour, comme des amis qui utilisent des centres de calcul haute performance, ils doivent encore planifier pour la disponibilité et pour le temps de calcul.

**Joe Beda :** C'est la chose fascinante c'est que c'est une question de rareté. Non ? C'est comme, il n'y a qu'un nombre limité d'ordinateurs, et tu ne peux être utilisé qu'une fois. Je pense que tant de l'environnement informatique est vraiment post-rareté dans une certaine mesure, non ? Comme les ordinateurs sont, sinon bon marché, abondants, non. Mais il y a encore certaines choses comme, "hé, beaucoup d'ordinateurs dans un centre de données, calcul haute performance".

Tu sais, j'ai revu l'autre jour "Contact", le film. Il y a tout comme, la grande partie c'est que comme obtenir, du temps de télescope quand tu peux et le coût de ça et donc, c'est intéressant de penser à, comme, c'est un autre endroit où c'est que l'infrastructure est une ressource rare et seulement une seule personne peut l'utiliser à la fois. Donc ouais, je pense que ce sera toujours le cas dans une certaine mesure.

**julia ferraioli :** Quoi qu'il en soit, je me demandais si tu pouvais partager un peu ton parcours et comment tu es entré dans l'open source.

# Trouver un chemin vers l'open source

**Joe Beda :** Je ne sais pas, comme, donc la chose bizarre c'est que j'utilise l'open source parce que je pense que tout le monde dans notre industrie utilise l'open source, qu'ils le sachent ou non. Mais je n'avais pas fait beaucoup de contribution réelle à l'open source. Je pense que la plupart de ma carrière a été du logiciel commercial, travaillant dans de grandes entreprises.

J'ai commencé chez Microsoft en travaillant sur Internet Explorer. Certaines de mes premières réalisations -- il y avait Microsoft, à un moment donné, a reconnu que la sécurité était importante. Il y a eu tout ce branle-bas de combat où tout le monde a pris quelques mois de congé pour aller faire une revue de code d'un tas de trucs en cherchant des problèmes de sécurité courants. La chose sur laquelle je me suis concentré était, comme, les décodeurs d'images. Nous utilisions des choses comme "libpng" à l'époque, et une très vieille version de ça, et en regardant ça à travers le prisme de la sécurité. Donc c'était un de ces endroits où j'ai vraiment commencé à regarder profondément en termes de, comme, une dépendance, une dépendance open source. Avant ça j'avais installé Linux à l'université et ce genre de choses.

Mais je pense que la première fois que je me suis vraiment impliqué dans une communauté, honnêtement, c'était probablement Kubernetes, et démarrer ce projet. Et donc il y avait beaucoup d'apprentissage en cours de route. Mais je dirais --, j'ai donné cette interview l'autre jour, et comme, une des choses que j'ai dites là qu'ils ont retenues était "Le logiciel comme sport d'équipe." Et je pense, que tu travailles dans une grande entreprise, ou que tu travailles dans l'open source, je pense que beaucoup des compétences dans l'environnement sont transférables. Comme, tu peux dire aux gens quoi faire, mais c'est tellement plus efficace si tu peux travailler ensemble, trouver des objectifs partagés, et motiver les gens à travailler ensemble. Je pense que c'est souvent le cœur de ce qu'est l'open source. Je pense que ça a rendu la transition relativement facile pour moi quand j'ai commencé à contribuer, et quand nous avons fait décoller Kubernetes.

**julia ferraioli :** Ce petit projet qui, tu sais, n'a pas juste eu sa propre conférence ou quoi que ce soit ?

**Joe Beda :** Eh bien, ouais, mais l'autre chose c'est -- j'étais chez Microsoft quand j'ai fait quelques stages là-bas, et j'y étais pendant sept ou huit ans, tu sais. J'étais là quand, comme, il y avait la panique autour de "Linux est cette chose qui va tuer Microsoft". Et donc, de l'extérieur, je pense que nous avons tous regardé Linux prendre sa primauté en termes d'où il existe dans l'industrie, l'impact qu'il a eu. Et donc il y a définitivement au moins, de l'extérieur, tu vois ces modèles, et tu es comme, "Oh, voici à quel point ces choses peuvent devenir grandes." Donc c'était définitivement certaines des choses auxquelles nous pensions quand Kubernetes démarrait c'est que "hé, si cette chose réussit, le ciel est la limite." Mais ouais, il y avait beaucoup d'improvisation en cours de route aussi.

**julia ferraioli :** Donc Joe, tu as mentionné que tu vois l'ingénierie logicielle comme un sport d'équipe. Comment penses-tu que ça change ou ne change pas quand nous parlons de logiciel open source ? Penses-tu qu'il y a une différence matérielle ?

# Une évolution du "Logiciel comme sport d'équipe"

**Joe Beda :** Je pense que c'est une excellente question. Je pense que les compétences sont très transférables. Mais je pense que l'open source amplifie certaines de ces dynamiques. Comme, dans une entreprise, tu as une hiérarchie claire, tu as des objectifs d'entreprise clairs, tu as des incitations claires. Dans l'open source, c'est beaucoup plus... les gens viennent avec leurs propres motivations, leurs propres objectifs, leurs propres contraintes de temps.

Et donc je pense que l'art de motiver les gens et de les faire travailler ensemble devient encore plus important. Parce que tu ne peux pas juste dire "hé, fais ça parce que c'est ton travail." Tu dois vraiment convaincre les gens que c'est quelque chose qui vaut la peine d'être fait, et que c'est quelque chose qu'ils veulent faire.

**amanda casari :** Donc en pensant à Kubernetes spécifiquement, parce que c'est un projet que tu as aidé à démarrer, comment as-tu navigué ces défis de motivation et de coordination dans les premiers jours ?

**Joe Beda :** Ouais, c'est une excellente question. Je pense que nous avons eu de la chance à certains égards. Nous avions Google derrière nous, ce qui nous donnait une certaine crédibilité. Nous avions aussi une équipe de personnes qui étaient vraiment passionnées par le problème que nous essayions de résoudre.

Mais je pense que la chose la plus importante que nous avons faite était d'être vraiment transparents sur ce que nous faisions et pourquoi nous le faisions. Nous avons essayé d'être très ouverts sur nos décisions de conception, nos compromis, nos erreurs. Et je pense que ça a aidé à construire la confiance avec la communauté.

L'autre chose que nous avons faite était d'essayer d'être vraiment réactifs aux commentaires. Comme, si quelqu'un venait avec une idée ou une critique, nous essayions vraiment d'écouter et de répondre de manière réfléchie. Même si nous n'étions pas d'accord, nous essayions d'expliquer notre raisonnement.

**julia ferraioli :** C'est intéressant parce que tu mentionnes la transparence et la réactivité comme étant clés. Comment penses-tu que ces valeurs ont évolué au fur et à mesure que Kubernetes a grandi ?

**Joe Beda :** C'est une excellente question. Je pense que c'est devenu plus difficile à certains égards. Quand tu as un petit groupe de personnes, il est plus facile d'être transparent et réactif. Quand tu as des milliers de contributeurs et des millions d'utilisateurs, ça devient beaucoup plus difficile.

Je pense que nous avons dû développer des processus et des structures plus formels pour maintenir ces valeurs. Comme, nous avons des groupes d'intérêt spéciaux, nous avons des processus d'amélioration, nous avons des rôles de gouvernance plus formels.

Mais je pense que l'esprit est toujours là. Je pense que la communauté Kubernetes est toujours vraiment engagée à être ouverte et inclusive et collaborative.

**amanda casari :** En parlant de gouvernance, comment vois-tu l'évolution de la gouvernance dans l'open source plus largement ? Pas seulement Kubernetes, mais l'écosystème en général ?

**Joe Beda :** Je pense que nous voyons beaucoup d'expérimentation avec différents modèles de gouvernance. Le modèle traditionnel du "dictateur bienveillant à vie" fonctionne pour certains projets, mais je pense qu'il ne passe pas à l'échelle pour des projets vraiment grands et complexes.

Je pense que nous voyons plus de projets adopter des modèles de gouvernance plus distribués, avec des comités et des processus de prise de décision plus formels. Et je pense que c'est probablement une bonne chose, même si ça peut rendre les choses plus lentes parfois.

L'autre chose que je pense est vraiment importante c'est la durabilité. Comme, comment nous nous assurons que les mainteneurs ne s'épuisent pas ? Comment nous nous assurons que les projets peuvent continuer même si les contributeurs originaux passent à autre chose ?

**julia ferraioli :** C'est un excellent point sur la durabilité. Quels sont tes pensées sur l'avenir de l'open source ? Où vois-tu les plus grandes opportunités et défis ?

**Joe Beda :** Je pense que l'open source a gagné. Comme, c'est maintenant la façon par défaut de construire des logiciels dans la plupart des domaines. Et je pense que c'est fantastique.

Mais je pense que ça vient aussi avec de nouveaux défis. Comme, comment nous nous assurons que l'open source reste vraiment ouvert et accessible ? Comment nous nous assurons qu'il ne soit pas juste dominé par de grandes entreprises ?

Je pense aussi qu'il y a des questions vraiment intéressantes sur la sécurité et la chaîne d'approvisionnement. Comme, quand tout le monde dépend de l'open source, comment nous nous assurons qu'il soit sécurisé et fiable ?

Et puis il y a la question de la durabilité que j'ai mentionnée. Comment nous nous assurons que les gens qui font le travail sont soutenus et récompensés pour leurs contributions ?

**amanda casari :** Ces défis semblent assez intimidants. Qu'est-ce qui te donne de l'espoir ?

**Joe Beda :** Je pense que ce qui me donne de l'espoir c'est que je vois beaucoup de gens vraiment intelligents et passionnés qui travaillent sur ces problèmes. Et je pense que la communauté open source est vraiment bonne pour s'adapter et évoluer.

Comme, nous avons vu la communauté s'attaquer à des problèmes comme la diversité et l'inclusion. Nous avons vu des innovations dans les modèles de financement et de gouvernance. Je pense que nous continuerons à voir ce genre d'innovation.

Et au final, je pense que l'open source est fondamentalement à propos de personnes qui travaillent ensemble pour résoudre des problèmes. Et tant que nous avons des gens qui se soucient de ça, je pense que nous trouverons des moyens de surmonter ces défis.

**julia ferraioli :** C'est une note merveilleusement optimiste sur laquelle terminer. Y a-t-il autre chose que tu aimerais partager avec nos auditeurs ?

**Joe Beda :** Je pense juste que si tu es intéressé par l'open source, plonge-toi dedans. Trouve un projet qui te passionne et commence à contribuer. Ça ne doit pas être du code - ça peut être de la documentation, des tests, du design, de la gestion de communauté, peu importe.

L'open source est vraiment à propos de communauté, et la seule façon de vraiment le comprendre c'est d'en faire partie. Et je pense que tu trouveras que c'est une expérience vraiment enrichissante.

**amanda casari :** Merci beaucoup, Joe. C'était vraiment un plaisir de parler avec toi.

**Joe Beda :** Merci de m'avoir invité. C'était amusant.

**julia ferraioli :** Et merci à tous nos auditeurs. Nous vous verrons la prochaine fois sur Open Source Stories.