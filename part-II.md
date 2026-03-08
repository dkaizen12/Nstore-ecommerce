# 📂 Arborescence finale (rappel)

ecommerce-site/
├─ index.html
├─ login.html
├─ register.html
│
├─ styles/
│  ├─ variables.css
│  ├─ base.css
│  ├─ layout.css
│  └─ components.css
│
├─ scripts/
│  ├─ main.js
│  ├─ cart.js
│  ├─ products.js
│  ├─ auth.js
│  ├─ forms.js
│  └─ api/
│     ├─ storage.api.js
│     ├─ auth.api.js
│     ├─ media.api.js
│     └─ payment.api.js
│
├─ assets/
│  ├─ images/
│  └─ icons/
│
└─ README.md

---

# 🧠 UTILITÉ DE CHAQUE FICHIER (DÉTAILLÉ)

---

## 🟦 HTML

### `index.html`

🎯 **Rôle**

* Page principale du site
* Affichage des produits
* Panier
* Navigation

🔗 **Connexions**

* Charge tous les fichiers CSS
* Charge `main.js`
* Déclenche le chargement des produits via `products.js`

---

### `login.html`

🎯 **Rôle**

* Connexion utilisateur

🔗 **Connexions**

* CSS commun
* `auth.js`
* `forms.js`
* API Auth (`auth.api.js`)

---

### `register.html`

🎯 **Rôle**

* Inscription utilisateur

🔗 **Connexions**

* CSS commun
* `auth.js`
* `forms.js`
* API Auth (`auth.api.js`)

---

## 🎨 CSS

### `styles/variables.css`

🎯 **Rôle**

* Design System
* Variables globales (couleurs, ombres, états)
* Mode sombre

🔗 **Connexions**

* Utilisé par TOUS les autres fichiers CSS

---

### `styles/base.css`

🎯 **Rôle**

* Reset CSS
* Styles globaux (`body`, `a`, `img`)
* Typographie

🔗 **Connexions**

* Dépend de `variables.css`

---

### `styles/layout.css`

🎯 **Rôle**

* Structure du site
* Header, footer, grid
* Containers
* Responsive layout

🔗 **Connexions**

* Utilise les variables
* Affecte la structure globale

---

### `styles/components.css`

🎯 **Rôle**

* Composants UI réutilisables
* Cartes produit
* Boutons
* Formulaires
* Modales
* Panier

🔗 **Connexions**

* Utilise `variables.css`
* Appliqué aux éléments HTML générés par JS

---

## ⚙️ JavaScript – Core

### `scripts/main.js`

🎯 **Rôle**

* Point d’entrée JS
* Initialise l’application
* Lance le chargement des produits
* Initialise le panier
* Gère le thème (light/dark)

🔗 **Connexions**

* Appelle `products.js`
* Appelle `cart.js`
* Initialise l’état global

---

### `scripts/products.js`

🎯 **Rôle**

* Gestion des produits
* Affichage des cartes produit
* Interaction avec l’API produits

🔗 **Connexions**

* Appelle `storage.api.js`
* Crée du DOM utilisé par `cart.js`

---

### `scripts/cart.js`

🎯 **Rôle**

* Logique panier
* Ajout / suppression
* Calcul total
* Persistance locale

🔗 **Connexions**

* Reçoit les produits depuis `products.js`
* Utilise `localStorage`

---

### `scripts/forms.js`

🎯 **Rôle**

* Validation de tous les formulaires
* Gestion UX des erreurs

🔗 **Connexions**

* Utilisé par `login.html`, `register.html`
* Utilisé par formulaire ajout produit

---

### `scripts/auth.js`

🎯 **Rôle**

* Gestion de l’état utilisateur
* Connexion / déconnexion
* Rôles (admin / user)

🔗 **Connexions**

* Utilise `auth.api.js`
* Communique avec les pages HTML

---

## 🔌 JavaScript – APIs

### `api/storage.api.js`

🎯 **Rôle**

* Communication avec l’API produits
* CRUD produits

🔗 **Connexions**

* Utilisé par `products.js`
* Utilisé par formulaire ajout produit

---

### `api/auth.api.js`

🎯 **Rôle**

* Communication avec l’API d’authentification

🔗 **Connexions**

* Utilisé par `auth.js`
* Utilisé par `login.html`, `register.html`

---

### `api/media.api.js`

🎯 **Rôle**

* Gestion des images produits
* Upload
* Récupération URL

🔗 **Connexions**

* Utilisé par formulaire ajout produit
* Retourne URLs pour `products.js`

---

### `api/payment.api.js`

🎯 **Rôle**

* Simulation paiement
* Validation commande

🔗 **Connexions**

* Utilisé par `cart.js`
* Utilisé lors du checkout

---

## 🖼 Assets

### `assets/images/`

🎯 **Rôle**

* Images statiques
* Logos
* Bannières

---

### `assets/icons/`

🎯 **Rôle**

* Icônes UI
* SVG

---

## 📘 README.md

🎯 **Rôle**

* Documentation projet
* Présentation recruteur
* Instructions

---

# 🔗 FLUX GLOBAL (COMMENT TOUT SE CONNECTE)

```
index.html
   ↓
main.js
   ↓
products.js → storage.api.js
   ↓
cart.js
   ↓
payment.api.js
```

```
login.html / register.html
   ↓
forms.js
   ↓
auth.js
   ↓
auth.api.js
```

```
formulaire ajout produit
   ↓
media.api.js
   ↓
storage.api.js
   ↓
products.js
```

---

# 🎯 Pourquoi cette architecture est excellente

✔️ Séparation claire
✔️ Lisible
✔️ Testable
✔️ Évolutive
✔️ Pro