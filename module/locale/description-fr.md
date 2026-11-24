# Improved Siegeengines

**Version** : 1.0.31

Dans le jeu d'origine, les engins de siège de l'IA se gaspillent d'eux-mêmes : les catapultes roulent jusqu'au pied de murs qu'elles auraient pu bombarder de loin, les tentes de siège s'éloignent toujours plus au fil de la partie jusqu'à ce que les trébuchets n'atteignent plus rien, les tours de siège attendent un mur jugé idéal et les boucliers mobiles poursuivent des cerfs. Ce module corrige chacun de ces problèmes.

Chaque point ci-dessous peut être activé ou désactivé séparément. Seuls les engins de l'IA sont modifiés, à l'exception de l'accostage et des passagers des tours de siège ainsi que des ingénieurs à l'huile, qui profitent aussi au joueur.

## Fonctionnalités

**Les catapultes et trébuchets choisissent leurs cibles.** Une catapulte ou un trébuchet de l'IA examine tout autour à portée maximale pour trouver le mur, la tour ou la porte ennemis les plus proches et tire depuis sa position. Les bâtiments civils ne sont visés que lorsqu'aucune fortification n'est à portée. Il n'avance que si absolument rien n'est à portée. (La recherche d'origine ne regarde qu'une direction à la fois et ignore les murs partiellement abîmés, d'où les catapultes collées aux remparts.)

**Arrêt en chemin pour tirer.** Le jeu ne cherche de cible qu'à l'arrêt, faisant passer les catapultes de l'IA devant des cibles à portée lors des raids ou marches. Désormais, une catapulte ou un trébuchet de l'IA en mouvement observe régulièrement autour de lui et s'arrête pour tirer dès qu'un mur, une tour, une porte ou un bâtiment ennemi est à portée.

**Passage à l'adversaire suivant.** Une catapulte ou un trébuchet ne vise que le joueur contre lequel son armée a été envoyée. Une fois ce joueur vaincu (son seigneur tué), il tire sur tout autre ennemi à portée au lieu de rester inactif.

**Autres ennemis à portée.** Quand rien du joueur assiégé n'est à portée, une catapulte ou un trébuchet tire sur les murs et bâtiments des autres ennemis au lieu de passer devant. Les cibles du joueur assiégé restent prioritaires ; les bâtiments déjà détruits ne sont jamais visés.

**Fin des tirs sur les ruines.** Un engin visant un bâtiment (baliste incendiaire ou catapulte) continuait de tirer sur l'emplacement vide après sa destruction, car le jeu ne vérifiait que le numéro du bâtiment. Désormais, une cible détruite est abandonnée et remplacée, balistes incendiaires incluses.

**Meilleure précision.** Le jeu autorise un rocher de catapulte de l'IA à tomber jusqu'à 12 cases trop court et 6 de côté, si bien qu'à longue portée la plupart tombent devant le mur. La dispersion est désormais réduite de moitié et centrée sur la cible (réglable ; 100 % conserve la précision d'origine). Vos propres engins restent inchangés.

**Réutilisation des emplacements de tentes.** Dès que la troupe partie de cet emplacement a disparu, que rien ne s'y trouve et qu'aucun ennemi n'est assez proche pour attaquer un engin là, l'IA peut y monter une nouvelle tente. Dans le jeu d'origine, un emplacement restait bloqué toute la partie.

**Placement des tentes selon la portée.** Les tentes de catapultes, trébuchets et balistes incendiaires sont posées là où l'engin atteint le château : entre 0 et 10 cases (réglable) en deçà de la portée depuis les murs, tours et portes ennemis, afin de toucher aussi l'intérieur.

**Les ingénieurs rejoignent toujours leur tente.** Si l'entrée d'une tente est bloquée, elle se déplace sur un côté libre et les ingénieurs ayant abandonné ou bloqués en chemin sont renvoyés, complétés par les ingénieurs inactifs à proximité. Une tente entièrement murée reçoit ses ingénieurs dès qu'un accès s'ouvre.

**Accostage des tours de siège élargi.** Si le jeu ne trouve pas de place, une tour accoste par son coin contre un mur diagonal, ou jusqu'à trois cases plus loin sur le même mur.

**Les tours de siège de l'IA trouvent leur propre mur.** Une tour inactive de l'IA se rend au mur ennemi accostable le plus proche (rayon de 100 cases). S'il n'y en a aucun ou que l'accès échoue, elle suit l'armée comme un grand bouclier — patrouilles, puis escorte de siège, puis armée principale, puis une troupe à distance aléatoire, puis renforts.

**Fantassins embarqués sur les tours de siège.** Sélectionnez des fantassins et cliquez sur l'une de vos tours : jusqu'à 9 montent dessus et tirent même en roulant (archers, etc.), protégés comme sur une tour accostée. Ils ne sont pas sélectionnables en trajet, meurent avec la tour ou y restent à l'accostage. Sélectionnez la tour et cliquez dessus : le premier clic débarque les passagers, le second les ingénieurs. Les tours de l'IA embarquent leurs tireurs dans un rayon de 3 cases.

**Les boucliers accompagnent leurs troupes.** Les boucliers de l'IA se répartissent équitablement entre combleurs de douves, engins à distance de l'armée d'attaque (jamais ceux de la défense du château) et troupes à distance. Les renforts n'en reçoivent qu'en dernier ; sans troupe, le bouclier attend sur place.

**Huile versée uniquement sur le sol.** Les ingénieurs — les vôtres inclus — ne versent l'huile que sur un sol dégagé où elle peut brûler, jamais sur un mur, un escalier ou une tour où elle se perdait. D'eux-mêmes, ils ne visent que des ennemis sur un tel sol. Envoyés ailleurs, ils versent sur le sol le plus proche dans un angle de 45 degrés ou gardent leur huile avec « emplacement impossible ».

**Écoulement de l'huile selon sa quantité.** Une marmite couvre un nombre défini de cases (41 par défaut) depuis le point visé. En terrain dégagé c'est identique au jeu d'origine ; dans un passage étroit elle s'étire comme plusieurs marmites successives. Les bâtiments inflammables (des masures jusqu'à l'armurerie, l'église et la cathédrale) perdent jusqu'à un tiers de leur vie là où l'huile les atteint ; murs, tours, portes et donjons restent intacts.

## Bon à savoir

* En multijoueur, tous les joueurs doivent utiliser ce module avec les mêmes réglages.
* Rien n'est enregistré dans les sauvegardes.
