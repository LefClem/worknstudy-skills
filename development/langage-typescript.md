# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
- les types de bases ✔️
- comment et pourquoi étendre une interface ❌ 
- les classes et les decorators ❌ 

## 💻 J'utilise

### Un exemple personnel commenté ✔️

/**
 * In this challenge, you have to add a list of skills to each group (based on 
 * students skills in the group). Duplicates skills for one group is not permitted. Skills must be
 * sorted alphabatically. Groups order, students order and students skills order must remain
 * untouched.
 * 
 * @param groups List of groups without skills, but with students
 * @returns List of groups with a new prop skills
 */

// ↓ uncomment bellow lines and add your response!
export default function ({ groups }: { groups: Group[] }): GroupWithSills[] {
    const newGroups = groups.map((group) => {
        let skills: string[] = [];
        group.students.forEach((student) => {
            student.skills.forEach((skill) => {
                skills.push(skill);
            })
        })
        let newArrSkills = [...new Set(skills)].sort();
        skills = newArrSkills;
        Object.assign(group, { skills: newArrSkills });
        return {...group, skills: skills}        
    })

    return newGroups;
}

// used interfaces, do not touch
interface Student {
    name: string;
    age: number;
    skills: string[];
}

export interface Group {
    students: Student[];
    name: string;
}

export interface GroupWithSills extends Group {
    skills: string[];
}

### Utilisation dans un projet ✔️

https://github.com/LefClem/the-good-corner

Description : Clone du site Le Bon Coin avec une API GraphQL 

### Utilisation en production si applicable ❌ 

[lien du projet](...)

Description :

### Utilisation en environement professionnel ✔️

Description : J'utilise Typescript au quotidien dans mon travail en modifiant les interface pour appeler de nouvelles données dans les composants, pour typer les données renvoyer et les nouvelles variables crées

## 🌐 J'utilise des ressources

### Titre

- https://www.codecademy.com/learn/learn-typescript
- Site anglophone permettant d'apprendre Typescript par la pratique

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
