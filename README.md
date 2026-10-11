# Générateur Générique de Contrats Commerciaux (JSON ⇄ XML)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![JSON/XML](https://img.shields.io/badge/Interopérabilité-JSON%20%E2%87%84%20XML-2563eb?style=flat-square)
![Tailscale](https://img.shields.io/badge/Hosted_with-Tailscale_Funnel-24292e?style=flat-square&logo=tailscale)

Application web légère et sans dépendances permettant d'établir dynamiquement des contrats de transactions commerciales à partir d'un **moteur de templating générique** et d'assurer l'**interopérabilité des données** entre les formats **JSON** et **XML**.

---

##  Objectifs du Projet

Ce projet répond à trois exigences d'ingénierie logicielle et d'échange de données informatisé (EDI) :

1. **Développement de l'outil (`a`)** : Interface utilisateur ergonomique avec saisie en temps réel, aperçu au format feuille A4 et exportation directe en PDF / impression.
2. **Architecture générique (`b`)** : Découplage total entre les données et la vue grâce à un moteur de *templating* par balises (`{{groupe.propriete}}`). L'outil peut générer n'importe quel type de document juridique ou commercial sans modifier le code source.
3. **Format interopérable JSON à base XML (`c`)** : Structuration arborescente stricte permettant une bijection 1:1 en temps réel entre un objet **JSON** et un document **XML** valide.

---

##  Fonctionnalités Principales

* **Édition et prévisualisation en temps réel** : Toute modification dans le formulaire ou dans le modèle met à jour instantanément le contrat A4, le flux JSON et le flux XML.
* **Moteur de Template personnalisable** : Éditeur de modèle intégré permettant d'adapter les clauses du contrat à la volée via des variables dynamiques (`{{vendeur.nom}}`, `{{transaction.montant_ht}}`, etc.).
* **Sérialisation JSON & XML** : Conversion récursive automatique avec échappement des caractères spéciaux XML (`&`, `<`, `>`) et téléchargement en `.json` ou `.xml`.
* **Prêt pour l'impression (Print-friendly)** : Feuille de style `@media print` dédiée qui masque l'interface applicative pour ne conserver que le document officiel au format A4 lors de l'export PDF.

---

##  Structure du Projet

```text
.
├── index.html   # Structure de l'interface, moteur de templating JS et convertisseur JSON/XML
├── style.css    # Design system moderne (SaaS UI, aperçu feuille A4, règles @media print)
└── README.md    # Documentation du projet
