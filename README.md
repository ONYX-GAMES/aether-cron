# aether-cron

Planificateur des tâches périodiques de l'API AETHER, hébergée sur Vercel (serverless, sans boucle de fond).

Un seul workflow, [`launch-cron.yml`](.github/workflows/launch-cron.yml), toutes les 5 minutes :
- `GET /cron/minute` : rappels de lancement et récaps Nemoria ;
- `GET /cron/imminent` : lancements des prochaines 48 h, un passage sur trois (~15 min).

Le repo est public pour bénéficier des minutes GitHub Actions illimitées. Il ne contient aucun secret :
`CRON_SECRET` est un secret du repo, à garder identique à la variable `CRON_SECRET` du projet Vercel `aether-api`.

GitHub désactive les workflows planifiés après 60 jours sans activité sur un repo public :
le réactiver depuis l'onglet Actions si besoin.
