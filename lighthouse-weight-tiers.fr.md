> Traduction communautaire (brouillon) — politique NTARI P2-002, Diffusion multilingue mondiale. Source : lighthouse-weight-tiers.md (original anglais, instantané du 2026-10-05). Brouillon communautaire assisté par machine, en attente de relecture par le mainteneur régional conformément à P2-002 §3.1. Les spécifications techniques essentielles restent en anglais conformément au §2.2.
>
> Vous avez remarqué une erreur de traduction ? N'hésitez pas à la corriger
> vous-même : forkez le dépôt https://github.com/NTARI-RAND/lighthouse et
> ouvrez une pull request. Les corrections de traduction sont des
> contributions précieuses, tout autant que le code.

> **Préséance.** L'original anglais est normatif. Cette traduction est proposée pour la lecture, non pour l'interprétation : là où elle diverge de `lighthouse-weight-tiers.md`, c'est l'anglais qui fait foi. Les mots-clés normatifs (MUST, MUST NOT, SHOULD, SHOULD NOT, MAY), les noms de champs, les étiquettes et les identifiants sont conservés en anglais, car ils constituent le contrat de conformité.

# Paliers de poids de Lighthouse — projet de spécification

Ce document est soumis à Janus-Facing Architecture. Un palier est un **fait structurel relatif à la corroboration**, jamais un verdict sur la vérité. Les paliers se comptent en **unités de hubs indépendants** : c'est le hub, et non le compte, qui constitue l'unité de comptage, l'indépendance étant lue structurellement et les hubs sous contrôle commun étant exclus. Les définitions des paliers relèvent de la **politique, non du mécanisme** — elles existent sous forme de données de politique comparables par diff et sont engagées dans le registre attesté par témoins avec des entrées de journal des modifications en langage clair, de sorte que la question « quelles règles de palier étaient en vigueur lorsque ceci a été restitué ? » ait toujours une réponse attestée. Toute restitution qui affiche un palier porte un justificatif : quelles réplications, quels hubs, quelle distribution de concordance, quelle version de la politique des paliers. Les assertions de connaissance et leurs réplications sont des **relations typées**, distinctes des signaux de commerce et d'arbitrage ; aucun lecteur ne peut les confondre.

---

## T0 — Ancré (Anchored)

Une assertion de connaissance existe dans le registre attesté par témoins sous la forme d'un triplet lié — **assertion de fait, procédure, résultat** — engagé par un déclarant en règle, dans un hub, selon la discipline ordinaire de la couche registre : en ajout seul, attestée par des témoins indépendants, monotone. L'ancrage n'engage **que des faits structurels et des références** : les hachages de contenu des trois artefacts, un type d'assertion, un identifiant de version de procédure, un horodatage, une référence pseudonyme au déclarant, une référence au hub. Les artefacts eux-mêmes — la procédure écrite, les données — entrent dans les communs de contribution sous AGPL, adressés par contenu et servis par les hubs ; le grand livre ne conserve que les hachages.

- L'ancrage est conditionné par le pacte : la réputation décide **si** un compte peut ancrer, jamais combien ni avec quelle visibilité.
- L'existence est le plancher, jamais une preuve. Un lecteur peut en déduire que cette assertion, avec cette procédure, existait à ce moment-là, émise par un compte alors en règle. Un lecteur NE peut PAS en déduire un examen, une plausibilité ou une vérité.
- Tout ancrage appelle une réponse. N'importe qui peut ancrer une contestation qui y fait référence ; le silence du déclarant accumule du dwell (délai enregistré) — un fait lisible, jamais un fait arbitré automatiquement.
- Un artefact devenu irrécupérable n'efface pas l'ancrage ; l'assertion est alors restituée comme « artefact-dark » (artefact indisponible), autre fait lisible.
- Un manquement ultérieur d'un déclarant au pacte **annote ses ancrages, sans jamais les effacer**. Un fabricateur peut avoir dit quelque chose de vrai ; les réplications de ses assertions reposent sur leur propre registre.

Surface d'abus : l'émission en masse. Défense : T0 ne dimensionne rien, tout ancrage est une exposition qui appelle une réponse dans le cadre du pacte, et un hub peut limiter le rythme des ancrages au titre d'une politique locale et publiée.

## T1 — Cité (Cited)

D'autres ancrages font référence à l'assertion. Les citations sont des **arêtes typées** — extends (prolonge), uses-procedure (utilise la procédure), disputes (conteste), mentions (mentionne) — et les types d'arêtes sont des données de politique. La citation restitue le **graphe de découverte** : c'est ainsi que les assertions sont trouvées, parcourues et contestées d'un hub à l'autre.

- Le nombre de citations MUST NOT entrer dans le poids, dans le classement à des fins de récompense ni dans l'éligibilité — **définitivement**, et non en attendant quoi que ce soit. Les citations sont, et resteront, presque gratuites à émettre ; un signal qui ne coûte rien ne peut rien pondérer.
- Une arête *disputes* est de première classe et est restituée à côté d'*extends*. Le graphe ne fait jamais de solde.
- Les surfaces de découverte MUST restituer la provenance — qui cite, depuis quel hub — afin qu'un cercle de citations soit lisible comme une forme. L'analyse du « trop propre » lit les sous-graphes fermés comme matière à signalement ; un signalement est un élément de contestation, jamais un retrait.

Un lecteur peut en déduire de l'attention et de la connectivité. Un lecteur NE peut PAS en déduire une corroboration. La citation permet de trouver les assertions ; elle ne les confirme jamais.

## T2 — Répliqué dans le hub (Replicated in-hub)

Un compte autre que celui du déclarant, inscrit dans le **propre hub du déclarant**, a exécuté une version précise de la procédure et a ancré une **réplication** : la référence à la version de la procédure, le hachage de son propre résultat et sa **déclaration de concordance** — cohérent (consistent), incohérent (inconsistent) ou non concluant (inconclusive) — laquelle est sa propre assertion appelant une réponse, contestable comme n'importe quel ancrage.

- Toutes les réplications d'un même hub **se ramènent à une seule unité-hub**, quel que soit le nombre de comptes. Ce regroupement est la défense contre les Sybils : les comptes fantoches n'achètent rien, et la mesure tient sans aucune détection de contrôleur.
- Les propres comptes du déclarant sont exclus ; lorsque le contrôle commun de comptes est structurellement visible, il est exclu lui aussi — mais c'est la règle de regroupement, et non la détection, qui porte la garantie.
- T2 apporte de la structure et de la restitution, jamais d'éligibilité. Sa fonction est celle d'une rampe d'accès : il prouve que la procédure est **exécutable par d'autres mains que celles de son auteur**, et il fait apparaître les défauts de procédure à peu de frais, avant que l'effort inter-hubs ne soit engagé.

Un lecteur peut en déduire l'exécutabilité et un intérêt local. Un lecteur NE peut PAS en déduire une confirmation indépendante — un hub partagé signifie un équipement partagé, une gravité sociale partagée, des angles morts partagés.

## T3 — Répliqué inter-hubs (Replicated cross-hub)

Des réplications ancrées existent depuis des hubs **structurellement indépendants** de celui du déclarant. Le palier porte un décompte en unités-hub — le nombre de hubs indépendants distincts comptant au moins une réplication ancrée — tenu **par catégorie de concordance** : « cohérent dans quatre hubs, incohérent dans un » est publié exactement ainsi, définitivement. C'est la règle de non-moyenne appliquée à la connaissance.

- L'indépendance est lue structurellement au niveau du hub : un contrôle distinct deux à deux. Opérateur commun, contrôleur commun, parent administratif partagé — exclus. **Les dix succursales d'un réseau de bibliothèques de comté forment une seule unité.**
- La relation de témoin n'est pas une relation de contrôle. Les hubs qui contresignent mutuellement leurs points de contrôle restent des corroborateurs indépendants ; sinon, des partenaires de fédération ne pourraient jamais se corroborer les uns les autres, et les petits réseaux mourraient étranglés à la naissance.
- Un hub n'est une unité comptable que tant que son propre registre est honnêtement attesté par témoins — au moins deux témoins indépendants, dont aucun ne repose sur les propres clés du hub. Les réplications d'un nouveau hub fonctionnent sous l'**étiquette de substitution** jusqu'à ce que son attestation par témoins soit réelle : une reconnaissance par étapes, exactement comme à la couche gouvernance.
- Une réplication réelle présente de la dispersion. Une concordance trop parfaite entre des hubs supposément indépendants est en soi matière à signalement par l'analyse — la signature des transactions fictives (wash trading) transposée à la connaissance.
- Une incohérence restée sans réponse accumule du dwell sur l'assertion d'origine — lisible, jamais un déclassement automatique.

Surface d'abus : les hubs fabriqués de toutes pièces, puisque l'AGPL permet à quiconque d'en monter un. Défense : le statut d'unité se gagne structurellement — registre attesté par témoins, exclusion du contrôle, étiquette de substitution jusqu'à la fédération — de sorte qu'un faux hub coûte ce que coûte un vrai hub.

## T4 — Attesté (Attested)

Un hub ancre, sous sa propre clé institutionnelle, une **attestation de survenue** : cette version de la procédure a été exécutée dans ces locaux, à cette date, au cours de cette session, par cette référence de compte. **La survenue, jamais la vérité** — le hub atteste l'événement qu'il a directement accueilli, non la conclusion. Le résultat du réplicateur et sa déclaration de concordance restent un ancrage distinct, qui lui est propre et qui y est lié.

- Une attestation mensongère est un manquement au pacte imputable au hub lui-même — arbitrable, lu comme une structure, et alimentant l'examen de la conduite de l'opérateur qui régit la réputation du hub. L'attestation a du mordant parce que la réputation d'une institution la soutient.
- Compté en unités-hub comme T3 : de nombreuses exécutions attestées dans un même hub forment une seule unité. Le nombre d'exécutions est restitué à titre de détail et ne dimensionne rien.
- **L'attestation est un service, jamais une permission.** Un hub peut refuser d'accueillir ou d'attester toute procédure — la planification, la supervision et le devoir de diligence ordinaire relèvent d'une politique locale au hub et publiée — et une assertion refusée ne perd rien ailleurs : elle s'ancre en T0, circule dans le graphe en T1, se corrobore inter-hubs en T3. La diligence ordinaire du lieu d'accueil accomplit un travail de sécurité sans qu'aucun centre ne devienne une autorité de vérité ou de contenu.
- Un hub MUST NOT attester des exécutions réalisées par des comptes placés sous son propre contrôle — son opérateur, son personnel agissant en tant que hub. À ce palier, l'emploi est une relation de contrôle ; une unité auto-attestée, c'est le renard qui compte les poules : elle compte pour zéro et porte l'étiquette.
- Le coût d'émission du palier se paie en **personnes présentes et en après-midi** — linéaire en nombre de hubs, sans économies d'échelle. C'est cette linéarité, et non une quelconque vérification d'identité, qui constitue l'économie anti-Sybil.

Un lecteur peut en déduire que des institutions indépendantes ont engagé leur réputation sur la survenue de l'événement. Un lecteur NE peut PAS en déduire que le résultat est correct — seulement que le falsifier coûte désormais à de vraies institutions de vrais après-midi, multipliés.

---

## Disciplines qui s'imposent à travers les paliers

- **Liaison à la version.** Une réplication est liée à la version de la procédure qu'elle a exécutée. Une procédure affinée est un nouvel ancrage citant l'ancien ; le poids s'accumule par version, avec la chaîne visible. Sinon, le poids s'accumule sur la v1 pendant que la v2 est discrètement livrée en dessous.
- **La concordance est une donnée ; le manquement est une conduite.** Une réplication incohérente est un fait de concordance, non une accusation, et elle n'est jamais acheminée comme une plainte pour préjudice. Seule la conduite — la fabrication, la présentation trompeuse de ce qui a été exécuté, une attestation mensongère — entre dans le circuit des plaintes du pacte. **Le désaccord n'est jamais un manquement.** C'est le maintien de ces deux canaux séparés qui empêche les plaintes pour préjudice de devenir l'arme des différends scientifiques.
- **L'éligibilité, jamais le dimensionnement.** Le statut de palier détermine si une assertion est éligible au flux entrant de l'économie ; le seuil — T3 et au-delà, ou T4 uniquement lors de la bascule — relève d'une politique gouvernée, et non de la définition des paliers. Le dimensionnement des versements appartient à l'échange réel qu'il finance, lequel porte la friction commerciale que les paliers ne peuvent pas porter.
- **Aucune restitution réduite.** Pas de score unique, pas d'étoiles, pas de badge « vérifié ». Un palier est restitué avec son justificatif : les réplications, les hubs, la distribution de concordance, la version de la politique en vigueur.

## Demandes à refuser ou à signaler

- *« Affichez le score global de l'assertion. »* → Reconstitue la moyenne que le pacte interdit. Publiez la distribution.
- *« Améliorez le classement selon le nombre de citations. »* → T1 ne dimensionne rien, définitivement.
- *« Laissez le hub attester les exécutions de son propre personnel. »* → De l'auto-attestation portant une clé institutionnelle.
- *« Laissez les hubs facturer un placement plus rapide ou dans un palier supérieur. »* → De la réputation vendue. La planification des attestations relève de la politique du hub ; le statut de palier ne s'achète jamais.
- *« Déclassez automatiquement en cas de réplication incohérente. »* → La concordance est une donnée. Restituez-la ; ne l'arbitrez jamais à l'horloge ni au décompte.
- *« Marquez l'assertion comme vérifiée en T4. »* → L'autorité de vérité sous un plus beau manteau. La survenue, jamais la vérité.
- *« Intégrez la réputation commerciale dans le poids de la connaissance. »* → Confond des relations typées. Un bon marchand n'est pas pour autant un bon déclarant.

## Résidu nommé

Exclusion géographique : les communautés sans hub participant ne peuvent pas atteindre T4, et n'atteignent T3 que par une inscription à distance — une lacune à contourner par la conception (journées d'attestation itinérantes, arrangements avec des hubs partenaires), jamais à accepter en silence. Démarrage à froid : de faibles nombres de hubs au début signifient une faible corroboration ; les étiquettes de substitution portent l'honnêteté jusqu'à ce que la fédération s'étoffe. Des cercles de collusion entre personnes réelles s'étendant sur plusieurs hubs restent possibles à un coût linéaire ; ils relèvent de la fraude — territoire du pacte — et chaque cas arbitré est un manquement qui ne se dilue jamais dans une moyenne.
