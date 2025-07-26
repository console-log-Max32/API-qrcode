# 🧩 QR Code Generator API

Une API simple, rapide et **ultra-flexible** pour générer des QR codes en base64 via requête HTTP.  
Utilisable dans **toutes sortes de projets** : web, mobile, desktop ou backend.

---

## ✨ Fonctionnalités

- Génération de QR codes en base64
- Personnalisation des couleurs (`dark`, `light`)
- Choix de la taille du QR code
- Accès via POST HTTP (JSON)
- Facile à intégrer dans n’importe quel type de projet

---

## 🌐 Lien de l'api

http://88.151.197.191:2025/qrcode

---

## 🚀 Exemple d’appel

```js
fetch('http://' + '88.151.197.191:2025/qrcode' + '/generate', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ text: 'exemple', size: 300, dark: '#000080', light: '#a0a0a0' })
}) 
.then(res => res.json())
.then(data => {
  console.log(data.image);
});
````

### ✅ Réponse :

```json
{
  "image": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAA..."
}
```

---

## 🔧 Paramètres acceptés

| Champ   | Type   | Description                            | Par défaut        |
| ------- | ------ | -------------------------------------- | ----------------- |
| `text`  | string | **Contenu à encoder** dans le QR code  | — *(obligatoire)* |
| `size`  | number | Taille du QR code en pixels            | `256`             |
| `dark`  | string | Couleur des éléments noirs du QR code  | `#000000`         |
| `light` | string | Couleur de fond du QR code             | `#FFFFFF`         |

---

## 🛠️ Cas d’usage

Cette API est **générique** : elle peut être utilisée pour générer des QR codes dans **toutes sortes de scénarios**, pas seulement ceux en exemple.

### 🔍 Exemples d’utilisation :

* **Sites web** : QR pour partager une URL ou une ressource
* **Applications mobiles** : QR pour authentification ou paiement
* **E-commerce** : QR sur un reçu ou une étiquette produit
* **Événementiel** : QR badge personnalisé pour chaque participant
* **Wi-Fi Guest Access** : QR de connexion rapide au réseau
* **Systèmes de réservation** : QR pour billet d'entrée numérique
* **Embeds Discord** : intégration dans des messages embeds (image base64 directe)

---

## 🌐 Exemple d’intégration web

Un exemple concret d’appel depuis une page HTML est fourni dans le fichier [`qrcodeApi.html`](./qrcodeApi.html).

---

## 🧠 À propos

Cette API a été pensée pour être **ultra-simple**, **modulaire**, et **prête à intégrer partout**.
Aucune dépendance lourde. Aucun service externe.

Besoin d’une fonctionnalité en plus ? Écris-nous sur Discord :

* [@console.log(" *x1 ")](https://discord.com/users/1066067393123733595)
* [@! ℳ𝓪𝔁𝟑𝟐](https://discord.com/users/1163887501895815168)

---

## Vu total de nos API
<img src='https://komarev.com/ghpvc/?username=console-log-Max32-API&style=for-the-badge'>

---

> 🛠️ Maintenu par des développeurs **amateurs ET bénévoles** — soyez cool avec nous ✊

> Chatgpt nous as permis d'économiser du temps en rédigeant à notre place le fichier d'exemple (html) et le readme. Je pense que je n'apprends rien à personne en précisant que cet outil magique a encore besoin d'une supervision humaine.
