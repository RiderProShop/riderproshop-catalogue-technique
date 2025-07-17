# Catalogue Rider Pro Shop (FR)

Bienvenue ! Ce dépôt open‑source contient :

- **categories_fr.json** : structure des catégories et sous‑catégories du site RiderProShop.com/fr  
- **products_fr.json** : liste des produits avec prix, images et descriptions courtes  
- **guides/** : tutoriels techniques Markdown pour l’entretien et le choix d’équipements  

---

## Structure du repo

riderproshop-catalogue-technique/
├── docs/
│ └── fr/
│ ├── categories_fr.json
│ ├── products_fr.json
│ └── guides/
│ └── … (tutoriels Markdown)
└── README.md (index général)

## Guides disponibles

- [Le bon quad électrique enfant : comment choisir](guides/le-bon-quad-electrique-enfant-comment-choisir.md)
- [Moto thermique pour un enfant de 6 ans : comment choisir](guides/moto-thermique-pour-un-enfant-de-6-ans-comment-choisir.md)
- [Choisir une pocket bike](guides/choisir-une-pocket-bike.md)
- [Choisir une moto cross pour un enfan](guides/choisir-une-moto-cross-pour-un-enfant.md)
- [Choisir le bon quad thermique pour un enfant de 3 ans](guides/choisir-le-bon-quad-thermique-pour-un-enfant-de-3-ans.md)
- [Choisir le bon quad enfant](guides/choisir-le-bon-quad-enfant.md)

## Exemple d’utilisation en JavaScript

```js
// Récupérer le catalogue des catégories
const categories = await fetch(
  'https://raw.githubusercontent.com/riderproshop/riderproshop-catalogue-technique/main/docs/fr/categories_fr.json'
)
  .then(res => res.json())
  .then(data => data.categories);

// Récupérer la liste des produits
const products = await fetch(
  'https://raw.githubusercontent.com/riderproshop/riderproshop-catalogue-technique/main/docs/fr/products_fr.json'
)
  .then(res => res.json())
  .then(data => data.products);

console.log(categories);
console.log(products);
