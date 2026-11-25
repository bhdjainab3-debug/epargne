# 🌸 Mon épargne

Une petite application pour suivre ton épargne vers un objectif. Sa mission : **te demander le moins d'effort possible, une fois par mois.**

- Tu entres le **solde de ton compte épargne** (un seul champ).
- Tu importes le **relevé CSV de ta banque** : les dépenses sont classées automatiquement par catégorie, et l'appli retient tes corrections.
- Le tableau de bord montre ta progression, ta trajectoire, ce qu'il faut épargner chaque mois, tes dépenses par catégorie, des alertes et une projection.

🔒 **Tes données restent sur ton appareil.** Pas de connexion à ta banque, rien n'est envoyé sur internet. Tout est enregistré dans le navigateur de ton téléphone ou de ton ordinateur.

---

## 1. Mettre l'appli en ligne (une seule fois, environ 5 minutes)

L'appli est une page web. Pour l'ouvrir sur iPhone, il lui faut une adresse (un lien). GitHub en fournit une gratuitement avec **GitHub Pages**.

> ⚠️ GitHub Pages n'est gratuit que pour les projets **publics**. Rendre le projet public montre le **code** de l'appli, **jamais tes chiffres** : ils restent dans ton navigateur et ne vont jamais dans le projet. Les données d'exemple (noms, montants) sont inventées.

1. Va sur **github.com** et ouvre le projet **epargne**.
2. Clique sur **Settings** (l'icône d'engrenage, en haut à droite du projet).
3. *Rendre le projet public* : tout en bas de la page, dans **Danger Zone**, clique sur **Change visibility** → **Make public**, puis confirme.
4. Dans le menu de gauche, clique sur **Pages**.
5. Sous **Build and deployment** → **Source**, choisis **Deploy from a branch**.
6. Sous **Branch**, choisis la branche qui contient l'appli (`main` une fois le travail fusionné, sinon `claude/savings-tracker-app-s2hhd9`), dossier **/ (root)**, puis **Save**.
7. Attends 1 à 2 minutes, puis recharge la page : GitHub affiche l'adresse de ton appli, du genre
   `https://bhdjainab3-debug.github.io/epargne/`

## 2. L'installer sur ton iPhone

1. Ouvre le lien ci-dessus dans **Safari** (pas dans Chrome).
2. Touche le bouton **Partager** (le carré avec une flèche vers le haut).
3. Choisis **Sur l'écran d'accueil**, puis **Ajouter**.
4. Une icône de fleur rose 🌸 apparaît : à partir de maintenant, **ouvre toujours l'appli depuis cette icône**.

> 💡 Sur iPhone, l'appli ouverte depuis l'icône et l'appli ouverte dans Safari ont chacune leur propre mémoire. Utilise toujours l'icône pour retrouver tes données.

## 3. Sur ton ordinateur

- Ouvre le même lien dans ton navigateur habituel (Chrome, Safari, Edge, Firefox) et ajoute-le à tes favoris.
- **Sans internet / sans GitHub** : tu peux aussi télécharger `index.html` et l'ouvrir d'un double-clic. Ça marche de la même façon.

> 💡 L'iPhone et l'ordinateur **ne se synchronisent pas** (c'est le prix du « rien ne part en ligne »). Choisis un appareil principal pour ta mise à jour mensuelle. Pour passer tes données de l'un à l'autre : **Réglages → Sauvegarder** sur le premier, puis **Réglages → Restaurer une sauvegarde** sur le second.

---

## Ta routine mensuelle (2 minutes)

Au début de chaque mois, ouvre l'appli → onglet **Mon mois** :

1. **Mon solde d'épargne** : regarde dans l'appli ING le montant de ton compte épargne, tape-le, **Enregistrer**.
2. **Mon relevé ING** : exporte le fichier CSV du mois écoulé (les explications sont dans l'appli, sous « Comment obtenir le fichier chez ING ? »), puis **Choisir mon fichier CSV**.
3. S'il reste des opérations « À classer » : choisis leur catégorie **une seule fois**. L'appli crée une règle et ne te le redemandera plus.
4. **Réglages → Sauvegarder (télécharger)** pour garder une copie de secours (range-la dans iCloud Drive).

C'est tout. Le tableau de bord se met à jour tout seul.

## Comment les calculs fonctionnent

- **Trajectoire nécessaire** : ton objectif est réparti **en proportion de tes revenus prévus**. Tu gagnes ~620 €/mois de février à juin, puis ~1 950 €/mois en juillet-août. L'appli s'attend donc à ce que tu épargnes davantage l'été, quand tu gagnes plus. C'est plus réaliste qu'une ligne droite.
- **À épargner chaque mois** : ce qui reste à épargner, réparti sur les mois restants de la même façon (selon tes revenus).
- **Projection** : ton taux d'épargne réel jusqu'ici (montant épargné ÷ revenus reçus) appliqué aux revenus encore à venir.
- **Alertes sur les dépenses** : comparaison des deux derniers mois importés, catégorie par catégorie (alerte si une catégorie augmente de plus de 25 % et de plus de 15 €).

Tout se modifie dans **Réglages** : objectif, date limite, début du suivi, revenus prévus mois par mois, noms des catégories, règles de classement.

## Essayer tout de suite

Avant février 2027, clique sur **« Voir un exemple »** dans le tableau de bord : l'appli se remplit de données inventées pour que tu puisses explorer. Tu peux aussi importer le fichier `exemple-releve-ing.csv` (un faux relevé ING) pour voir le classement automatique en action. Ensuite, **« Effacer l'exemple et commencer »**.

## Les fichiers du projet

| Fichier | À quoi il sert |
|---|---|
| `index.html` | Toute l'appli (affichage + calculs) |
| `manifest.webmanifest`, `icon-*.png` | Nom et icône pour l'écran d'accueil de l'iPhone |
| `sw.js` | Permet d'ouvrir l'appli sans connexion internet |
| `exemple-releve-ing.csv` | Un faux relevé ING pour tester l'import |
