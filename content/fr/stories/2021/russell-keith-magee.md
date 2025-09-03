---
title: "Le parcours de Russell Keith-Magee vers l'open source"
date: 2021-10-05T19:07:35-07:00
draft: false
summary: "Russell Keith-Magee se connecte avec Open Source Stories pour parler de ses premiers souvenirs de technologie, raconter comment il s'est impliqué dans l'écosystème Django, et partager ses réflexions sur le contractualisme open source."
storyteller: "Russell Keith-Magee"
storycorps: "85873751"
bio: "Le Dr Russell Keith-Magee est le fondateur du projet BeeWare, développant des outils et bibliothèques GUI pour soutenir le développement de logiciels Python sur les plateformes desktop et mobiles. Il a également été membre de l'équipe principale de Django depuis 2006, et pendant 5 ans, était Président de la Django Software Foundation. Dans son travail quotidien, il gère les pipelines de données pour Upwave. Il est un conférencier fréquent aux conférences Python et Django à travers le monde, partageant ses connaissances et expériences en tant que développeur FLOSS, mainteneur de communauté, et fondateur de startup (non réussie)."
facilitators: ["amanda casari", "julia ferraioli"]
story_audio: "https://media.blubrry.com/1466155/content.blubrry.com/1466155/Russell_Keith-Magee_s_journey_to_open_source.mp3"
explicit: "no"
bytes: 37945722
tags:
- Python
- Compassion
- Django
- Community
---
**julia ferraioli** : Je m'appelle julia ferraioli, et mes pronoms sont elle/elle. Nous sommes le 5 octobre 2021. Et je parle avec Russell Keith-Magee, qui est un technologue engagé, développeur principal sur le projet Django, et le fondateur du projet beware. J'enregistre cette conversation pour open source stories dans un bureau plutôt spartiate que je n'ai toujours pas décoré après avoir déménagé. Et mon premier souvenir d'un ordinateur est en fait de jouer à Wheel of Fortune sur MS DOS, si vous pouvez le croire. C'était il y a longtemps. Et Russell, voulez-vous vous présenter ?

**Russell Keith-Magee** : Oui. Salut, je m'appelle Russell Keith-Magee. Je parle aujourd'hui depuis Perth, en Australie occidentale, qui est Whadjuk Nyoongar Boodja ; les Whadjuk Noongar sont les propriétaires traditionnels de la terre d'où j'enregistre. En raison des fuseaux horaires, c'est en fait le six octobre là où j'enregistre -- les fuseaux horaires, comment ça marche ? Mon premier souvenir d'un ordinateur est en fait mon père ramenant à la maison un Macintosh Apple original. Mon père était très passionné par l'expérimentation de nouvelles technologies farfelues et donc nous avions un Commodore64 dans la maison très très tôt.

Mais avant cela, avant que nous ayons celui-là, il avait eu pour un essai pendant un week-end un Macintosh original qu'il avait ramené à la maison et je me souviens vivement avoir découvert -- aucune idée de ce que j'allais faire avec cette chose -- mais j'ai découvert qu'il y avait un programme de peinture et vous pouviez dessiner et vous pouviez dessiner des choses avec de la peinture. Mais si vous aviez le pinceau le plus gros, et que vous coloriez tout l'écran entièrement en noir, et puis vous cliquez sur reset, il passerait par quelques nuances de niveaux de gris alors que la couleur disparaissait. Je ne sais pas pourquoi cela m'a époustouflé que vous puissiez faire cela. C'est assis dans le bureau de mon père regardant ses doigts se raser passer par des phases de gris qui amusait le moi de sept ans, je suppose.

**julia ferraioli** : Il me semble me souvenir d'effets comme ça moi-même, ainsi que de démarrer manuellement un économiseur d'écran. Qui bien sûr, si vous l'aviez laissé fonctionner trop longtemps, se graverait dans les moniteurs.

**Russell Keith-Magee** : Oui.

## Sur la compassion

**julia ferraioli** : Alors merci de vous joindre à moi aujourd'hui. Je suis vraiment excitée de discuter avec vous. Et je veux juste avoir une petite idée de votre parcours. Plongeons dans les trucs vraiment légers. Comme... quelles sont quelques leçons importantes que vous avez apprises dans votre vie ?

**Russell Keith-Magee** : Je suppose que c'est une leçon continue d'apprendre qu'il n'y a presque aucune situation où avoir de la compassion et de l'empathie pour les gens avec qui vous traitez, cela ne vous servira pas bien. Dans ma jeunesse, je peux me souvenir d'être beaucoup plus en colère et frustré contre tous ces autres gens stupides dans le monde qui ne comprennent tout simplement pas. En vieillissant, j'ai progressivement et parfois très douloureusement appris que ce n'est pas que tout le monde dans le monde est stupide. C'est juste que tout le monde dans le monde a un ensemble différent d'expériences et un ensemble différent de connaissances et un ensemble différent d'antécédents, un ensemble différent d'attentes. Le plus souvent, ce qui est perçu comme cette personne étant stupide, c'est juste que leur ensemble d'attentes entrant dans la situation sont radicalement différentes des vôtres. Se sortir de sa propre tête pour voir d'où ils viennent non seulement rendra le fait de traiter avec le monde beaucoup moins frustrant pour vous, mais peut souvent vous aider à arriver à l'objectif partagé que vous essayez d'atteindre beaucoup plus facilement.

Juste en vertu de cela, si vous comprenez d'où vient quelqu'un, il est beaucoup plus facile de présenter l'information d'une manière qu'ils vont pouvoir comprendre ou absorber ou reconnaître quoi que ce soit que vous disiez. Ce n'est pas pour dire que ce n'est pas incroyablement frustrant parfois quand vous êtes encore dans des conversations, mais cela m'a aidé à gérer ma frustration beaucoup plus de réaliser d'où viennent les autres personnes ou ne viennent pas d'un endroit d'essayer activement de me frustrer. C'est juste un accident du monde étant un endroit très grand et complexe et intriguant.

**julia ferraioli** : C'est une leçon fantastique. J'ai tendance à penser que les gens fonctionnent avec différentes variables d'environnement définies.

**Russell Keith-Magee** : Oui, oui. Et il y en a beaucoup, beaucoup et elles ne sont pas du tout documentées.

**julia ferraioli** : Non !

**Russell Keith-Magee** : Et assez souvent, ils sont même conscients des variables d'environnement sous lesquelles ils fonctionnent, ce qui fait partie de la frustration, je suppose. Mais oui, être conscient de ces variables environnementales est utile.

## Premières expériences avec l'open source

**julia ferraioli** : Excellent. Donc vous êtes très impliqué dans l'écosystème open source. Alors comment décririez-vous l'open source à quelqu'un qui ne le connaît pas ?

**Russell Keith-Magee** : Je suppose que je le décrirais comme un projet collectif où un groupe de personnes travaillent ensemble pour construire des solutions technologiques à un problème. Ainsi, en partageant, ils ne répètent pas le travail de chacun. Et ils peuvent apprendre des leçons de chacun. Si vous travaillez sur un système par vous-même, il y a une limite à ce que vous pouvez faire par vous-même. Si même deux petits groupes travaillent ensemble, il y a une limite à ce qu'ils peuvent accomplir par eux-mêmes. Mais si tout le monde travaille ensemble et partage ensemble, vous vous retrouvez avec une solution plus robuste, plus complète, parce que vous avez plus d'input dans ce qui est développé et ce qui est construit.

Donc c'est, à certains égards, l'antithèse de ce que le capitalisme moderne essaie de nous enseigner à tous de faire, qui vous savez cette idée que vous trouvez quelque chose dans lequel vous êtes bon et vous vous assurez de monopoliser le marché pour que personne d'autre ne puisse le faire. C'est cette idée que si nous contribuons tous ensemble, nous donnons tous un peu vers le projet. Tout le monde avance un peu plus loin en conséquence.

**julia ferraioli** : Un peu ce concept de bien collectif.

**Russell Keith-Magee** : Ouais.

**julia ferraioli** : Alors quelle a été votre première rencontre avec l'open source ? Comment en avez-vous pris conscience pour la première fois ?

**Russell Keith-Magee** : J'ai pris conscience de l'open source avant même que le mot open source soit une chose, donc ma première exposition était au milieu des années 90. Je bricolais avec un ordinateur et quelqu'un a fait le "Hé, hé, vous savez, avez-vous vu cette chose appelée Linux ?", et m'a passé une grande pile de disquettes que je pouvais installer sur mon ordinateur. Et il y a ce tout autre système d'exploitation qui était comme complètement différent de Windows. À ce moment-là, le logiciel libre était une chose. Et comme vous le faites habituellement, vous lisez tout le code autour ou la documentation et les déclarations de manifeste qui sont autour du logiciel libre. Et c'était une idée fascinante que c'est ce morceau de matériel, cette imprimante était frustrante. Alors les gens ont libéré le logiciel pour cela afin qu'ils puissent programmer leur propre imprimante comme, ouais, ça sonne bien. Comment puis-je en avoir plus de ça ?

C'était en quelque sorte le début de ma carrière universitaire au moment où j'étais, dans mes années d'honneur, le mouvement open source tel que nous le comprenons maintenant -- l'OSI [[Open Source Initiative](https://opensource.org)] et des groupes comme ça -- commençaient à formaliser ce qu'ils disaient, sous un nouveau récit sur ce que cela signifierait, qui n'était pas tout à fait dans les extrêmes de ce que la Free Software Foundation poussait mais dans une veine similaire.

**julia ferraioli** : Je vois. Vous avez parlé de Linux, mais y a-t-il eu un premier logiciel open source qui vous a vraiment fait adhérer à tout ça ?

**Russell Keith-Magee** : Je suppose que, si je devais mettre le doigt dessus, je dirais que c'était probablement le Bureau GNOME, encore, dans cette période de la fin des années 90, quand j'aurais dû passer beaucoup plus de temps à travailler sur ma thèse, mais c'était juste être intrigué par cette idée d'un bureau que vous pouviez construire et configurer et changer des choses