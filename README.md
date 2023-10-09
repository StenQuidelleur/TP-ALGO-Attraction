# TP-ALGO-Attraction

---

### **Travaux pratiques : Optimisation d'un parc d'attractions**

#### **Contexte** :
Vous êtes engagé en tant qu'ingénieur informaticien pour améliorer l'expérience des visiteurs d'un parc d'attractions. Votre mission est d'utiliser des structures de données et des algorithmes pour aider les visiteurs à naviguer dans le parc, choisir des attractions et planifier leur journée.

---

### **1. Structures de données pour le stockage** :

**Attraction** : Chaque attraction a un nom, un niveau de thrills (sensations fortes mesuré de 1 à 10), une durée (en minutes) et une zone du parc (ex: "Zone A").

-> Définir une classe **Attraction** avec Vars (nom, niveauThrills, durée, zone) / fonction init -> Initialisation de l'objet Attraction.

**Arbre de décisions** : Afin de guider les visiteurs dans le choix de leur prochaine attraction, mettez en place un arbre de décisions basé sur le niveau de thrills. Les attractions ayant un niveau de thrill inférieur iront à gauche et celles ayant un niveau supérieur iront à droite.

-> Définir une classe **Level** avec Vars (niveau, attractions, gauche, droite) / fonction init -> Initialisation du noeud avec un niveau de thrills.   
-> Définir une **fonction ajouterAttraction**(attraction) qui ajoute une attraction au noeud actuel ou à un de ses enfants.   
* Le noeud à gauche contient des attractions ayant un niveau de sensations fortes inférieur.   
* Le noeud à droite contient des attractions ayant un niveau de sensations fortes supérieur.   

**Graphe des zones** : Représente les différentes zones du parc et les chemins pour s'y rendre. Chaque zone est connectée à d'autres zones par des chemins, avec une certaine distance.

-> Définir une classe **Plan** avec Vars (zones, liens) / fonction init -> Initialisation du graphe **Plan**.   
-> Définir une **fonction ajouterZone**(zone, attractions) qui ajoute une zone et ses attractions au graphe.   
-> Définir une **fonction ajouterLien**(zoneA, zoneB, distance) qui ajoute un lien entre deux zones.   

**Hachage des zones** : Fournir un moyen rapide d'accéder à la distance entre deux zones spécifiques ainsi qu'aux attractions disponibles dans ces zones.   
Utilisez un système de hachage pour retrouver rapidement les informations sur une zone en fonction de son nom. Chaque entrée de la table de hachage devrait permettre d'obtenir la liste des attractions de cette zone ainsi que les distances vers les autres zones.   

-> Définir une classe **TableHachageZones** avec Vars (table) / fonction init -> Initialisation de la table de hachage.   
-> Définir une **fonction ajouter**(zone, attractions, distances) qui ajoute une zone, ses attractions et ses distances par rapport aux autres zones.   
-> Définir une **fonction rechercher**(zone): Retourne les attractions de la zone et les distances par rapport aux autres zones.  

---

### **2. Triage des attractions par durée** :

Mettez en œuvre différents algorithmes de tri pour classer les attractions selon leur durée.
- **fonction triParSelection**(listeAttractions) -> du moins long au plus long
- **fonction triParInsertion**(listeAttractions) -> du plus long au moins long
- **fonction triABulles**(listeAttractions) -> du moins long au plus long

---

### **3. Recherche d'attractions** :

Afin de permettre aux visiteurs de trouver rapidement une attraction, implémentez :
- **fonction rechercheLinéaire**(listeAttractions, nomAttraction)

Pour améliorer la recherche :
- **fonction rechercheDichotomique**(listeAttractionsTriées, nomAttraction)

---

### **4. Planification d'une journée** :

Créez une fonction qui permet aux visiteurs de planifier leur journée en fonction de leurs préférences en termes de thrills. Cette fonction prendra en compte la durée de chaque attraction et les déplacements entre les zones.
- **fonction planifierJournée**(listeAttractions, tempsDisponible, niveauThrillsSouhaité)

---

### **5. Parcours d'attractions par niveau de Thrills** :

Chaque attraction du parc est notée sur une échelle de 1 à 10, 1 étant le moins thrilling et 10 étant le plus thrilling. Écrivez une fonction récursive qui, étant donné une zone de départ, retourne une liste d'attractions à visiter dans l'ordre croissant de thrills.
- **fonction trouverParcours**(zoneDépart)

---

### **5. Reflexions supplémentaires** :

Comment ces structures et algorithmes interagissent avec le matériel informatique ?

Quels sont les défis à relever lors de la mise en œuvre dans un vrai parc ?

Comment ces algorithmes et structures peuvent-ils améliorer l'expérience globale des visiteurs du parc d'attractions ?

---
