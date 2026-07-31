> Traduction communautaire (brouillon) — politique NTARI P2-002, Diffusion multilingue mondiale. Source : lighthouse-seed.md (original anglais, instantané du 2026-07-29). Brouillon communautaire assisté par machine, en attente de relecture par le mainteneur régional conformément à P2-002 §3.1. Les spécifications techniques essentielles restent en anglais conformément au §2.2.
>
> Vous avez remarqué une erreur de traduction ? N'hésitez pas à la corriger
> vous-même : forkez le dépôt https://github.com/NTARI-RAND/lighthouse et
> ouvrez une pull request. Les corrections de traduction sont des
> contributions précieuses, tout autant que le code.

# Le réseau Lighthouse — document fondateur

**Une application de Janus-Facing Architecture : des communs de la connaissance attestés par témoins, portés par des hubs civiques.**

Network Theory Applied Research Institute

Ce document est intégralement soumis à Janus-Facing Architecture. Il nomme des rôles et des mécanismes, jamais le logiciel qui les remplit ; chaque invariant de l'architecture mère s'y applique sans avoir à être répété, et là où ce document et JFA divergent, soit ce document est corrigé, soit JFA est amendée au grand jour. Son pendant normatif est **lighthouse-weight-tiers.md**, la spécification complète des paliers ; le présent document résume les paliers et ne les duplique pas — un miroir est une seconde source de vérité, dérivante dès sa naissance.

**Vocabulaire, rattaché aux rôles JFA.** Un **hub** est une institution civique — une bibliothèque, une école ou toute organisation qui fait tourner le logiciel — réunissant deux rôles JFA dans un seul paquet déployable : l'**orchestrateur** (le rôle de coordinateur/opérateur de JFA : l'application destinée aux membres, le journal en ajout seul propre au hub, ses obligations d'arbitrage) et le **témoin** (qui contresigne les points de contrôle des *autres* hubs). **LBTAS** est l'échelle d'évaluation du pacte — conçue pour faire remonter les préjudices, dérivée du rapport Leveson ; son développement reste à définir (problème ouvert 2). Un **ancrage** est l'engagement de faits structurels et de hachages dans le registre attesté par témoins. Une **attestation** est la déclaration signée d'un hub selon laquelle une exécution a physiquement eu lieu dans ses locaux — la survenue, jamais la vérité. Une **unité-hub** est l'unité de comptage de la corroboration : le hub, jamais le compte. Une **étiquette de substitution** signale toute garantie fonctionnant en dessous de son plancher structurel.

---

## Partie I — ce qu'est Lighthouse

Lighthouse est un ensemble de communs de la connaissance où les faits empiriques sont consignés **en même temps que les procédures qui les éprouvent**, qu'ils viennent de déclarants issus du monde universitaire ou non, ancrés à un registre attesté par témoins via des hubs locaux où le public peut discuter, répliquer et contester en communauté. Il instancie la partie VI de JFA : un registre attesté par témoins peut ancrer n'importe quelle affirmation empirique ou commerciale ; une fois ancrée, une assertion devient citable, et le pacte note le déclarant exactement comme il note un partenaire commercial. Les mêmes rails qui rendent le commerce digne de confiance rendent la connaissance digne de confiance.

Le nom est la discipline. Un phare ne certifie pas qu'une route est sûre ; il rend le danger visible et laisse la navigation au navire. Lighthouse éclaire les assertions — leurs procédures, leurs réplications, leurs litiges, la réputation de leurs déclarants — et ne rend jamais de verdict sur la vérité. Signalement, jamais verdict ; ancrer, jamais certifier.

Ce qu'il ne doit pas devenir, hérité mot pour mot : une agence de notation de la vérité, un marché publicitaire où la visibilité s'achète, un monopole de l'accréditation. La découverte reste fédérée, citée et contestable.

## Partie II — le modèle d'assertion

L'objet de connaissance atomique est un triplet lié : **affirmation factuelle, procédure, résultat**, ancré comme assertion, jamais posé comme fait.

- Le grand livre n'inscrit que des faits structurels et des références — hachages de contenu des trois artefacts, type d'assertion, identifiant de version de la procédure, horodatage, référence pseudonyme du déclarant, référence du hub. **Aucune donnée personnelle (PII) dans les communs**, jamais.
- Les artefacts eux-mêmes — texte de la procédure, données — entrent dans les communs de contribution sous AGPL, adressés par contenu, servis par les hubs. La provenance suit la règle entrant = sortant ; une contribution ne peut être reprise.
- Les assertions de connaissance, les réplications et leurs litiges sont des **relations typées**, distinctes des signaux de commerce et d'arbitrage. Aucun lecteur ne peut les confondre.
- Les réplications sont liées à la **version de la procédure** qu'elles ont exécutée. Un affinement est un nouvel ancrage citant l'ancien ; la réputation s'accumule par version, avec la chaîne visible.
- Tout ancrage appelle une réponse ; les contestations sont des arêtes de première classe ; le silence d'un déclarant accumule du dwell (délai enregistré) — lisible, jamais arbitré automatiquement. Un artefact devenu irrécupérable s'affiche en « artefact obscur » (artifact-dark) ; l'ancrage, lui, ne s'efface jamais.

## Partie III — le pacte appliqué

LBTAS note les **déclarants, jamais les assertions**. Une assertion n'acquiert de réputation que par la structure de corroboration de la partie V ; une personne n'en acquiert que par sa conduite.

- C'est la distribution complète qui est publiée, jamais une moyenne ; la note la plus basse est le manquement lui-même. Une fabrication ne se dissout jamais dans un volume confortable de bon travail.
- **La concordance est une donnée ; le manquement est une conduite.** Une réplication incohérente est un fait de concordance — cohérent, incohérent, non concluant — jamais une accusation, et elle n'est jamais acheminée comme plainte pour préjudice. Seule la conduite entre dans le circuit du pacte : la fabrication, la présentation trompeuse de ce qui a été exécuté, une attestation mensongère. **Le désaccord n'est jamais un manquement.** Cette séparation des canaux est ce qui empêche les plaintes pour préjudice de devenir l'arme du désaccord scientifique.
- Le pacte est symétrique : toute plainte appelle une réponse, les rejets annotent, et un manquement ultérieur annote les ancrages d'un déclarant sans les effacer — un faussaire peut avoir dit vrai, et les réplications de ses assertions tiennent sur leur propre dossier.
- Aucune autorité de vérité, nulle part : pas de « vérifié comme vrai » venant d'un hub, d'un centre, d'une analyse ou d'un modèle. Une aide à la lecture automatique explique ; elle ne certifie jamais.

## Partie IV — l'architecture des hubs

Un seul paquet, deux rôles, deux clés, **toujours tournées vers l'extérieur**.

- Chaque hub fait tourner l'orchestrateur et le témoin, mais **aucune institution ne témoigne de son propre journal**. Les points de contrôle de la bibliothèque A sont contresignés par l'école B et la bibliothèque C ; A leur rend la faveur sur les leurs. Les clés de témoin sont distinctes deux à deux et ne sont jamais celles de l'opérateur lui-même — un orchestrateur fusionné avec son témoin dans une même institution, c'est précisément l'opérateur qui s'atteste lui-même, ce que la couche registre existe pour empêcher.
- Une plainte pour préjudice visant un hub **se dépose auprès du témoin d'un hub voisin**, en amont, l'opérateur étant absent de la naissance de la plainte qui le concerne. Partout où deux hubs se fédèrent, l'écart de vivacité du dépôt se referme.
- **Plancher de lancement : deux hubs indépendants.** Un pilote à un seul hub n'est conforme que sous étiquette de substitution ; il ne peut pas se présenter comme une fédération.
- **Un lieu d'accueil, jamais une barrière.** Le registre et le marché vivent dans le protocole, en dessous de l'application de n'importe quel hub. Un membre refusé ou maltraité à la bibliothèque A entre dans l'application de l'école B avec sa réputation et sa liquidité intactes. C'est cette portabilité — et non la bonne volonté d'un hub quelconque — qui fait des hubs des lieux d'accueil plutôt que des gardiens.
- L'indépendance des hubs se lit structurellement : un contrôle distinct deux à deux, à l'exclusion d'un opérateur commun, d'un contrôleur commun ou d'un parent administratif partagé. **Les dix antennes d'un réseau de bibliothèques de comté ne font qu'une seule unité.** La relation de témoin n'est *pas* une relation de contrôle — des hubs qui contresignent mutuellement leurs journaux restent des corroborateurs indépendants, sans quoi les petites fédérations mourraient étranglées à la naissance.
- Marché cible : les bibliothèques et les écoles, avec des membres se connectant à l'application mobile ou web de leur hub. Sous AGPL-3.0, toute institution peut entrer sur le marché de l'orchestration des communs de la connaissance ; le copyleft, joint à l'échelle de lisibilité, maintient ce marché contestable, et pas seulement ouvert.

## Partie V — les paliers de poids, par renvoi

Le texte normatif vit dans la spécification qui accompagne ce document. La forme générale : **T0 Ancré** (l'existence est le plancher, jamais une preuve) → **T1 Cité** (rend le graphe de découverte ; le nombre de citations ne dimensionne rien, définitivement) → **T2 Répliqué dans le hub** (exécutabilité ; toutes les réplications au sein d'un même hub se ramènent à une seule unité-hub) → **T3 Répliqué inter-hubs** (corroboration comptée en unités de hubs indépendants, tenue par catégorie de concordance — « cohérent dans quatre hubs, incohérent dans un » est publié exactement ainsi) → **T4 Attesté** (la clé institutionnelle d'un hub engage sa réputation sur *la survenue, jamais la vérité* ; le coût d'émission se paie en personnes présentes et en après-midi, de façon linéaire).

Quatre disciplines s'imposent à travers tous les paliers : la liaison à la version ; la concordance-est-donnée-le-manquement-est-conduite ; l'**éligibilité, jamais le dimensionnement** — le statut de palier détermine si une assertion peut entrer dans le flux entrant vers l'économie, et ne dimensionne jamais un versement ; et aucune restitution agrégée — pas de score, pas d'étoiles, pas de badge « vérifié », chaque palier étant publié avec son justificatif.

## Partie VI — la posture face aux Sybils

Gérée jusqu'à ce qu'elle ne soit plus payante, jamais résolue : les deux outils qui pourraient la résoudre — une autorité d'identité mondiale et un mur payant — sont les deux choses que l'architecture refuse. Quatre mouvements :

1. **La corroboration compte des hubs, pas des comptes.** Exclusion du même contrôleur à chaque palier ; dix comptes fantoches dans une même bibliothèque se ramènent à la valeur structurelle d'un seul hub.
2. **La présence physique est le coût unitaire.** L'attestation fait que le palier le plus élevé coûte des personnes et des après-midi, de façon linéaire et sans économies d'échelle — la malhonnêteté est tarifée au-dessus de son rendement, non empêchée.
3. **L'analyse du « trop propre ».** Les sous-graphes de citation fermés, les cercles d'admiration mutuelle et une concordance suspectement sans dispersion entre hubs « indépendants » sont matière à signalement — un signalement contestable, jamais un retrait, parce que les faux positifs retombent sur de petites communautés de niche honnêtes, et parce que le lieu naturel de la contestation, c'est le hub lui-même, sur son propre plancher.
4. **Les récompenses séquencées derrière la bascule.** Au lancement, le poids ne dimensionne rien : ni classement, ni flux entrant. Le graphe s'accumule dans le registre attesté par témoins — les cercles construits tôt sont un effort perdu et restent définitivement visibles à toute analyse rétroactive. Le poids est ensuite activé par un changement de politique gouverné et attesté, pour les seuls paliers inter-hubs et attestés. Sybil avant le poids des citations : satisfait par l'ordonnancement plutôt que par la perfection.

Résidu nommé : une seule personne fréquentant réellement N hubs (le coût linéaire est la défense) ; les cercles de collusion entre humains réels s'étendant sur plusieurs hubs (fraude — territoire du pacte, chaque cas arbitré étant un manquement qui ne se dilue jamais dans une moyenne) ; la portée en paliers des membres à distance (problème ouvert 3) ; la faiblesse de la corroboration au démarrage à froid (les étiquettes de substitution portent l'honnêteté).

## Partie VII — le flux entrant vers l'économie

La connaissance ancrée et corroborée devient un intrant de R&D pour les produits et services des économies JFA — le rendement d'un cultivar, le mode de défaillance d'un outil, la courbe de coût d'une méthode, circulant des communs vers l'échange réel.

- Le statut de palier conditionne l'**éligibilité** au flux entrant ; le seuil — T3 et au-delà, ou T4 seulement au moment de la bascule — relève d'une politique gouvernée et attestée, non de la définition des paliers. Le dimensionnement des versements appartient à l'échange réel qu'il finance, lequel porte la friction commerciale que les paliers ne peuvent pas porter.
- **Jamais de placement payant.** Les assertions d'un fournisseur sur ses propres produits s'ancrent, se répliquent et se contestent comme celles de n'importe qui d'autre ; ce sont le pacte et l'analyse qui les surveillent, jamais des frais de référencement.
- Les invariants économiques de JFA s'appliquent en bloc : l'unité se gagne, elle ne s'achète jamais ; elle n'est pas convertible ; la dénomination n'implique pas la convertibilité ; et un examen réglementaire achevé avant toute phase de crédit.

## Partie VIII — l'ordre de développement

Construire de bas en haut ; l'ordre est l'argument. Chaque étape est livrée avec des étiquettes de substitution honnêtes.

1. **Étape 0 — le registre fédéré.** Pilote à deux hubs : journaux en ajout seul par hub, points de contrôle monotones contresignés mutuellement, preuves de cohérence, dépôt chez le voisin. C'est la construction à plus fort effet de levier de JFA elle-même (problème ouvert 2) habillée aux couleurs de Lighthouse ; rien de ce qui vient au-dessus ne se lit honnêtement avant qu'elle ne soit réelle.
2. **Étape 1 — ancrage et découverte.** T0 et T1 : le triplet d'assertion, le graphe de citations typé, la mise à disposition des artefacts depuis les communs AGPL. Sans rien dimensionner.
3. **Étape 2 — réplication et concordance.** T2 et T3 : comptage en unités-hub, distributions de concordance, restitution du dwell. Les justificatifs et les règles-comme-données-de-politique-comparables-par-diff sont livrés *ici*, comme fonctionnalités de lancement — la lisibilité est un livrable de construction, pas un vernis.
4. **Étape 3 — attestation.** T4 : clés institutionnelles des hubs, discipline de la survenue, règle d'exclusion du personnel, l'attestation mensongère alimentant l'examen de la conduite de l'opérateur.
5. **Étape 4 — la bascule du flux entrant.** Seulement après l'examen réglementaire et seulement pour les paliers inter-hubs et attestés, par un changement de politique gouverné et attesté.

## Partie IX — problèmes ouverts

1. **L'interface d'examen du registre n'est pas conçue.** L'examen du registre par les membres, via l'application de leur hub, hérite intégralement de l'échelle de lisibilité — des décisions qui s'expliquent au point d'usage, des règles qui vivent comme des données comparables par diff, des versions de politique attestées, des aides à la lecture automatique qui ne deviennent jamais des oracles. C'est la prochaine conversation de conception, et elle est nommée ici plutôt que contournée.
2. **LBTAS attend sa définition.** Le présent document la traite comme l'échelle d'évaluation du pacte, dérivée du rapport Leveson et destinée à faire remonter les préjudices ; son développement, ainsi que toute adaptation propre à Lighthouse des niveaux de l'échelle, restent à écrire.
3. **L'exclusion géographique.** Une communauté sans hub participant ne peut pas atteindre T4 et n'atteint T3 que par une inscription à distance. Des journées d'attestation itinérantes et des accords entre hubs partenaires sont des pistes de contournement possibles ; l'acceptation silencieuse n'en est pas une.
4. **La capture d'un hub, au-delà de l'analyse.** Des institutions réelles peuvent s'entendre ; la réponse est l'arbitrage plus l'examen de la conduite de l'opérateur, tous deux dépendant du caractère réel de la fédération — ce problème repose sur l'étape 0 exactement comme le problème 4 de JFA repose sur son problème 2.
5. **Tout ce qui figure dans la partie VII de JFA s'applique ici.** Les problèmes 2, 4, 7 et 8 en particulier. La conception du hub-comme-témoin propre à Lighthouse est un levier proposé sur le problème 8 — des institutions civiques comme témoins durables, publiquement responsables et mutuellement indépendants — à prouver en déploiement, non à présumer.

## La norme

Un système n'est Lighthouse que si les sept points tiennent tous ; s'il en manque un, c'est un autre logiciel qui porte le vocabulaire.

1. Les assertions sont ancrées comme des assertions ; aucun centre, aucune analyse, aucun hub, aucun modèle ne détient de verdict sur la vérité.
2. Les hubs sont des lieux d'accueil, jamais des barrières : le registre et le marché vivent en dessous de l'application de tout hub, et un membre quitte un hub pour un autre avec sa réputation et sa liquidité intactes.
3. Aucune institution ne témoigne de son propre journal ; deux hubs indépendants constituent le plancher de la fédération, et tout ce qui est en deçà porte l'étiquette de substitution.
4. La corroboration se compte en unités de hubs indépendants, jamais en comptes ; le nombre de citations ne dimensionne rien, définitivement.
5. Les distributions sont publiées entières — la concordance à côté du volume, le préjudice à côté de l'éloge — jamais sous forme de score agrégé ni de badge « vérifié », et chaque restitution porte son justificatif.
6. La concordance est une donnée et le manquement est une conduite ; le désaccord n'est jamais un manquement.
7. Le poids conditionne l'éligibilité et ne dimensionne jamais un versement ; chaque récompense se trouve derrière une bascule gouvernée et attestée, séquencée en traitant Sybil d'abord.

---

Pendant la mise en œuvre, le protocole de tension est en vigueur : dès que l'on constate qu'une contrainte est reformulée par commodité, qu'un substitut est livré sans étiquette ou qu'un problème ouvert est contourné — s'arrêter, nommer la tension, la rattacher à l'invariant ou au problème concerné, et proposer le geste conforme minimal. La faire remonter ; ne pas l'absorber.

*Ce document est une documentation libre relevant des communs AGPL-3.0 du projet ; il est fait pour être lu, réimplémenté et contesté.*
