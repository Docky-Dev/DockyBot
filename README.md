# 📊 Fetch MrBeast Subs (via GitHub App)

**Fetch MrBeast Subs** est un workflow GitHub Actions qui récupère automatiquement le **nombre d’abonnés YouTube de MrBeast** toutes les 5 minutes, via une **GitHub App** personnalisée.
Les données sont ensuite enregistrées dans un fichier `mrbeast.json` et poussées sur le dépôt GitHub, permettant un suivi en temps réel des abonnés.

---

## 🚀 Fonctionnement

Le script utilise :

* **Mixerno API** → pour obtenir le nombre d’abonnés de la chaîne YouTube de MrBeast
* **GitHub App** → pour authentifier et publier les mises à jour automatiquement
* **GitHub Actions (cron)** → pour exécuter la tâche toutes les 5 minutes sans intervention manuelle

---

## ⚙️ Configuration

### 1. Secrets à ajouter dans ton dépôt

Dans ton dépôt GitHub, va dans **Settings → Secrets → Actions** et ajoute ces trois valeurs :

| Nom du secret     | Description                                   |
| ----------------- | --------------------------------------------- |
| `APP_ID`          | ID de ton GitHub App                          |
| `INSTALLATION_ID` | ID de l’installation de ton App sur ton dépôt |
| `PRIVATE_KEY`     | Clé privée (au format PEM) de ton App         |


---

## 📁 Résultat

Un fichier `mrbeast.json` contenant la dernière valeur récupérée :

```json
{
  "subscriberCount": "268512345"
}
```

---

## 💡 Objectif

Ce projet sert d’exemple pour :

* apprendre à utiliser une **GitHub App** dans un workflow Actions,
* automatiser la mise à jour de données externes,
* stocker et suivre l’évolution de statistiques en temps réel.

---

## 👤 Auteur

**Projet développé par [DevXCat](https://github.com/DevXCat)**
GitHub App utilisée : **DockyBot**
