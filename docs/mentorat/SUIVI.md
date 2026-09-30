# Suivi du mentorat — kickoff_dev

> Fichier tenu à jour par le mentor. Lu au début de chaque session.
> Dernière mise à jour : 2026-09-30 (session 1)

## 1. État actuel

| Élément            | Valeur                                              |
|--------------------|-----------------------------------------------------|
| Phase              | A — Conception                                      |
| Étape              | A.1 — Cadrage (questions posées, réponses attendues) |
| Sprint en cours    | Aucun (les sprints démarrent en phase B, étape 12)  |
| Issue en cours     | Aucune                                              |
| Dépôt distant      | Vide au 2026-09-30 (aucun commit sur GitHub)        |

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
| 1. Conception logicielle | — | Cadrage | Besoins, CDC, UML, archi |
| 2. Bases de données (conception, SQL, admin) | — | — | MCD/MLD, 3FN, rôles |
| 3. Git / GitHub | — | — | SSH, protection, PR, CI |
| 4. Node / Express / TS / React / IA | — | — | — |
| 5. Scrum | — | — | Backlog, sprints |

> Règle : chaque sprint fait avancer les 5 axes. En phase A (hors sprint),
> les axes 3, 4 et 5 progressent surtout par la théorie et les questions
> d'entretien ; le rattrapage pratique se fait en phase B.

## 4. Erreurs récurrentes

- (aucune observée pour l'instant)

## 5. Points à réviser

- (vide)

## 6. Décisions prises

| Date | Décision | Pourquoi |
|------|----------|----------|
| 2026-09-30 | Le fichier de suivi vit dans `docs/mentorat/` | Seul dossier où le mentor écrit |

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
