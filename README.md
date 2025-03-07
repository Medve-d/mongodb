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

Afficher les utilisateurs qui ont plus d'un livre emprunté :

![alt text](cours/image-51.png)

Afficher les livres avec $regex :

![alt text](cours/image-52.png)

afficher les livres entre 10€ et 20€ :

![alt text](cours/image-53.png)

# Création d'une collection emprunts
Commande pour créé et inclures les emprunt en cours :

![alt text](cours/image-54.png)

Comparez cette approche : 

cette approche permet de regroupé directement les emprunts en cours dans une collection, cela évite d'une part que si un utilisateur est supprimé, les emprunts en cours ne le soient pas et d'autre part cela permet de faire des recherches plus rapides sur les emprunts en cours, également de faire une indexisation sur cette collection.

# TP Final 2

Pour créer 1000 livres j'ai eu recours à un code javascript me permettant d'en générer :

```
import fs from "fs";

function genererLivreAleatoire(id, titres, auteurs, editeurs, genres, langues) {
  const titre = titres[Math.floor(Math.random() * titres.length)];
  const auteur = auteurs[Math.floor(Math.random() * auteurs.length)];
  const annee_publication = Math.floor(Math.random() * (2023 - 1500 + 1)) + 1500;
  const editeur = editeurs[Math.floor(Math.random() * editeurs.length)];
  const genre = genres[Math.floor(Math.random() * genres.length)];
  const nombre_pages = Math.floor(Math.random() * (1000 - 50 + 1)) + 50;
  const langue = langues[Math.floor(Math.random() * langues.length)];
  const disponible = Math.random() < 0.8;
  const stock = Math.floor(Math.random() * 5) + 1;
  const note_moyenne = (Math.random() * (5 - 3) + 3).toFixed(1);
  const description = "Description aléatoire du livre " + titre + " de " + auteur + ".";
  const prix = (Math.random() * (20 - 5) + 5).toFixed(2);
  const isbn = "978" + Math.floor(Math.random() * 10000000000).toString();
  const date_ajout = new Date(new Date().getTime() - Math.random() * 365 * 24 * 60 * 60 * 1000);

  return {
    titre: titre,
    auteur: auteur,
    annee_publication: annee_publication,
    editeur: editeur,
    genre: genre,
    nombre_pages: nombre_pages,
    langue: langue,
    disponible: disponible,
    stock: stock,
    note_moyenne: parseFloat(note_moyenne),
    description: description,
    prix: parseFloat(prix),
    isbn: isbn,
    date_ajout: date_ajout
  };
}

const titres = Array.from({ length: 500 }, (_, i) => `Titre ${i + 1}`);
const auteurs = Array.from({ length: 250 }, (_, i) => `Auteur ${i + 1}`);
const editeurs = Array.from({ length: 100 }, (_, i) => `Éditeur ${i + 1}`);
const genres = Array.from({ length: 25 }, (_, i) => [`Genre ${i + 1}`, `Sous-genre ${i + 1}`]);
const langues = ["Français", "Anglais", "Espagnol", "Allemand", "Italien", "Russe", "Chinois", "Japonais", "Arabe", "Portugais"];

const livres = [];
for (let i = 0; i < 1000; i++) {
  livres.push(genererLivreAleatoire(i, titres, auteurs, editeurs, genres, langues));
}

const livresJSON = JSON.stringify(livres, null, 2);

fs.writeFile('livres_1000.json', livresJSON, (err) => {
  if (err) {
    console.error('ERREUR', err);
  } else {
    console.log('Les livres ont été générés et enregistrés dans livres_1000.json');
  }
});
```

# Voici les screen pour analyser les performances des requêtes sans index:

 ### Analyse avec la recherche de titre

![alt text](cours/image-55.png)

### Analyse avec l'auteur 

![alt text](cours/image-56.png)

### Analyse avec la recherche d'un livre entre 10€ et 20€ et tri par note minimal 

![alt text](cours/image-57.png)

## /!\ J'ai changé la collections livre pour rechercher par le genre et la langue et tri par note décroissante

![alt text](cours/image-58.png)

# Création d'index 

Pour titre et auteur on a fait un index simple car, pour la recherche demandé il n'y pas beaucoup d'options

![alt text](cours/image-59.png)

Pour les index composé, on va les privilégier pour les recherches avec des filtres et des tris par exemple

![alt text](cours/image-60.png)

![alt text](cours/image-61.png)

Je ne constate pas particulièrement des améliorations pour les recherches par titre et auteur mais pour les recherches avec des filtres et des tris, les performances sont bien meilleures.

### 1.3

Depuis un index créé sur le champ titre et description, la recherche a pris executionTimeMillis: 0, et totalDocsExamined: 1.

La recherche est beaucoup plus optimisé.

### 1.4 

Une requête couverte a bien donné totalDocsExamined : 0

![alt text](cours/image-62.png)

Après avoir créé un index pour rendre un isbn unique, j'ai essayé d'ajouté un livre avec un isbn déjà existant.

![alt text](cours/image-63.png)

J'ai lancé en local mais rien ne prend + de 100ms  

![alt text](cours/image-64.png)

5 > Je n'ai pas trouvé d'index lent ou pas utilisé 

## TABLEAU RESULTATS

Avant index :
| Requête | totalDocsExamined | executionTimeMillis | Type d'étape |
|---------|-------------------|---------------------|--------------|
| Titre   | 1000              | 1                  | COLLSCAN       |
| Auteur   | 1000               | 1                  | COLLSCAN       |
| Plage prix et note : <  | 1000               | 2                  | SORT        |
| Genre langue et note : >  | 1000               | 1                  | SORT        |

Après index : 


| Requête | totalDocsExamined | executionTimeMillis | Type d'étape |
|---------|-------------------|---------------------|--------------|
| Titre   | 4              | 0                  | FETCH      |
| Auteur   | 4               | 0                  | FETCH      |
| Plage prix et note : <  | 645               | 2                  | SORT       |
| Genre langue et note : >  | 4               | 2                  | Fetch        |


## 2 . Rapport :

1. Je constate que les requêtes sont beaucoup plus optimisées après l'ajout d'index. recherche dans moins de collections et temps d'exécution réduit.

2. Les meilleurs index sont ceux qui sont composé et qui permettent de faire des recherches avec des filtres et des tris

3. L'écriture demande plus de temps que la lecture

# TP2
2.1  
Dans ce code on va trouver tous les utilisateurs autour de la bibliothèque national de France

![alt text](cours/image-65.png)

2.2 
Dans code on va chercher les bibliothèque autour d'un utilisateur
![alt text](cours/image-66.png)

2.3

# TP 3

3.1 

Voici la commande pour faire des statistique sur le genre des livres 

![alt text](cours/image-67.png)

Voici la même commande mais pour les éditeurs : 

![alt text](cours/image-68.png)