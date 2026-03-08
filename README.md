# README - E-Commerce Web Site

## 🌐 Présentation du projet

Ce projet est un site web e-commerce interactif et responsive, permettant aux utilisateurs de naviguer parmi des produits, ajouter des articles à leur panier, remplir des formulaires et profiter d’animations modernes pour une expérience fluide.

L’application fonctionne **en front-end uniquement** et s’appuie sur **des APIs externes** pour simuler un environnement e-commerce réel (authentification, stockage, médias et paiement).
L’interface est entièrement responsive, adaptée aux mobiles, tablettes et ordinateurs.

---

# 🛠 1. Fonctionnalités principales (détaillées)

## 🛍 Panier d’achat

### ✅ Fonctionnalités

* Ajout dynamique de produits au panier
* Suppression d’un article
* Modification des quantités
* Calcul automatique du total
* Mise à jour en temps réel du compteur d’articles
* Sauvegarde locale avec `localStorage`
* Message de confirmation lors de l’ajout

### 🎓 Apprentissage

* Manipulation avancée du **DOM**
* Gestion d’événements (`addEventListener`)
* Utilisation des tableaux et objets en JavaScript
* Méthodes JS (`map`, `reduce`, `filter`)
* Persistance locale avec `localStorage`
* Synchronisation UI / données

### ⚙️ Installation / Mise en place

1. Créer une structure HTML pour le panier (sidebar ou modal).
2. Ajouter des boutons "Ajouter au panier" dans les cartes produits.
3. Créer une structure de données JS pour stocker les produits.
4. Implémenter les fonctions :

   * `addToCart()`
   * `removeFromCart()`
   * `updateCartTotal()`
5. Sauvegarder l’état du panier dans `localStorage`.

---

## 🃏 Cartes produit

### ✅ Fonctionnalités

* Affichage dynamique des produits via API
* Image produit
* Nom
* Description courte
* Prix
* Bouton d’ajout au panier
* Effets hover animés
* Badges (promotion, nouveauté)

### 🎓 Apprentissage

* Génération dynamique de composants UI
* Utilisation de **Flexbox & Grid**
* Structuration visuelle
* Responsive Design
* Animations CSS

### ⚙️ Installation

1. Récupérer les produits via une API REST.
2. Générer les cartes avec JavaScript.
3. Styliser `.product-card` avec `box-shadow` et `border-radius`.
4. Ajouter effets `hover` et responsive avec `@media queries`.

---

## 📝 Formulaires (Contact, Commande & Produits)

### ✅ Fonctionnalités

* Formulaire de contact
* Formulaire de commande
* Formulaire d’ajout de produit
* Validation en temps réel
* Messages d’erreur dynamiques
* Vérification des formats (email, champs requis)
* Feedback visuel (bordure rouge / verte)

### 🎓 Apprentissage

* Validation JavaScript
* Gestion des événements `submit`
* Expressions régulières (regex)
* UX Design
* Accessibilité (`label`, `aria`)
* Séparation logique / affichage

### ⚙️ Installation

1. Créer les formulaires HTML.
2. Empêcher l’envoi par défaut (`event.preventDefault()`).
3. Valider les données côté client.
4. Envoyer les données vers une API (POST).
5. Afficher les messages de succès ou d’erreur.

---

## 🎬 Animations

### ✅ Fonctionnalités

* Hover sur boutons
* Animation d’apparition des cartes produit
* Effet slide du panier
* Animation du compteur panier

### 🎓 Apprentissage

* `transition`
* `@keyframes`
* Manipulation dynamique des classes CSS
* Optimisation des performances visuelles

### ⚙️ Installation

* Ajouter transitions CSS.
* Créer animations avec `@keyframes`.
* Activer les animations via JavaScript.

---

## 🧠 DOM Manipulation

### ✅ Fonctionnalités

* Création dynamique d’éléments HTML
* Mise à jour en temps réel de l’interface
* Notifications utilisateur
* Filtrage et rafraîchissement des produits

### 🎓 Apprentissage

* `querySelector`
* `createElement`
* `appendChild`
* `classList`
* Gestion avancée des événements

### ⚙️ Installation

* Créer des fonctions JS réutilisables.
* Lier les événements aux éléments dynamiques.
* Tester via la console navigateur.

---

## 📱 Responsive Design

### ✅ Fonctionnalités

* Mobile First
* Menu adaptatif
* Grille produits responsive
* Panier optimisé pour mobile

### 🎓 Apprentissage

* Media Queries
* Flexbox
* CSS Grid
* Design adaptatif

### ⚙️ Installation

* Définir les breakpoints :

  * 480px (mobile)
  * 768px (tablette)
  * 1024px (desktop)
* Adapter tailles, grilles et espacements.

---

# 🔌 2. APIs intégrées (Version GitHub Pages)

## 📦 API de stockage (Produits)

### Rôle

* Stocker les produits
* Ajouter, modifier et supprimer des articles
* Charger dynamiquement le catalogue

### API utilisée

* **MockAPI**

### 🎓 Apprentissage

* Requêtes HTTP (`GET`, `POST`, `PUT`, `DELETE`)
* `fetch()` et `async/await`
* JSON
* Architecture API REST

---

## 🔐 API d’authentification

### Rôle

* Inscription utilisateur
* Connexion / déconnexion
* Gestion de l’état utilisateur

### API utilisée

* **Firebase Authentication**

### 🎓 Apprentissage

* Authentification sécurisée
* Gestion des sessions côté client
* Séparation front / auth provider

---

## 🖼 API médias (Images)

### Rôle

* Hébergement des images produits
* Récupération d’URLs sécurisées

### API utilisée

* **Cloudinary**

### 🎓 Apprentissage

* Upload de médias
* Gestion des ressources externes
* Optimisation des performances visuelles

---

## 💳 API paiement (Simulation)

### Rôle

* Simulation du processus de paiement
* Validation du panier avant commande

### API utilisée

* **Stripe** *(mode test uniquement)*

### 🎓 Apprentissage

* Intégration d’une API tierce
* Gestion d’un flux de paiement
* Sécurité et bonnes pratiques (sandbox)

---

# 🎨 3. Palette de couleurs (Approche professionnelle)

## 🎯 Objectif

Créer une identité visuelle cohérente basée sur un logo **bleu et orange** :

* 🔵 Bleu → Confiance, sécurité, technologie
* 🟠 Orange → Action, dynamisme, conversion

## 🌈 Variables CSS

```css
:root {
  --primary-blue: #1E90FF;
  --secondary-orange: #FFA500;
  --background-light: #F9F9F9;
  --text-dark: #333333;
  --accent-color: #FF6F00;
  --card-background: #FFFFFF;
  --border-color: #E0E0E0;
}
```

---

# 📂 4. Structure du projet (Professionnelle)

```
ecommerce-site/
├─ index.html
├─ login.html
├─ register.html
├─ styles/
│  ├─ variables.css
│  ├─ base.css
│  ├─ components.css
│  ├─ layout.css
├─ scripts/
│  ├─ main.js
│  ├─ cart.js
│  ├─ products.js
│  ├─ auth.js
│  ├─ api/
│  │  ├─ storage.api.js
│  │  ├─ auth.api.js
│  │  ├─ media.api.js
│  │  └─ payment.api.js
├─ assets/
│  ├─ images/
│  ├─ icons/
└─ README.md
```

---

# ⚙️ 5. Technologies utilisées

* **HTML5**
* **CSS3**
* **JavaScript (ES6+)**
* **APIs REST**
* **Git & GitHub Pages**

---

# 🚀 Installation complète du projet

1. Cloner le projet

```bash
git clone https://github.com/username/Nstore-ecommerce.git
```

2. Ouvrir le dossier

```bash
cd Nstore-ecommerce
```

3. Lancer
   Ouvrir `index.html` ou utiliser Live Server.

---

# 💡 Bonnes pratiques intégrées

* Code structuré et commenté
* Séparation des responsabilités
* APIs modulaires
* Variables CSS centralisées
* Responsive optimisé
* Accessibilité respectée
* Architecture évolutive