# Refactoring — EcoTrip Calculator
**Groupe :** [Phong, Arthur C, Valentin]

---

## Principe SOLID appliqué : [nom du principe]

**Problème identifié :**
[Décrivez ce qui était violé dans le code original — localisez avec fichier + ligne]

**Transformation réalisée :**
[Ce que vous avez fait — créé une interface ? extrait une classe ? inversé une dépendance ?]

**Avant :**
```[langage]
// extrait du code original
```

**Après :**
```[langage]
// extrait du code refactoré
```

**Bénéfice concret :**
[Ce que ça change en pratique : "on peut maintenant ajouter un mode de transport sans toucher à..."]

---

## Pattern GOF appliqué : [nom du pattern]

**Problème résolu :**
[Quel problème de conception ce pattern adresse-t-il dans ce contexte ?]

**Structure mise en place :**
[Décrivez les classes/interfaces créées et leur rôle]

**Bénéfice concret :**
[Ce que ça change en pratique]

---

## Object Calisthenics appliquées

### Règle #[6] — [Ne pas abréger]

**Violation originale :** `[calculatorService.ts:2]`
```
calculate(d: any, t: any, ct: any, p: any, c: any): any {
```
Mauvaise nomenclature passée en paramètre de la méthode calculate qui peut amener à des confusions, mauvaises interprétations.

**Transformation :**
```
calculate(distance: any, transport: any, carType: any, passengers: any, country: any)
```
Nous avons renommé toutes les variables 

**Bénéfice :**
Meilleure compréhension des variables

### Règle #[3] — [Encapsuler les primitives]

**Violation originale :** `[calculatorService.ts:2]`
```
calculate(d: any, t: any, ct: any, p: any, c: any): any {
```
On remplace le type any, 

**Transformation :**
```
calculate(distance: any, transport: any, carType: any, passengers: any, country: any)
```
On remplace 'any' par un export de type (transport) où on lui donne/impose les choix possibles pour les transports (exemple : car, train ou bus)

**Bénéfice :**
Meilleure compréhension des variables

---

## Ce qu'on ferait ensuite
[Si vous aviez 15 minutes de plus : quelle serait la prochaine transformation prioritaire et pourquoi ?]