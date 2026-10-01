# Suivi du mentorat — kickoff_dev

> Fichier tenu à jour par le mentor. Lu au début de chaque session.
> Dernière mise à jour : 2026-10-01 (session 2)

## 1. État actuel

| Élément            | Valeur                                              |
|--------------------|-----------------------------------------------------|
| Phase              | A — Conception                                      |
| Étape              | A.1 — Cadrage v2 (nouvelle cible : équipes de projet étudiantes + encadrant) : réponses aux questions révisées attendues |
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

## 5. Points à réviser

- Différence entre persona principal, persona secondaire et persona hors cible.
- Indicateur principal (« north star ») contre indicateurs secondaires ; indicateur mesurable dès le MVP ou pas.
- Savoir répondre à l'objection « un bon prompt dans ChatGPT suffit ».
- Savoir justifier le choix du projet et le pivot (« pourquoi ce projet ? »).
- Entretien de validation façon « Mom Test » : questions sur des faits passés, pas d'avis sur l'idée.

## 6. Décisions prises

| Date | Décision | Pourquoi |
|------|----------|----------|
| 2026-09-30 | Le fichier de suivi vit dans `docs/mentorat/` | Seul dossier où le mentor écrit |
| 2026-10-01 | **Pivot A** : kickoff_dev cible les équipes de projet étudiantes en informatique (Madagascar) et leur encadrant, au lieu du freelance seul | Cible joignable pour valider, toutes les fonctionnalités servent (équipe, disponibilités, validation humaine par l'encadrant), pas de paiement dans le MVP. Commande et paiement pour restaurants = projet 2 |

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
