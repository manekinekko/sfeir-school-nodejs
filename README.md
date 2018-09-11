# Sfeir Schools

On va faire un petit projet pour gérer des Sfeir Schools !

On aura besoin de [Node.js 10](https://nodejs.org/en/).

:arrow_forward: `git checkout -f project-01-readme`.

## Step 1

- Installer [Express](http://expressjs.com/).
- Créer une route correspondant [à la méthode `GET`](https://fr.wikipedia.org/wiki/Hypertext_Transfer_Protocol#M%C3%A9thodes) pour répondre "Hello, Sfeir School!".
- Lancer avec `npm start`.
- Tester avec [httpie](https://httpie.org/): `http http://localhost:3000/`.

Ensuite:

- :sos: `git checkout -f project-01-solution`.
- :fast_forward: `git checkout -f project-02-readme`.

## Step 2

Une Sfeir School est un objet, par exemple:

```json
{
  "title": "Sfeir School NodeJS",
  "trainer": "Siegfried Ehret",
  "attendees": 42
}
```

- On va gérer les Sfeir Schools en mémoire avec un tableau.
- Modifier la route `GET` pour renvoyer l'ensemble des Sfeir Schools.
- Créer une route correspondant à la méthode `POST` pour ajouter une Sfeir School (installer le module [body-parser](https://github.com/expressjs/body-parser)).
- Lancer avec `npm start`.
- Tester avec [httpie](https://httpie.org/):
  - Pour récupérer la liste: `http http://localhost:3000/`.
  - Pour ajouter une Sfeir School: `http POST http://localhost:3000/ title="Sfeir School NodeJS" trainer="Siegfried Ehret"`.

Ensuite:

- :sos: `git checkout -f project-02-solution`.
- :fast_forward: `git checkout -f project-03-readme`.

## Step 3

Des tests !

On va utiliser 2 modules qu'on va installer sous les `devDependencies`:

- [jest](https://facebook.github.io/jest/), un framework de tests.
- [supertest](https://github.com/visionmedia/supertest), pour tester simplement des requêtes à une API.

Et un peu de refactoring:

- Faire un module "lib/app.js" avec toute l'application sauf le `app.listen(...)`.
- Faire un "index.js" qui va appeler notre module et faire le `app.listen(...)`.
- Changer les scripts dans le package.json.

Et enfin:

- Créer un test qui va faire un `GET` sur `/` et vérifier que le `statusCode` est `200` et que le `body` est `[]`.
- Modifier le script npm "test" pour lui affecter la commande "jest".
- Lancer les tests avec `npm test`.

Ensuite:

- :sos: `git checkout -f project-03-solution`.
- :fast_forward: `git checkout -f project-04-readme`.
