# Suivi du mentorat — kickoff_dev

> Fichier tenu à jour par le mentor. Lu au début de chaque session.
> Dernière mise à jour : 2026-10-01 (session 2)

## 1. État actuel

| Élément            | Valeur                                              |
|--------------------|-----------------------------------------------------|
| Phase              | A — Conception                                      |
| Étape              | A.1 — Cadrage v2 relu ; validé sous 4 conditions → rédaction de `docs/conception/01-cadrage.md` attendue |
| Sprint en cours    | Aucun (les sprints démarrent en phase B, étape 12)  |
| Issue en cours     | Aucune                                              |
| Dépôt distant      | 1 commit (SUIVI.md) sur `claude/mentor-fullstack-nodejs-react-s8zaoe`, poussé le 2026-10-01 ; pas encore de `main` |

## 2. Feuille de route (cocher au fur et à mesure)

### Phase A — Conception
- [ ] A.1 Cadrage : problème, personas, proposition de valeur
- [ ] A.2 Recueil des besoins (le mentor joue le client)
- [ ] A.3 Cahier des charges (docs/)
- [ ] A.4 UML : cas d'utilisation, classes, séquences
- [ ] A.5 Base de données : MCD → MLD (3FN) → contraintes/index → rôles PostgreSQL
- [ ] A.6 Architecture
- [ ] A.7 Périmètre MVP 3 jours (MoSCoW)

### Phase B — Organisation agile sur GitHub
- [ ] B.8 Dépôt : SSH, protection de main, labels, milestones, modèles, conventions, .gitignore
- [ ] B.9 GitHub Projects (tableau Scrum)
- [ ] B.10 Backlog : epics → user stories → tâches
- [ ] B.11 CI GitHub Actions (typage, lint, tests, PostgreSQL de test)
- [ ] B.12 Sprints + cérémonies

### Phase C — Développement issue par issue
- (à remplir à partir de B.10)

## 3. Progression par axe

| Axe | Acquis | En cours | À venir |
|-----|--------|----------|---------|
| 1. Conception logicielle | Structure d'un cadrage (problème, alternatives, personas, proposition de valeur, indicateurs, hors-périmètre) | Cohérence entre personas et fonctionnalités ; indicateurs mesurables | Besoins, CDC, UML, archi |
| 2. Bases de données (conception, SQL, admin) | — | — | MCD/MLD, 3FN, rôles |
| 3. Git / GitHub | — | — | SSH, protection, PR, CI |
| 4. Node / Express / TS / React / IA | — | — | — |
| 5. Scrum | — | — | Backlog, sprints |

> Règle : chaque sprint fait avancer les 5 axes. En phase A (hors sprint),
> les axes 3, 4 et 5 progressent surtout par la théorie et les questions
> d'entretien ; le rattrapage pratique se fait en phase B.

## 4. Erreurs récurrentes

- **Réponses incohérentes entre elles** (cadrage) : le persona principal « paie », mais son budget est « à préciser » ; on mesure « l'écart entre le planning prévu et le planning réel », mais le suivi du temps est hors-périmètre ; on vise une « planification d'équipe » pour un freelance qui travaille seul. → Réflexe : relire chaque réponse à la lumière des autres.
- **Réponses non chiffrées** (« ça dépend », « à préciser ») là où un ordre de grandeur suffit. → Réflexe : donner une hypothèse chiffrée et la marquer « à valider ».
- **Périmètre trop large** (4 problèmes, 4 personas, 5 indicateurs, 2 langues). → Réflexe : un seul de chaque pour le MVP, le reste en « plus tard ».
- **Décision sans justification** (« on passe par A » sans le « pourquoi » demandé). → Réflexe : toute décision s'accompagne d'une phrase « parce que… ».
- **Champs copiés-collés d'un persona à l'autre** (vu 2 fois : cadrage v1 et v2). → Réflexe : chaque persona a un objectif et une frustration qui lui sont propres.
- **Rôles mélangés** : l'étudiant « suit plusieurs équipes » (c'est l'encadrant) ; le chef de projet valide le livrable (Q8) alors que c'est l'encadrant (Q5-6).

## 5. Points à réviser

- Différence entre persona principal, persona secondaire et persona hors cible.
- Indicateur principal (« north star ») contre indicateurs secondaires ; indicateur mesurable dès le MVP ou pas.
- Savoir répondre à l'objection « un bon prompt dans ChatGPT suffit ».
- Savoir justifier le choix du projet et le pivot (« pourquoi ce projet ? »).
- Vocabulaire de l'ingénierie des exigences : élicitation, analyse, spécification, validation, gestion des exigences ; exigence fonctionnelle / non fonctionnelle ; exigence vérifiable ; matrice de traçabilité ; norme ISO/IEC/IEEE 29148 (qui a remplacé IEEE 830).

## 6. Décisions prises

| Date | Décision | Pourquoi |
|------|----------|----------|
| 2026-09-30 | Le fichier de suivi vit dans `docs/mentorat/` | Seul dossier où le mentor écrit |
| 2026-10-01 | ~~Pivot A : cible = équipes de projet étudiantes~~ (remplacé le jour même, voir ligne suivante) | — |
| 2026-10-01 | **Identité du produit** : kickoff_dev est un atelier d'ingénierie des besoins et des exigences, et surtout de conception, guidé par l'IA. La cible se définit par le **rôle** (qui fait l'ingénierie des exigences et la conception), pas par le statut ; un projet étudiant n'est qu'un contexte d'usage parmi d'autres | Décision de l'étudiant : le produit ne s'adresse pas aux étudiants, il porte sur l'ingénierie des exigences et la conception |
| 2026-10-01 | Pas d'entretiens de validation (Mom Test) | Décision de l'étudiant : on se concentre sur le projet |
| 2026-10-01 | Langue (proposition du mentor, à confirmer dans le cadrage) : langue des documents générés choisie par projet (FR ou EN) dès le MVP ; interface en français seulement, multilingue prévu pour plus tard | Respecte le besoin « certains documents en anglais » sans doubler le travail sur l'interface |

## 7. Notes techniques / environnement

- Le mentor travaille dans un conteneur cloud (copie du dépôt), pas sur la
  machine de l'étudiant (`~/dev/kickoff_dev`). Il n'a pas `gh` : il lit
  GitHub via l'API (PR, issues, CI). Pour `psql`, il faudra que la base soit
  accessible depuis le conteneur, sinon l'étudiant colle les sorties.
- Le dépôt GitHub était vide : le premier commit (ce fichier) est poussé sur
  la branche `claude/mentor-fullstack-nodejs-react-s8zaoe`. **À l'étape B.8** :
  créer `main` à partir de cette branche (pour garder un historique commun),
  la pousser, la définir comme branche par défaut dans Settings → General,
  puis protéger `main`.

## 8. Journal des sessions

### Session 1 — 2026-09-30
- Création de SUIVI.md.
- Lancement de A.1 : 12 questions de cadrage posées (problème, personas,
  proposition de valeur, contraintes, hors-périmètre).
- Prochaine action de l'étudiant : répondre aux questions de cadrage.

### Session 2 — 2026-10-01
- Commit du suivi poussé sur GitHub (l'accès est rétabli).
- Réponses de cadrage relues en avocat du diable. Points forts : il reconnaît
  honnêtement que le problème est encore une hypothèse ; il a vu le vrai défaut
  de l'IA générique (elle produit sans poser de questions) ; il a suivi le coût
  de l'IA dès le départ.
- À trancher : le problème central, le persona principal (un freelance seul
  n'a pas besoin de planification d'équipe), un résultat clé réaliste
  (« 10 min » pour tout le pack est irréaliste), un seul indicateur principal,
  le budget, une seule langue pour le MVP.
- Modèle de `docs/conception/01-cadrage.md` donné (sections + consignes, pas le contenu).

### Session 2 (suite) — 2026-10-01
- L'étudiant demande s'il existe un projet plus réaliste (vrai problème, vraie
  cible). Le mentor a comparé 3 options et recommande l'option A : kickoff_dev
  recentré sur les équipes de projet étudiantes en informatique à Madagascar et
  leur encadrant. Raisons : cible joignable cette semaine, problème vécu, toutes
  les fonctionnalités servent, IA au centre. L'option B (commande et paiement
  pour restaurants) devient le projet 2.
- En attente : le choix de l'étudiant (A, B ou C) et sa justification.
- Décision : **option A** (2026-10-01), mais sans la justification demandée → à
  écrire dans le cadrage. Questions de cadrage révisées envoyées (Q1, Q3, Q4,
  Q5-6, Q7, Q8, Q9, Q11, Q12, plus deux nouvelles questions : la valeur pour
  l'encadrant et le risque de « triche »). Script d'entretien de validation
  (Mom Test) à préparer pour 3 camarades et 1 encadrant.

### Session 2 (suite 2) — 2026-10-01
- L'étudiant recadre : pas d'entretiens de validation ; le produit n'est pas
  « pour les étudiants », c'est un atelier d'ingénierie des exigences et de
  conception. Le mentor accepte.
- Revue du cadrage v2. Points forts : Q14 (questions avant rédaction, sections
  bloquées tant que leurs questions sont sans réponse, origine IA ou humaine de
  chaque passage, historique de qui a répondu) ; Q9 mesurable grâce aux
  horodatages ; « une séance de 2 h » est réaliste.
- Bloquant : la cible déclarée (« pas pour les étudiants ») contredit le
  persona (« étudiant en M2 »). Le différenciateur doit être la **traçabilité**
  besoin → exigence → UML → user story, et non la répartition des tâches.
- Cadrage validé à condition de corriger 4 points directement dans
  `docs/conception/01-cadrage.md`.
