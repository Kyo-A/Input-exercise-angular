# InputExercise

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.7.

Let's go with @Input
Tu vas créer 2 components avec une hiérarchie parent/enfant. Le component parent (DeveloperComponent) sera chargé d'afficher les informations d'un développeur telles que son nom, son prénom, son âge, sa biographie. Il devra aussi posséder au minimum 2 compétences, et chaque compétence sera affichée dans un autre component (SkillComponent).

Modèle de données de la classe Developer :\ Liste des propriétés :

lastName de type string en visibilité public
firstName de type string en visibilité public
age de type number en visibilité public
sexe de type string en visibilité public
bio de type string en visibilité public
skills est un tableau de type Skill en visibilité public
On doit retrouver toutes les propriétés dans le constructeur de ta classe
Modèle de données de la classe Skill :\ Liste des propriétés :

name de type string en visibilité public
logo de type string en visibilité public
site de type string en visibilité public
On doit retrouver toutes les propriétés dans le constructeur de ta classe
Modèle de données de la classe DeveloperComponent :\ Liste des propriétés :

developer de type Developer en visibilité public
Modèle de données de la classe SkillComponent:\ Liste des propriétés :

skill de type Skill en visibilité public
Structure du répertoire src/app :

app
├── ...
├── common
│   ├── developer.model.ts
│   └── skill.model.ts
├── developer
│   ├── developer.component.css
│   ├── developer.component.html
│   ├── developer.component.spec.ts
│   └── developer.component.ts
└── skill
    ├── skill.component.css
    ├── skill.component.html
    ├── skill.component.spec.ts
    └── skill.component.ts
Les dossier common, developer et skill doivent être au même niveau.\ Certains répertoires (générés automatiquement par ng) ont volontairement été omis. Les fichiers *.spec.ts ne sont pas obligatoires.

Pour réaliser ce challenge, tu devras :

Créer une classe Developer (developer.model.ts) représentant le modèle de données d'un développeur.
Créer une classe Skill (skill.model.ts) représentant le modèle de données d'une compétence.
Générer un composant <app-developer> (DeveloperComponent), qui sera chargé d'afficher les informations globales du développeur (nom, prénoms, âge, sexe, biographie).
A l'initialisation du component <app-developer>, tu devras créer un nouvel objet de type developer.
Générer un composant <app-skill> (SkillComponent), qui sera chargé d'afficher une des compétences du développeur (nom de la technologie, logo et lien vers le site officiel).
Les deux composants <app-developer> et <app-skill> doivent être au même niveau hiérarchique dans le dossier projet (voir structure du projet).
D'un point de vue structure HTML, <app-skill> est un composant enfant de <app-developer>.
Le composant <app-developer> utilisera la directive *ngFor pour afficher autant de composants <app-skill> qu'il y a de compétences pour le développeur. C'est-à-dire qu'il n'y aura qu'un seul composant <app-skill> déclaré dans le HTML du composant <app-developer>.
La compétence qui sera affichée par le composant <app-skill> lui sera transmise via @Input
Critères de validation
La structure du projet est respectée.
Les modèles de données Developer et Skill sont respectés.
Les noms des composants et leurs propriétés sont respectés.
Toutes les variables sont correctement typées.
Les compétences sont transmises de <app-developer> vers <app-skill> en utilisant @Input.
