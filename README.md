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

Pour l'énoncé 3 (Ajouter un tag à une certaine catégorie) j'ai rencontré un problème le code d'erreur est le suivant 

``` 
MongoServerError: Cannot apply $addToSet to non-array field. Field named 'tags' has non-array type string
``` 

j'ai du alors convertir tags

```
db.ecommerce_produits.updateMany(
  { tags: { $type: "string" } }, 
  [
    {
      $set: {
        tags: {
          $cond: {
            if: { $eq: [{ $type: "$tags" },   "string"] },
            then: [ "$tags" ], 
            else: "$tags" 
          }
        }
      }
    }
  ]
)
``` 

On a modifié le stock suite à une vente avec :

``` 
db.ecommerce_produits.updateOne(
  {_id: ObjectId('67c5b3b1099008c648bf642f')},
 {$inc : {stock: -1 }})
``` 

ici on a retiré 1 au stock de la tablette DEF que l'on a identifié à l'aide de ObjectId 

On vérifie que le stock ait bien été modifié :

```
{
  _id: ObjectId('67c5b3b1099008c648bf642f'),
  nom: 'Tablette DEF',
  description: 'Une tablette ideale pour le divertissement et la productivite',
  prix: 525,
  stock: 74,
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
    'Promo'
  ],
  promotion: true
}
```

Donc on est bien passé de 75 à 74 

![alt text](cours/image-25.png)

![alt text](cours/image-26.png)

Je vais chercher les produits qui ont en tags : 'portrait', 'photo'

```
db.ecommerce_produits.find({
  tags: { $all: ["portrait", "photo"] } 
})
```

```
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

Pour lister les produit avec un stock faible :

```
db.ecommerce_produits.find({
stock :{$lt :60 }
})
```

Et le résultat est :

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
    'Promo'
  ],
  promotion: true
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
```

Pour mettre seulement les produit ayant reçu la note de 5 : db.ecommerce_produits.find({categorie:"electronique"}).sort({prix:-1}).limit(5)

# TP FINAL JOUR 1

![alt text](cours/image-27.png)

Ici la BDD "bibliothèque_amazon" et 2 collections livre et utilisateurs

J'ai créé mes propre livres :

```
db.livre.insertOne({
  titre: "Les Misérables",
  auteur: "Victor Hugo",
  annee_publication: 1862,
  editeur: "Hetzel",
  genre: ["Roman historique", "Drame"],
  nombre_pages: 1900,
  langue: "Français",
  disponible: true,
  stock: 2,
  note_moyenne: 4.7,
  description: "L'histoire de Jean Valjean, un ancien forçat, et de sa lutte pour la rédemption dans la France du XIXe siècle.",
  prix: 12.00,
  isbn: "9782253005886",
  date_ajout: new Date("2023-02-01")
})
{
  acknowledged: true,
  insertedId: ObjectId('67c6c19d2981e6f6104d0062')
}
db.livre.insertOne({
  titre: "Orgueil et Préjugés",
  auteur: "Jane Austen",
  annee_publication: 1813,
  editeur: "T. Egerton",
  genre: ["Roman d'amour", "Satire sociale"],
  nombre_pages: 432,
  langue: "Anglais",
  disponible: true,
  stock: 5,
  note_moyenne: 4.6,
  description: "L'histoire d'Elizabeth Bennet et de Mr. Darcy, et de leurs préjugés respectifs.",
  prix: 9.50,
  isbn: "9782070409853",
  date_ajout: new Date("2023-02-10")
})
{
  acknowledged: true,
  insertedId: ObjectId('67c6c1cd2981e6f6104d0063')
}
db.livre.insertOne({
  titre: "1984",
  auteur: "George Orwell",
  annee_publication: 1949,
  editeur: "Secker & Warburg",
  genre: ["Science-fiction", "Dystopie"],
  nombre_pages: 328,
  langue: "Anglais",
  disponible: true,
  stock: 1,
  note_moyenne: 4.9,
  description: "Un roman dystopique qui décrit une société totalitaire et oppressive.",
  prix: 8.00,
  isbn: "9782070403219",
  date_ajout: new Date("2023-02-15")
})
{
  acknowledged: true,
  insertedId: ObjectId('67c6c1de2981e6f6104d0064')
}
db.livre.insertOne({
  titre: "Le Seigneur des Anneaux",
  auteur: "J.R.R. Tolkien",
  annee_publication: 1954,
  editeur: "Allen & Unwin",
  genre: ["Fantasy", "Aventure"],
  nombre_pages: 1200,
  langue: "Anglais",
  disponible: true,
  stock: 4,
  note_moyenne: 4.8,
  description: "L'histoire de Frodon Sacquet et de sa quête pour détruire l'Anneau Unique.",
  prix: 15.00,
  isbn: "9782266115984",
  date_ajout: new Date("2023-02-20")
})
{
  acknowledged: true,
  insertedId: ObjectId('67c6c1f42981e6f6104d0065')
}
db.livre.insertOne({
  titre: "Crime et Châtiment",
  auteur: "Fiodor Dostoïevski",
  annee_publication: 1866,
  editeur: "Le Messager russe",
  genre: ["Roman psychologique", "Drame"],
  nombre_pages: 672,
  langue: "Russe",
  disponible: true,
  stock: 3,
  note_moyenne: 4.7,
  description: "L'histoire de Rodion Raskolnikov, un étudiant pauvre qui commet un meurtre et doit faire face aux conséquences de son acte.",
  prix: 11.00,
  isbn: "9782253005848",
  date_ajout: new Date("2023-02-25")
})
{
  acknowledged: true,
  insertedId: ObjectId('67c6c2032981e6f6104d0066')
}
``` 

Et j'ai ajouté les utiliateurs donné en exemple dans le TP

Pour afficher afficher tous les livres dont la disponibilité est true :
![alt text](cours/image-28.png)

Pour afficher tous les livres publié après 2000 :

![alt text](cours/image-29.png)

 /!\ Pour le coup tous mes livres ici ont été publiés avant 2000

Pour afficher tous les livres publié par un auteur : 

![alt text](cours/image-30.png)

Pour afficher les livres dont les notes sont supérieures à 4:

![alt text](cours/image-31.png)

Pour lister les utilisateurs habitant à lyon : 

![alt text](cours/image-32.png)

Pour lister les livres à l'aide du genre "drame" :

![alt text](cours/image-33.png)

Pour afficher les prix dont le prix est inférieur à 15€ et une note supérieur à 4 : 

![alt text](cours/image-34.png)

Pour trouver quel livre a été empreinté j'ai dû faire un update: 

![alt text](cours/image-35.png)

Et ensuite recherché l'utilisateur qui a emprunté le livre par son titre :

![alt text](cours/image-36.png)

# Partie 3 UPDATE 

La commande pour mettre à jour le titre d'un livre spécifique : 
![alt text](cours/image-37.png)

Commande pour ajouter un champ stock à tous les livres : 

![alt text](cours/image-38.png)

Pour passer un livre indisponible : 
![alt text](cours/image-39.png)

Update pour changer un livre emprunté : 

![alt text](cours/image-40.png)

Changer l'adresse d'un utilisateur : 

![alt text](cours/image-41.png)

Ajouter un tag à un utilisateur : 

![alt text](cours/image-42.png)

Changer la note moyenne d'un livre : 

![alt text](cours/image-43.png)

Supprimer un livre par son titre : 

![alt text](cours/image-44.png)

Supprimer des livres dont l'auteur est X :

![alt text](cours/image-45.png)

Supprimer un utilisateur par son email :

![alt text](cours/image-46.png)

Trier les livres par les notes de manière décroissante : 

![alt text](cours/image-47.png)

Trier les livres par les plus anciens : 

![alt text](cours/image-48.png)

Compter les livres par auteur : 

![alt text](cours/image-49.png)

Afficher uniquement le titre, l'auteur et la note moyenne :

![alt text](cours/image-50.png)


# TP Final 2

