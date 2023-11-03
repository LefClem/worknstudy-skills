# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple) ✔️
- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) ✔️
- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) ✔️
- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ✔️ 

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
// Function that allows a user to create a new Post in a social network application
// and insert a local file in your post
exports.createPost = async (req, res) => {

    try {
        let post = req.file ?
            {
                ...req.body,
                user_id: req.auth.id,
                image_url: `${req.protocol}://${req.get('host')}/images/post/${req.file.filename}`
            } : {
                ...req.body,
                user_id: req.auth.id,
                image_url: ""
            };

        let results = await postsModels.createPost(post);
        res.status(201).json({ results });
    } catch (error) {
        res.status(400).json({ error });
    }

}
```

### Utilisation dans un projet ✔️

https://github.com/LefClem/Groupomania

Description : Petit réseau social d'entreprise pour une dizaine de personnes avec un back coder en NodeJS avec Express et une BDD MySql 

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- https://grafikart.fr/tutoriels/nodejs
- Série de vidéo qui permet de comprendre le fonctionnement de NodeJs

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
