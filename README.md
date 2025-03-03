# mongodb
SGBD = Système de Gestion de Base de Données

# Cours
![alt text](cours/image.png)
notion d'Index = permet de créer une table intermédiaire, exemple si données beaucoup sollicité on peut faire un Index afin d'accélérer la recherche de données mais en contrepartie ralenti l'écriture de données 

![alt text](cours/image-1.png)

![alt text](cours/image-2.png)

![alt text](cours/image-3.png)

![alt text](cours/image-4.png)

Ici l'ajout d'une collection 'ecommerce_produits' et l'ajout d'un produit crayon 


Voilà le code pour TP2 Exo1
```js
db.ecommerce_produits.insertMany([
  {
    nom: "Ordinateur Portable Asus",
    description: "Un ordinateur portable puissant pour le travail et les jeux.",
    prix: 1200,
    stock: 50,
    categorie: "Informatique",
    sous_categorie: "Ordinateurs Portable",
    caracteristiques_techniques: {
      processeur: "Intel Core i7",
      memoire: "16GB RAM",
      stockage: "512GB SSD",
      ecran: "15 pouces"
    },
    commentaires: [
      { auteur: "Jean.D", note: 5, commentaire: "Excellent produit !" },
      { auteur: "Marie.C", note: 4, commentaire: "Tres bon rapport qualite/prix" }
    ],
    tags: ["portable", "informatique", "performant"]
  },
  {
    nom: "Smartphone Huawei",
    description: "Un smartphone avec un appareil photo de haute qualite",
    prix: 800,
    stock: 100,
    categorie: "Telephonie",
    sous_categorie: "Smartphones",
    caracteristiques_techniques: {
      processeur: "Snapdragon 888",
      memoire: "8GB RAM",
      stockage: "128GB",
      appareil_photo: "108MP"
    },
    commentaires: [
      { auteur: "Pierre.M", note: 4, commentaire: "Tres satisfait de mon achat" },
      { auteur: "Sophie.D", note: 5, commentaire: "Le meilleur smartphone que j'ai eu" }
    ],
    tags: ["smartphone", "telephonie", "photo"]
  },
  {
    nom: "Tablette DEF",
    description: "Une tablette ideale pour le divertissement et la productivite",
    prix: 500,
    stock: 75,
    categorie: "Informatique",
    sous_categorie: "Tablettes",
    caracteristiques_techniques: {
      processeur: "Apple A14",
      memoire: "4GB RAM",
      stockage: "64GB",
      ecran: "10 pouces"
    },
    commentaires: [
      { auteur: "Lucie.G", note: 5, commentaire: "Parfaite pour regarder des films et series" },
      { auteur: "Thomas.D", note: 4, commentaire: "Bonne autonomie" }
      { auteur: "Romain.S", note: 4, commentaire: "Tres bon rapport qualite/prix" }
    ],
    tags: ["tablette", "informatique", "multimedia"]
  },
    {
    nom: "Casque Audio Bluetooth GHI",
    description: "Un casque sans fil avec une excellente qualite sonore",
    prix: 150,
    stock: 200,
    categorie: "Audio",
    sous_categorie: "Casques",
    caracteristiques_techniques: {
      autonomie: "30 heures",
      annulation_bruit: true,
      micro: true
    },
    commentaires: [
      { auteur: "Isabelle.L", note: 5, commentaire: "Son incroyable et tres confortable" },
      { auteur: "David.M", note: 4, commentaire: "Bon rapport qualite/prix" }
    ],
    tags: ["casque", "audio", "bluetooth"]
  },
  {
    nom: "Enceinte Connectee JBL",
    description: "Une enceinte intelligente pour la maison.",
    prix: 100,
    stock: 150,
    categorie: "Audio",
    sous_categorie: "Enceintes Connectees",
    caracteristiques_techniques: {
      assistant_vocal: "Alexa",
      wifi: true,
      bluetooth: true
    },
    commentaires: [
      { auteur: "Nathalie.R", note: 4, commentaire: "Tres pratique pour contrôler la maison" },
      { auteur: "Philippe.L", note: 3, commentaire: "Le son pourrait être meilleur" }
    ],
    tags: ["enceinte", "audio", "connectee"]
  },
  {
    nom: "Montre Connectée Apple",
    description: "Une montre intelligente pour suivre votre activite physique",
    prix: 250,
    stock: 125,
    categorie: "Objets Connectes",
    sous_categorie: "Montres Connectees",
    caracteristiques_techniques: {
      gps: true,
      cardiofrequencemetre: true,
      etanche: true
    },
    commentaires: [
      { auteur: "Sandrine.F", note: 5, commentaire: "Ideale pour le sport" },
      { auteur: "Laurent.C", note: 4, commentaire: "Bon suivi de l'activite" }
    ],
    tags: ["montre", "objets connectes", "sport"]
  },
  {
    nom: "Televiseur Samsung",
    description: "Un televiseur 4K pour une expérience immersive",
    prix: 900,
    stock: 80,
    categorie: "Television",
    sous_categorie: "Televiseurs 4K",
    caracteristiques_techniques: {
      taille_ecran: "55 pouces",
      hdr: true,
      smart_tv: true
    },
    commentaires: [
      { auteur: "Martine.C", note: 5, commentaire: "Image magnifique !" },
      { auteur: "Antoine.L", note: 4, commentaire: "Tres bon rapport qualite/prix" }
    ],
    tags: ["téléviseur", "télévision", "4k"]
  },
  {
    nom: "Console XBOX",
    description: "Une console de jeux pour les passionnes",
    prix: 400,
    stock: 60,
    categorie: "Jeux Video",
    sous_categorie: "Consoles",
    caracteristiques_techniques: {
      marque: "Microsoft",
      processeur: "AMD Ryzen",
      stockage: "1TB SSD"
    },
    commentaires: [
      { auteur: "Claire.B", note: 5, commentaire: "Graphismes incroyables !" },
      { auteur: "Sebastien.V", note: 4, commentaire: "Tres performante" }
    ],
    tags: ["console", "jeux vidéo", "gaming"]
  },
  {
    nom: "Appareil Photo Sony",
    description: "Un appareil photo pour les photographes professionnels",
    prix: 1500,
    stock: 30,
    categorie: "Photo",
    sous_categorie: "Appareils Photo Reflex",
    caracteristiques_techniques: {
      marque: "Sony",
      capteur: "24MP",
      video_4k: true,
      wifi: true
    },
    commentaires: [
      { auteur: "Helene.R", note: 5, commentaire: "Qualite d'image exceptionnelle" },
      { auteur: "Julien.P", note: 4, commentaire: "Tres polyvalent" }
    ],
    tags: ["appareil photo", "photo", "reflex"]
  },
  {
    nom: "Objectif Sony",
    description: "Un objectif pour appareil photo reflex.",
    prix: 300,
    stock: 90,
    categorie: "Photo",
    sous_categorie: "Objectifs",
    caracteristiques_techniques: {
      marque: "Sony",
      objectif: "50mm",
      stabilisation: false
    },
    commentaires: [
      { auteur: "Amelie.N", note: 5, commentaire: "Parfait pour les portraits" },
      { auteur: "Romain.S", note: 4, commentaire: "Tres bon rapport qualite/prix" }
    ],
    tags: ["objectif", "photo", "portrait"]
  }
]);

```

Voilà le code qui m'a permis de créer la collection 'ecommerce_produits' avec les conditions demandés
# Exercice 2

Maintenant on va récupérer les produit d'une seule categorie :

```
db.ecommerce_produits.find({ categorie: "Informatique" })
```
![alt text](cours/image-5.png)
![alt text](cours/image-6.png)
![alt text](cours/image-7.png)

Pour rechercher chaque produit entre 50€ et 200€

```
db.ecommerce_produits.find({ prix: { $gte: 50, $lte: 200 } })
```

![alt text](cours/image-8.png)
![alt text](cours/image-9.png)
![alt text](cours/image-10.png)

Pour afficher les produit avec un stock disponible 

```
db.ecommerce_produits.find({ stock: { $gte : 0 } })
```

![alt text](cours/image-11.png)
![alt text](cours/image-12.png)
![alt text](cours/image-13.png)
![alt text](cours/image-14.png)
![alt text](cours/image-15.png)
![alt text](cours/image-16.png)
![alt text](cours/image-17.png)
![alt text](cours/image-18.png)
![alt text](cours/image-19.png)
![alt text](cours/image-20.png)
![alt text](cours/image-21.png)
![alt text](cours/image-22.png)

Pour trouver un produit avec au moins 3 avis :

```
db.ecommerce_produits.find({
  commentaires :{
    $size : 3
  }
  })
``` 

Ce qui donne :

![alt text](cours/image-23.png)
![alt text](cours/image-24.png)

# Exercice 3
```
db.ecommerce_produits.updateMany({},
{ $mul : { prix : 1.05 } })
``` 
Ensuite un code qui me confirme que le changement a été appliqué à 10 documents : 

```
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 10,
  modifiedCount: 10,
  upsertedCount: 0
}
``` 

Ce code m'a permis d'ajouter 5% à tous les produits de ma collection

Résultat :
``` 
{
  _id: ObjectId('67c5b3b1099008c648bf642d'),
  nom: 'Ordinateur Portable Asus',
  description: 'Un ordinateur portable puissant pour le travail et les jeux.',
  prix: 1260,
  stock: 50,
  categorie: 'Informatique',
  sous_categorie: 'Ordinateurs Portable',
  caracteristiques_techniques: {
    processeur: 'Intel Core i7',
    memoire: '16GB RAM',
    stockage: '512GB SSD',
    ecran: '15 pouces'
  },
  commentaires: [
    {
      auteur: 'Jean.D',
      note: 5,
      commentaire: 'Excellent produit !'
    },
    {
      auteur: 'Marie.C',
      note: 4,
      commentaire: 'Tres bon rapport qualite/prix'
    }
  ],
  tags: [
    'portable',
    'informatique',
    'performant'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf642e'),
  nom: 'Smartphone Huawei',
  description: 'Un smartphone avec un appareil photo de haute qualite',
  prix: 840,
  stock: 100,
  categorie: 'Telephonie',
  sous_categorie: 'Smartphones',
  caracteristiques_techniques: {
    processeur: 'Snapdragon 888',
    memoire: '8GB RAM',
    stockage: '128GB',
    appareil_photo: '108MP'
  },
  commentaires: [
    {
      auteur: 'Pierre.M',
      note: 4,
      commentaire: 'Tres satisfait de mon achat'
    },
    {
      auteur: 'Sophie.D',
      note: 5,
      commentaire: "Le meilleur smartphone que j'ai eu"
    }
  ],
  tags: [
    'smartphone',
    'telephonie',
    'photo'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf642f'),
  nom: 'Tablette DEF',
  description: 'Une tablette ideale pour le divertissement et la productivite',
  prix: 525,
  stock: 75,
  categorie: 'Informatique',
  sous_categorie: 'Tablettes',
  caracteristiques_techniques: {
    processeur: 'Apple A14',
    memoire: '4GB RAM',
    stockage: '64GB',
    ecran: '10 pouces'
  },
  commentaires: [
    {
      auteur: 'Lucie.G',
      note: 5,
      commentaire: 'Parfaite pour regarder des films et series'
    },
    {
      auteur: 'Thomas.D',
      note: 4,
      commentaire: 'Bonne autonomie'
    },
    {
      auteur: 'Romain.S',
      note: 4,
      commentaire: 'Tres bon rapport qualite/prix'
    }
  ],
  tags: [
    'tablette',
    'informatique',
    'multimedia'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6430'),
  nom: 'Casque Audio Bluetooth GHI',
  description: 'Un casque sans fil avec une excellente qualite sonore',
  prix: 157.5,
  stock: 200,
  categorie: 'Audio',
  sous_categorie: 'Casques',
  caracteristiques_techniques: {
    autonomie: '30 heures',
    annulation_bruit: true,
    micro: true
  },
  commentaires: [
    {
      auteur: 'Isabelle.L',
      note: 5,
      commentaire: 'Son incroyable et tres confortable'
    },
    {
      auteur: 'David.M',
      note: 4,
      commentaire: 'Bon rapport qualite/prix'
    }
  ],
  tags: [
    'casque',
    'audio',
    'bluetooth'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6431'),
  nom: 'Enceinte Connectee JBL',
  description: 'Une enceinte intelligente pour la maison.',
  prix: 105,
  stock: 150,
  categorie: 'Audio',
  sous_categorie: 'Enceintes Connectees',
  caracteristiques_techniques: {
    assistant_vocal: 'Alexa',
    wifi: true,
    bluetooth: true
  },
  commentaires: [
    {
      auteur: 'Nathalie.R',
      note: 4,
      commentaire: 'Tres pratique pour contrôler la maison'
    },
    {
      auteur: 'Philippe.L',
      note: 3,
      commentaire: 'Le son pourrait être meilleur'
    }
  ],
  tags: [
    'enceinte',
    'audio',
    'connectee'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6432'),
  nom: 'Montre Connectée Apple',
  description: 'Une montre intelligente pour suivre votre activite physique',
  prix: 262.5,
  stock: 125,
  categorie: 'Objets Connectes',
  sous_categorie: 'Montres Connectees',
  caracteristiques_techniques: {
    gps: true,
    cardiofrequencemetre: true,
    etanche: true
  },
  commentaires: [
    {
      auteur: 'Sandrine.F',
      note: 5,
      commentaire: 'Ideale pour le sport'
    },
    {
      auteur: 'Laurent.C',
      note: 4,
      commentaire: "Bon suivi de l'activite"
    }
  ],
  tags: [
    'montre',
    'objets connectes',
    'sport'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6433'),
  nom: 'Televiseur Samsung',
  description: 'Un televiseur 4K pour une expérience immersive',
  prix: 945,
  stock: 80,
  categorie: 'Television',
  sous_categorie: 'Televiseurs 4K',
  caracteristiques_techniques: {
    taille_ecran: '55 pouces',
    hdr: true,
    smart_tv: true
  },
  commentaires: [
    {
      auteur: 'Martine.C',
      note: 5,
      commentaire: 'Image magnifique !'
    },
    {
      auteur: 'Antoine.L',
      note: 4,
      commentaire: 'Tres bon rapport qualite/prix'
    }
  ],
  tags: [
    'téléviseur',
    'télévision',
    '4k'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6434'),
  nom: 'Console XBOX',
  description: 'Une console de jeux pour les passionnes',
  prix: 420,
  stock: 60,
  categorie: 'Jeux Video',
  sous_categorie: 'Consoles',
  caracteristiques_techniques: {
    marque: 'Microsoft',
    processeur: 'AMD Ryzen',
    stockage: '1TB SSD'
  },
  commentaires: [
    {
      auteur: 'Claire.B',
      note: 5,
      commentaire: 'Graphismes incroyables !'
    },
    {
      auteur: 'Sebastien.V',
      note: 4,
      commentaire: 'Tres performante'
    }
  ],
  tags: [
    'console',
    'jeux vidéo',
    'gaming'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6435'),
  nom: 'Appareil Photo Sony',
  description: 'Un appareil photo pour les photographes professionnels',
  prix: 1575,
  stock: 30,
  categorie: 'Photo',
  sous_categorie: 'Appareils Photo Reflex',
  caracteristiques_techniques: {
    marque: 'Sony',
    capteur: '24MP',
    video_4k: true,
    wifi: true
  },
  commentaires: [
    {
      auteur: 'Helene.R',
      note: 5,
      commentaire: "Qualite d'image exceptionnelle"
    },
    {
      auteur: 'Julien.P',
      note: 4,
      commentaire: 'Tres polyvalent'
    }
  ],
  tags: [
    'appareil photo',
    'photo',
    'reflex'
  ]
}
{
  _id: ObjectId('67c5b3b1099008c648bf6436'),
  nom: 'Objectif Sony',
  description: 'Un objectif pour appareil photo reflex.',
  prix: 315,
  stock: 90,
  categorie: 'Photo',
  sous_categorie: 'Objectifs',
  caracteristiques_techniques: {
    marque: 'Sony',
    objectif: '50mm',
    stabilisation: false
  },
  commentaires: [
    {
      auteur: 'Amelie.N',
      note: 5,
      commentaire: 'Parfait pour les portraits'
    },
    {
      auteur: 'Romain.S',
      note: 4,
      commentaire: 'Tres bon rapport qualite/prix'
    }
  ],
  tags: [
    'objectif',
    'photo',
    'portrait'
  ]
}
``` 

Par la suite on va ajouter un champ promotion (ci-dessous je vais lister uniquement les produit de la catégorie informatique): 

``` 
{
  _id: ObjectId('67c5b3b1099008c648bf642d'),
  nom: 'Ordinateur Portable Asus',
  description: 'Un ordinateur portable puissant pour le travail et les jeux.',
  prix: 1260,
  stock: 50,
  categorie: 'Informatique',
  sous_categorie: 'Ordinateurs Portable',
  caracteristiques_techniques: {
    processeur: 'Intel Core i7',
    memoire: '16GB RAM',
    stockage: '512GB SSD',
    ecran: '15 pouces'
  },
  commentaires: [
    {
      auteur: 'Jean.D',
      note: 5,
      commentaire: 'Excellent produit !'
    },
    {
      auteur: 'Marie.C',
      note: 4,
      commentaire: 'Tres bon rapport qualite/prix'
    }
  ],
  tags: [
    'portable',
    'informatique',
    'performant'
  ],
  promotion: true
}

{
  _id: ObjectId('67c5b3b1099008c648bf642f'),
  nom: 'Tablette DEF',
  description: 'Une tablette ideale pour le divertissement et la productivite',
  prix: 525,
  stock: 75,
  categorie: 'Informatique',
  sous_categorie: 'Tablettes',
  caracteristiques_techniques: {
    processeur: 'Apple A14',
    memoire: '4GB RAM',
    stockage: '64GB',
    ecran: '10 pouces'
  },
  commentaires: [
    {
      auteur: 'Lucie.G',
      note: 5,
      commentaire: 'Parfaite pour regarder des films et series'
    },
    {
      auteur: 'Thomas.D',
      note: 4,
      commentaire: 'Bonne autonomie'
    },
    {
      auteur: 'Romain.S',
      note: 4,
      commentaire: 'Tres bon rapport qualite/prix'
    }
  ],
  tags: [
    'tablette',
    'informatique',
    'multimedia'
  ],
  promotion: true
}
``` 