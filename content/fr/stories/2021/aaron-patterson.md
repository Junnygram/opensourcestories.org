---
title: "Aaron Patterson sur les changeurs de donne de l'open source"
date: 2021-10-14
draft: false
summary: "Aaron Patterson parle avec julia et amanda de l'installation de Linux pour la première fois, l'histoire derrière le premier patch, l'hésitation initiale autour du forking, et partage quelques conseils pour ses collègues programmeurs. Comprend beaucoup de mauvais jeux de mots de tout le monde."
storyteller: "Aaron Patterson"
storycorps: "85873752"
bio: "Aaron Patterson est un Senior Staff Engineer travaillant chez Shopify où il se concentre sur le développement du noyau Ruby et du noyau Rails. Outre ses réalisations en logiciel (qui sont à la fois nombreuses et grandes), il est connu pour son humilité, sa gentillesse, et ses accomplissements dans le domaine de la bio-écriture."
facilitators: ["julia ferraioli", "amanda casari"]
story_audio: "https://media.blubrry.com/1466155/content.blubrry.com/1466155/Aaron_Patterson_on_open_source_game_changers.mp3"
explicit: "no"
bytes: 38309764
tags:
- GitHub
- GPL
- Ruby
---

**julia ferraioli** : Bonjour, je m'appelle julia ferraioli. Nous sommes le 14 octobre 2021. Le temps n'a plus de sens. Je suis désolée. Je suis ici avec amanda casari et Aaron Patterson. Aaron est notre conteur pour aujourd'hui. J'enregistre cette conversation pour Open Source Stories dans mon bureau à Seattle, Washington, où il fait étrangement soleil en ce moment, ce qui est vraiment bizarre. Je vais passer le relais à amanda pour qu'elle se présente.

**amanda casari** : Salut, je m'appelle amanda casari. Je parle avec julia ferraioli et Aaron Patterson. J'enregistre cette conversation pour Open Source Stories. Nous faisons ce script à chaque fois ; cela pourrait être un peu répétitif, nous pouvons l'éditer, c'est bien. L'environnement dans lequel j'enregistre en ce moment est cette période vraiment effrayante en Nouvelle-Angleterre, où c'est juste avant Halloween, les feuilles ont déjà atteint leur pic et commencent à tomber. Il fait noir tôt. J'ai découvert que j'avais besoin de m'installer tard donc c'était une expérience vraiment effrayante. Mais je suis assez excitée de parler avec tout le monde.

**julia ferraioli** : Aaron, veux-tu nous parler un peu de toi ?

**Aaron Patterson** : Oui. Est-ce mon tour ? Mon nom est, désolé, je vais faire ça avec ma meilleure voix d'Ira Glass.

**julia ferraioli** : Parfait.

**Aaron Patterson** : Je plaisante. Je ne peux pas faire ça. Mon nom est Aaron Patterson, et je vous parle. D'où est-ce que je parle ? Qu'est-ce que c'est ? Je dis mon nom puis la date et d'où je parle ? D'accord.

**julia ferraioli** : Tu peux juste dire d'où tu parles -- c'est bien.

**Aaron Patterson** : Mon nom est Aaron Patterson. Nous sommes le 14 octobre 2021. Je parle depuis mon bureau dans ma maison à Seattle, Washington. Et oui, je peux confirmer qu'il fait un peu soleil dehors en ce moment. Oui.

**julia ferraioli** : Très étrange. Eh bien, merci beaucoup de nous rejoindre aujourd'hui. Maintenant, Aaron, je pense que je t'ai rencontré pour la première fois lors d'un meetup Ruby ici à Seattle. C'était il y a un moment.

**Aaron Patterson** : Oui. Oui, c'était le cas. J'essayais de me souvenir -- où nous sommes-nous rencontrés pour la première fois ? Et je ne peux pas me souvenir, parce que nous vivions dans le même quartier. Donc je te voyais tout le temps. Donc j'étais comme, "Oh, hé, alors où l'ai-je rencontrée pour la première fois ?" Ça devait être un meetup Seattle Ruby où nous nous sommes rencontrés pour la première fois.

**julia ferraioli** : Ouais, j'étais une totale novice -- je le suis toujours, pour être honnête.

Je me demandais si tu pouvais me donner une petite image de ta première expérience avec la technologie.

## Codes secrets et subversion des systèmes

**Aaron Patterson** : Oh là là. J'ai eu de la technologie autour de moi pratiquement toute ma vie. Ma mère est ingénieure électricienne. Donc quand je grandissais, nous avions toujours de l'électronique partout. Mon père est aussi ingénieur. Et j'ai appris beaucoup de technologie d'eux. En fait, quand j'étais enfant, j'étais vraiment passionné par les codes secrets. Parce que je voulais écrire du code, écrire des messages secrets à mes amis, vous voyez ? Ma mère m'a enseigné le binaire. Elle m'a dit "Oh, tu peux utiliser ça. Tu peux encoder ton message en uns et zéros, et puis le donner à tes amis." J'étais comme "c'est incroyable ! Fantastique !"

Donc je trouvais ça incroyable, mais essayer de convaincre mes amis de le faire à l'école, ça ne marchait pas. Aucun élève de CE2 ne va encoder des trucs en uns et zéros pour passer des petits mots en classe. Mais oui, j'ai eu de la technologie autour de moi pratiquement toute ma vie.

**julia ferraioli** : Je me souviens avoir appris les différentes bases quand j'étais enfant aussi. Je pense que j'ai eu une crise existentielle à ce moment-là. Donc bravo à toi de ne pas avoir eu de crise existentielle.

**Aaron Patterson** : Je ne me souviens pas exactement comment c'est arrivé, genre, elle m'a juste dit "ok, tu sais, tu peux faire tout ça avec des uns et des zéros." Et moi "quooooi ?!"

**amanda casari** : Ça me donne absolument de l'espoir parce que je n'ai pas eu ce genre d'exposition quand j'étais enfant, à la technologie, même si mes parents — ma mère faisait de la chimie et mon père était ingénieur naval. Je n'ai rien eu de tout ça. Mais je fais ce genre de trucs avec mes enfants. Genre "oh, tu demandes comment ça marche ? Asseyons-nous et parlons-en." Et mon aîné qui a 10 ans maintenant me dit des trucs comme "oui, mais pas de grande explication Maman".

**julia ferraioli** : Bonne définition des limites.

**Aaron Patterson** : Il faut juste d'une manière ou d'une autre transformer ça en code. Genre, comment peuvent-ils apprécier la technologie ou l'utiliser avec leurs amis ? L'utiliser pour subvertir les systèmes.

**amanda casari** : Je pense qu'on avait une bonne base avec Harriet l'Espionne, où certaines choses, même si le cadre était plus ancien, mais beaucoup de ce désir d'être Harriet l'Espionne avait des ramifications intéressantes.

**Aaron Patterson** : Laissez-moi vous apprendre un truc, clic droit -> Afficher la source [bruits d'explosion].

**julia ferraioli** : Ok, donc je suis très consciente de mes compétences en gestion du temps ici. Maintenant, Aaron, tu es assez actif dans la communauté open source... Quelle a été ta première rencontre avec ça ? Comment tu t'es impliqué ?

## Installer Linux, l'angoisse de `xf86config`, et le premier patch

**Aaron Patterson** : Je suppose que ma première rencontre en tant qu'utilisateur était probablement quand j'étais au lycée, genre j'ai installé Linux sur l'ordinateur de mes parents et je pense que c'est la première fois que je me souviens avoir vraiment eu des sueurs froides. Parce que c'était genre "Oh, et si je n'arrive pas à remettre Windows sur ce truc ? Et si j'ai définitivement cassé ce machin ?"

Donc quand je configurais Linux, et il y avait ce truc genre, à l'époque tu devais faire ce truc pour configurer X windows, tu faisais `xf86config`. Et je lisais toute la documentation. Et il y avait ce truc, c'était genre, ok, tu dois configurer la fréquence pour le moniteur... genre un réglage pour la carte vidéo ou le moniteur ou quelque chose. Et il y avait ce gros avertissement qui disait genre, si tu fais ça mal, tu peux littéralement griller l'ordinateur. Ça va le _griller_. Et moi "oh merde, j'espère que je vais pas foirer ça !" J'ai réussi d'une manière ou d'une autre.

Mais je prenais des cours de programmation au lycée. En cours, on utilisait le compilateur Borland C, et je ne voulais pas payer pour ça. Donc j'installais Linux pour avoir un compilateur C.

J'ai réussi à remettre Windows dessus. Donc c'était ok, mais bon sang, j'étais vraiment nerveux.

**julia ferraioli** : Un peu tendu ?

**Aaron Patterson** : Oui, oui, c'est sûr.

En tant que contributeur, je pense que j'ai fait ma toute première contribution en — je m'en souviens en 2001. J'étais programmeur Perl à l'époque. Je travaillais pour une entreprise appelée classmates.com. Que vous connaissez peut-être ou pas... certaines personnes plus âgées s'en souviennent peut-être... On avait un système où et — je sais que c'est mal, mais acceptez-le tel quel. On stockait tout le monde dans le système. Pour ceux qui ne connaissent pas, ce site web était basiquement comme un annuaire scolaire. Tu t'inscrivais et tu pouvais voir toutes les personnes qui avaient eu leur diplôme la même année que toi, et tu pouvais contacter les gens. C'est basiquement juste comme un registre de diplômés d'école. On stockait le nom de tout le monde en majuscules. Tu entrais ton nom, et peu importe ce que tu entrais, on le mettait juste en majuscules et on balançait ça dans la base de données.

Je me souviens que la raison à l'époque était parce qu'Oracle pouvait faire une recherche de texte sur les majuscules — si c'était tout dans la même casse, ça pouvait faire une recherche de texte plus rapidement. Donc ils faisaient ça. Mais bien sûr, quand tu regardais l'annuaire, personne ne voulait voir son nom en majuscules, non ? Donc bien sûr la meilleure solution pour ça était, on avait une bibliothèque Perl qui prenait les majuscules et essayait de deviner la casse, essayait de la mettre correctement en casse quand c'était affiché à l'utilisateur.

Le problème était — ça marchait plutôt bien, ça marchait ok avec la plupart des noms américains. Mais ensuite on a commencé à avoir beaucoup de Latino-Américains qui s'inscrivaient et ça ne marchait pas du tout pour eux. Donc ma première contribution open source était un patch à cette bibliothèque qui lui donnait un mode espagnol. Donc tu pouvais dire "ok, maintenant on veut ajuster ça pour le mode espagnol".

Et je pense que c'était ma toute première contribution open source.

**amanda casari** : Je peux demander — tu te souviens comment tu as eu la distribution Linux que tu as installée en premier ?

**Aaron Patterson** : Oh, ouais. CD dans un livre chez Barnes and Noble.

**amanda casari** : Et comment tu as contribué le premier patch ? Tu as envoyé un CD dans un livre ?

**Aaron Patterson** : Non, non, non, non. Il y avait des listes de diffusion. Je devais faire un patch, et puis l'envoyer à une liste de diffusion. Mais il n'y avait pas GitHub ou quoi que ce soit. Je ne pouvais pas trouver de dépôt pour ce truc du tout. Je devais basiquement juste le patcher et faire un diff et puis envoyer un diff par email à l'auteur et dire "hey, tu peux ajouter ça ?" Et puis ils l'ont fait.

**julia ferraioli** : Tu te souviens des commentaires de review que tu as eus pour ce patch ?

**Aaron Patterson** : Oh zéro. Donc j'ai juste envoyé un email à l'auteur avec un patch. Et je suis "Hey, on utilise ça au boulot. Et on a besoin d'un mode espagnol. Ça ne gère pas ces cas." Genre je leur ai donné une liste de noms. Je suis "ça ne gère pas ces cas, ça ne gère pas ces cas." L'auteur était basiquement "Oh, d'accord. Fait."

**julia ferraioli** : Très décontracté.

**Aaron Patterson** : Ouais, c'était un processus assez facile. Mais je dirais que c'était ma première contribution open source, et c'était probablement plusieurs années après ça avant que je fasse beaucoup d'autres contributions open source.

**julia ferraioli** : Tu sens que ça a tricoté ensemble le code qui t'a vraiment fait _toi_ ? Ta contribution à Perl ?

**Aaron Patterson** : Non.

**julia ferraioli** : Le pire jeu de mots de tous les temps.

**amanda casari** : Tiré par les cheveux. C'était un très bon étirement. Je pense que tu as laissé tomber quelque chose là-dedans, peut-être.

**julia ferraioli** : J'essaie juste de filer la métaphore.

**Aaron Patterson** : [Chuchotement] Ok.

**julia ferraioli** : Je m'excuse.

**Aaron Patterson** : C'est bon. C'est bon. Je veux dire, ça arrive dans beaucoup de cas. Il faut faire le changement.

**julia ferraioli** : Eh bien, dans cette veine, changeons un peu. Je sais qu'on t'avait envoyé quelques questions pour aujourd'hui. De quoi aimerais-tu parler ?

**Aaron Patterson** : Oh merde, c'était genre la seule question. "De quoi veux-tu parler ?" On peut parler de n'importe quoi. On peut parler de fabrication de fromage. On peut parler de fabrication de fromage. Mais je sais que c'est un truc open source. Donc on peut parler d'autres trucs aussi. Je ne sais pas. C'est une question tellement ouverte. Je n'ai aucune idée.

**julia ferraioli** : Mais réduisons un peu. Une des choses qu'on explore c'est les moments pivots dans l'open source ou l'évolution des contributeurs open source. Il y a un moment que toi ou l'industrie avez vécu quelque chose comme ça que tu aimerais partager ?

**Aaron Patterson** : OUI.

## La GPL

**Aaron Patterson** : Donc j'ai lu cette question, et j'ai aimé. Je suppose que je programme professionnellement depuis 1999. Donc je programme depuis longtemps et je suis impliqué dans la communauté open source depuis longtemps aussi. Donc j'ai vu plusieurs... il n'y a pas juste un pivot pour moi, non ? D'abord, je pense, si tu poses cette question à n'importe quel développeur open source, bien sûr, ils vont dire GPL. Ils sont obligés, tu dois dire celui-là, parce que c'était important. Parce qu'avant ça si on n'avait pas fait ça, on n'aurait probablement plus d'open source, ou on n'aurait pas eu d'open source au départ.

Donc je pense que c'était un moment pivot. Même si je pense que je suis trop jeune pour savoir... je ne suis pas assez vieux pour avoir été là avant et après la GPL. Genre j'étais là après la GPL. Mais je pense que c'est ce qui a vraiment poussé l'open source en avant. Pour moi, cependant. Je pense qu'on voit — eh bien, on l'a déjà vu.

Il y a deux autres points que je voulais faire après ça. Je pense que maintenant on voit un mouvement pour s'éloigner de la GPL. Donc ce n'est pas vraiment un truc pivot. C'est plus un arrière-plan. Il n'y a pas un moment unique, je ne sais pas comment décrire ça exactement, il y a eu un mouvement lent dans l'industrie pour s'éloigner de la GPL.

## L'ère GitHub, les listes de diffusion, et le forking

**Aaron Patterson** : Et ça se lie en quelque sorte au point pivot probablement le plus important pour moi dans ma génération de programmation, qui serait probablement GitHub. Juste parce que contribuer aux projets était tellement dur avant que GitHub existe ; tu devais connaître tous ces trucs. Tu devais être capable de comprendre genre, ok, qui est la bonne personne à qui envoyer un email ? Comment je mets ensemble un diff pour ce truc, et puis j'envoie un email à cette personne. C'est juste que la barrière d'entrée était tellement haute que, pour moi, GitHub était vraiment un moment pivot pour l'open source. Et je ne suis pas sûr de comment ça se rapporte au truc de licence, mais je sais qu'il y a deux trucs qui se passent là.

**amanda casari** : Tu te souviens quand les projets qui t'intéressaient le plus et/ou auxquels tu contribuais ont migré vers GitHub ?

**Aaron Patterson** : Rails est probablement le plus gros. Avant on utilisait subversion sur notre propre truc hébergé, je pense qu'on avait notre propre serveur hébergé. Et puis on a migré ça vers GitHub, et c'était important. C'était super sympa ; s'éloigner de ton propre truc hébergé c'est juste, juste génial [rires]. Mais en plus de ça, avec les autres trucs, genre les pull requests, ça n'existait pas.

Aussi je me souviens d'un truc, quand GitHub est arrivé, ils ont dit "tu forkes un projet", et à l'époque, j'étais genre "Whoa, tu peux forker un projet. Tu peux pas faire ça. C'est pas légal." [Plus de rires.] Parce qu'avant ça forker un projet c'était important. Si tu forkais le projet de quelqu'un ça voulait dire que tu étais genre "Non, vous êtes les pires. Je vais plus jamais travailler avec vous. Je forke votre projet !" Et maintenant GitHub arrive et genre "Non, tu forkes juste. Tu fais tes changements, et tu renvoies juste..."

**julia ferraioli** : J'ai l'impression qu'il y a encore le fork minuscule et le Fork majuscule.

**Aaron Patterson** : Je pense. Je pense que dans mon esprit, avant GitHub, il n'y avait pas de fork minuscule. Il y avait que des patches, juste envoyer des patches, non ? Il n'y avait pas de fork minuscule. Juste faire ton travail. Envoyer un patch quelque part. Et puis GitHub nous a donné celui en minuscule. Maintenant tu peux le faire. Maintenant tu peux faire un gros fork.

**julia ferraioli** : C'est la fourchette à dîner versus la fourchette à salade.

**Aaron Patterson** : Exactement, oui.

**amanda casari** : C'est comme ça qu'on sait qu'on est dans le bon endroit ou le mauvais endroit.

**Aaron Patterson** : Le problème c'est que je ne sais jamais quelle fourchette utiliser. Donc genre, et si j'utilise accidentellement la grosse fourchette ?

**julia ferraioli** : Je suis sûre que la communauté te le dira.

**amanda casari** : Est-ce que ça semblait un peu impoli la première fois que tu as fait le fork ?

**Aaron Patterson** : Oh, non, non, ça ne l'était pas. Une fois que quelqu'un m'a expliqué le workflow, j'étais genre "Ok. Ouais, c'est bon. C'est bon. C'est juste un mot. C'est ok." Mais je me souviens avoir pensé genre "oh merde, est-ce que c'est ok de faire ça ?"

**julia ferraioli** : Quand GitHub a été lancé pour la première fois, ils n'étaient pas vraiment focalisés sur l'open source. Non ? Plateforme de codage social ?

**Aaron Patterson** : Je pense que c'est vrai. Ils étaient juste une plateforme de codage social. Mais je veux dire, je ne sais pas ce que tu serais d'autre. Si ça va être social, ça doit être open source, basiquement. Non ? Surtout si tu lances juste un site web, qui d'autre va l'utiliser ? Tu peux pas coder socialement ton projet closed source. Genre, comment c'est social ?

**julia ferraioli** : Ta plateforme de codage anti-social ?

**Aaron Patterson** : Oui.

**julia ferraioli** : C'est vrai. Mais l'avènement de cette plateforme user-friendly qui faisait que tu n'avais pas à envoyer un email à l'auteur de la bibliothèque avec un patch, parce que tu ne sais pas où est le dépôt, c'était un changement énorme pour l'open source, et l'industrie open source.

**Aaron Patterson** : Avant ça on avait SourceForge, qui était un peu comme ça, mais ils n'offraient pas... L'offre principale de GitHub était une pull request, genre c'était **_le_** truc. Tu ne pouvais pas faire ça sur SourceForge. Ils avaient l'hébergement, mais tu devais encore envoyer un patch par email quelque part. Et aussi, à l'époque, SourceForge essayait de monétiser. Donc ils sont juste devenus couverts de pubs. Je ne sais pas si c'est approprié pour ça.

**julia ferraioli** : Ma première expérience avec l'open source était sur SourceForge. Et tu devais faire très attention où tu cliquais.

**Aaron Patterson** : Tu te souviens — ils avaient des boutons de téléchargement, qui étaient totalement de faux téléchargements. C'étaient basiquement des pubs ou quelque chose genre "comment c'est, comment c'est légal ? Ça ressemble vraiment à un appât et changement de dernière minute genre tu ne devrais pas faire ça." Donc je pense que ça a donné à GitHub un énorme avantage parce que c'était genre "oh, hey, ce site web n'a pas de pubs partout."

**amanda casari** : Donc je suis curieuse Aaron, donc quand les projets ont commencé à migrer vers GitHub, si tu n'envoyais plus de patches par email aux gens, est-ce que les listes de diffusion étaient encore aussi actives ou aussi riches pour la conversation qu'elles l'étaient avant ? Ou avaient-elles changé ?

**Aaron Patterson** : C'est une très bonne question. Je pense qu'elles ont basiquement diminué au fil du temps. Je veux dire, quand GitHub a été lancé pour la première fois, ouais, bien sûr, les listes de diffusion continuaient et tout ça tu envoyais des emails à beaucoup de gens et c'était amusant. En fait, les listes de diffusion et IRC — c'est quelque chose que je regarde avec nostalgie ; c'était très amusant. Mais ces trucs sont tellement durs à utiliser que j'ai l'impression qu'ils sont moins inclusifs, si ça a du sens. Mais ouais, je pense que l'activité des listes de diffusion a définitivement diminué au fil du temps. Je veux dire, j'étais sur la liste de diffusion Ruby. Je ne le suis pas. Je n'ai pas lu la liste de diffusion depuis longtemps [rires]. Je déteste l'admettre mais...

**julia ferraioli** : Vous l'avez entendu ici, les gens.

**Aaron Patterson** : Oui, je lis la liste de diffusion ruby-core, mais pas vraiment. Donc la liste de diffusion ruby-core est basiquement juste un miroir de notre site web. Genre le site web de suivi des issues. Je lis juste le site web de suivi des issues. Je n'aime pas l'email. Je reçois trop d'emails, si tu regardes mon téléphone, il dit que j'ai plus de 10 000 emails non lus. Et je regarde ça, et je suis genre "voyons si on peut atteindre 11 000." [Rires.]

**julia ferraioli** : Ça ressemble à mes notifications GitHub.

**Aaron Patterson** : Oh, ouais. J'ai abandonné ça il y a longtemps. Le prochain GitHub sera GitHub, mais sans notifications.

**julia ferraioli** : Donc quels autres types de changements tu as vus avec l'avènement et l'adoption de GitHub ?

**Aaron Patterson** : Je ne sais pas. Je veux dire, plus de CI, la CI n'existait pas. Beaucoup de gens ont essayé de faire de la CI, mais personne ne pouvait la rendre profitable. Je suppose que jusqu'à ce que Travis arrive, je pense qu'ils étaient la toute première entreprise à réussir à faire de la CI et à survivre. Il y avait eu un tas d'autres entreprises avant ça dont je me souviens qui avaient des offres d'intégration continue, mais elles ont toutes fait faillite. Donc ouais, il y a ça.

D'autres trucs qui ont changé ? Je ne sais pas. IRC qui meurt. Maintenant, au lieu d'utiliser IRC, on peut utiliser Slack. Et c'est basiquement comme IRC sauf que c'est lent et ça utilise toute ta mémoire. Je suppose que tu sais de quoi on devrait parler, on devrait parler d'éditeurs. Parce que c'est quelque chose qui a énormément changé au fil du temps. Je pense, cependant, que je suis une personne triste. J'utilise vim depuis 20 ans.

**amanda casari** : Je pense que c'est depuis combien de temps julia y est piégée. Donc elle apprécierait vraiment une sortie.

**Aaron Patterson** : Vim, je ne peux pas te quitter.

**julia ferraioli** : Eh bien, en fait, je suis dans vim. Mais c'est vim à l'intérieur d'Emacs. Je ne sais plus vraiment où je suis. Eliza m'aide à sortir.

**Aaron Patterson** : C'est quoi ce film où ils continuent à aller plus profond ? C'est Inception. vim, Emacs, Inception.

**amanda casari** : Oui. Inception d'éditeur.

**julia ferraioli** : Mais les éditeurs plus user-friendly, surtout avec diverses intégrations ? Révolutionnaire.

## La révolution des éditeurs

**Aaron Patterson** : C'est sûr. Je pense qu'une des meilleures choses qui soit sortie récemment, à mon avis, c'est VSCode. Je pense que c'est génial. Je ne l'utilise pas, mais je pense que c'est vraiment incroyable pour la communauté de développement, et la communauté open source en général, non ? Je vais admettre, vim n'est pas facile à utiliser. Ce n'est pas facile à utiliser, mais c'est celui que j'utilise. Et c'est celui avec lequel je veux rester. Mais que quelqu'un soit sorti et ait développé un éditeur que les nouveaux peuvent utiliser et s'habituer et s'impliquer dans la programmation. C'est important pour moi. Je pense que c'est vraiment, vraiment génial.

**amanda casari** : Je pense que c'est intéressant aussi, surtout en entendant ton expérience avec ta première installation open source, et comme c'était effrayant de penser "Et si je détruis la technologie que j'essaie en fait de changer ou avec laquelle travailler". Mais tellement d'outils, surtout ces dernières années maintenant ont cette capacité d'avoir de l'interopérabilité, et de l'intégration, et de pouvoir construire ces chaînes et workflows, avec une bonne documentation. Donc que ce ne soit pas ce processus mystique semble vraiment révolutionnaire. Ça change beaucoup de pouvoir faire des choses sans avoir nécessairement besoin de quelqu'un qui ne peut pas l'aborder depuis le début ou être nouveau dans la communauté ou venir et poser de bonnes questions éduquées en cherchant des trucs sur comment contribuer mais n'a pas à apprendre un code secret ?

**Aaron Patterson** : Absolument. Je suis totalement d'accord. C'est tellement bien, avoir ces outils qui sont faciles à utiliser. Je suppose que je suis un énorme fan des trucs qui baissent la barrière d'entrée. Donc GitHub est un de ces trucs et ces nouveaux éditeurs, c'est un autre truc. Et je pense que ça va juste s'améliorer. Je n'ai aucune idée comment, genre, je ne peux pas imaginer. Je ne sais pas comment on va baisser la barrière plus. Mais je pense qu'on va continuer à la baisser. Et je pense que c'est une bonne chose.

**julia ferraioli** : Génial. Merci, Aaron. On a juste 10 minutes qui restent. Je sais, tu t'inquiétais de la durée. Donc on vient de couvrir les prédictions, ou leur absence peut-être. Où vois-tu certains des problèmes non résolus dans l'open source ? Les défis ?

**Aaron Patterson** : J'ai lu cette question. Je ne sais pas ; c'est dur. C'est dur à dire. Une des choses que j'ai écrites c'est, eh bien **_le truc_** que j'ai écrit c'est la durabilité de l'open source. Parce que beaucoup de gens font de l'open source sur leur temps libre, et je ne pense pas que ce soit vraiment durable. Quand j'ai commencé à faire de l'open source... Donc en 2001, j'avais 21 ans. Je suppose que j'avais 20 ans. Je n'étais pas marié, je pouvais juste faire tu sais, j'avais beaucoup de temps libre. Et beaucoup de gens n'ont pas ce luxe. Donc je pense que c'est un très gros défi de l'open source c'est comment on peut donner aux gens ce temps pour y mettre ? Je n'ai pas vraiment de bonnes solutions pour ça. Chaque avenue que j'ai recherchée pour ça a des problèmes. Donc je ne sais pas. Mais je pense que c'est un défi. Et si on peut casser cette noix, je pense que ça aidera beaucoup.

**julia ferraioli** : C'est définitivement un problème non résolu. Je pense que beaucoup de gens ont diverses pensées. Et, ouais, je ne pense pas qu'on ait une solution qui adresse toutes les préoccupations.

**Aaron Patterson** : Non, je veux dire, il y a diverses — en ce moment mon boulot de jour c'est que je fais de l'open source. Ça m'a pris beaucoup, beaucoup d'années, mais j'ai finalement trouvé une entreprise qui est genre "Oui, on va te payer pour faire de la programmation open source". Mais tout le monde ne peut pas faire ça. Donc quoi d'autre ? Comment on peut faire payer les gens autrement ? Ou comment on donne du temps libre aux gens ? Ouais, je n'ai pas de bonne réponse. C'est un sujet difficile.

**julia ferraioli** : On est tous assez privilégiés, dans cette conversation d'avoir l'open source comme partie de nos boulots. Mais c'est définitivement pas comme ça pour tout le monde. Et je sais qu'un des problèmes qu'on voit c'est que de plus en plus ton CV open source est considéré comme un composant d'embauche. [Gémissements.]

**Aaron Patterson** : Ouais, ça me tue.

**amanda casari** : C'est le mois parfait pour parler de ça aussi.

**Aaron Patterson** : Je n'aime vraiment pas quand les gens utilisent l'open source comme un CV. Je veux dire, certains des meilleurs programmeurs que je connaisse, ils ne font pas d'open source, mais ils sont vraiment géniaux. Ils sont vraiment géniaux. Ce sont de bons ingénieurs. Donc tu sais, pourquoi ? Pourquoi on a besoin de ça ?

**amanda casari** : Donc j'ai une question pour vous deux alors. J'ai vu l'open source comme un excellent moyen d'avoir un CV public est genre un des incitants que j'ai vus pour les gens qui cherchent à percer dans la tech ou cherchent à être embauchés par certaines entreprises ou postes. Donc j'ai l'impression que ça se vend parfois comme ça pour les gens parce qu'il y a une idée que ça a un avantage et peut-être que ça en a même pour faire une première contribution, c'est genre "oh, fais une première contribution. Maintenant tu as un CV public, les gens voient que tu comprends les outils". Est-ce que vous sentez que... est-ce que ça est venu parce que ça résolvait un problème plus tôt ? Ou avant ? Est-ce qu'à un moment c'était quelque chose qui résolvait vraiment le problème qui existait avant qui n'existe juste plus maintenant ? Ou est-ce qu'on a trouvé que c'était une mauvaise pratique parce que c'était tellement exclusif ?

**Aaron Patterson** : C'est une très bonne question. Donc pour te donner un peu de contexte sur moi de mon expérience. Une de vos questions était "qu'est-ce que tu regrettes ?"

**julia ferraioli** : Sympa et léger.

**Aaron Patterson** : Oui. Très léger. Une des choses... une raison pour laquelle j'ai commencé à contribuer à l'open source c'est qu'un de mes regrets c'est que je n'ai pas fini l'université. Donc quand les gens essaient de, ou quand tu cherches un boulot ? Je veux dire, je veux être programmeur. Mais comment tu peux prouver aux employeurs potentiels que c'est quelque chose que tu peux vraiment faire ? Et l'open source est un moyen de prouver ça. C'est genre "eh bien, je n'ai pas d'expérience de boulot, mais tu peux voir que j'ai fait XYZ". Et je veux dire, je ne sais pas. Je pense que c'est un bon moyen de démontrer que tu as les compétences même si tu n'as pas l'historique de boulot, mais j'admets, à cette époque, j'avais beaucoup de temps libre, donc j'ai pu faire ça.

**julia ferraioli** : Donc je vais prendre la voie facile et blâmer le fait qu'on n'a que quelques minutes qui restent pour passer sur la question, et te demander, Aaron, est-ce que tu as des pensées de fin pour les gens qui écoutent ou lisent ?

**Aaron Patterson** : Pensées de fin ? Mon dieu, je peux juste descendre toute la liste de trucs — j'ai lu toutes les questions, et j'ai répondu à toutes les questions. Est-ce que je devrais juste y aller ? Je vais passer par chacune d'elles. Je n'ai pas fait de pensées de fin cependant, donc je ne sais pas.

## Pensées de fin

**Aaron Patterson** : J'ai une bonne pensée de fin pour vous : L'océan. [Pause, puis rires.] Non, Non, Non, je plaisante. Je plaisante. Donc c'est juste une blague. Je suppose que j'ai beaucoup de pensées de fin. Une chose. Bon sang, je ne peux pas choisir, c'est tellement dur pour moi de choisir juste une. Donc peut-être que je vais en débiter quelques-unes.

Une en revenant au truc d'éditeur. Un conseil que j'aimerais donner aux gens qui sont programmeurs, aux gens qui veulent être programmeurs, ou sont programmeurs c'est peu importe quel éditeur tu utilises, mais apprends-le bien. Apprends comment bien utiliser l'éditeur. La raison pour laquelle je dis ça c'est parce que de mon expérience j'ai utilisé vim plus longtemps que j'ai utilisé n'importe quel langage de programmation. Et je peux faire n'importe quel langage de programmation dans cet éditeur. Donc pour moi le truc qui est probablement la pièce de technologie la plus importante sur mon ordinateur c'est cet éditeur, donc peu importe lequel tu utilises, apprends-le. Je pense qu'on manque de temps ici... une pensée de fin... genre quelque chose de profond...

**julia ferraioli** : Eh bien, je pense qu'une bonne pensée de fin c'est de te remercier de nous avoir rejoints aujourd'hui.

**Aaron Patterson** : Oui, mon autre pensée de fin c'est mes cheveux. [Silence]

**julia ferraioli** : Ça a été un délice absolu. Merci.

**Aaron Patterson** : Merci, j'ai passé un bon moment.

**julia ferraioli** : Et j'espère qu'on pourra te ravoir bientôt.

**Aaron Patterson** : Moi aussi. J'adorerais, merci.

**julia ferraioli** : Merci _toi_.

**Aaron Patterson** : ....et, coupez.