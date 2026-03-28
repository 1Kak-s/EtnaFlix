# EtnaFlix

Application mobile de découverte de films construite avec React Native et Expo. Elle permet de naviguer parmi les films tendances, populaires et les mieux notés, et d'accéder à des fiches détaillées pour chaque film.

---

## Fonctionnalites

- Consultation des films tendances (semaine), populaires et les mieux notes
- Recherche de films en temps reel par titre
- Fiche detaillee : synopsis, note, date de sortie, duree, genres
- Interface en langue francaise (contenu fourni via l'API TMDB)
- Compatible iOS, Android et Web

---

## Stack technique

| Technologie | Version |
|---|---|
| React Native | 0.81.5 |
| Expo | ~54.0.20 |
| React | 19.1.0 |
| React Navigation (Stack) | ^7.6.0 |
| Expo Linear Gradient | ^15.0.7 |
| React Native Web | ^0.21.0 |

---

## Structure du projet

```
EtnaFlix/
├── App.js                    # Composant racine
├── index.js                  # Point d'entree
├── app.json                  # Configuration Expo
├── assets/                   # Images et icones
└── src/
    ├── constants/
    │   └── theme.js          # Couleurs, espacements, config API
    ├── navigation/
    │   └── AppNavigator.jsx  # Navigation par pile (3 ecrans)
    ├── screens/
    │   ├── WelcomeScreen.jsx # Ecran d'accueil
    │   ├── HomeScreen.jsx    # Liste des films
    │   └── DetailScreen.jsx  # Detail d'un film
    └── services/
        └── tmdb.js           # Appels a l'API TMDB
```

---

## Navigation

```
WelcomeScreen
    └── HomeScreen
            └── DetailScreen
```

---

## API

L'application utilise l'API [TMDB (The Movie Database)](https://www.themoviedb.org/).

Endpoints utilises :

| Endpoint | Description |
|---|---|
| `GET /trending/movie/week` | Films tendances de la semaine |
| `GET /movie/popular` | Films populaires |
| `GET /movie/top_rated` | Films les mieux notes |
| `GET /search/movie` | Recherche par titre |
| `GET /movie/{id}` | Detail d'un film (credits inclus) |

La cle API et l'URL de base sont configurees dans `src/constants/theme.js`.

---

## Installation

### Prerequis

- Node.js >= 18
- npm ou yarn
- Expo CLI : `npm install -g expo-cli`
- Application Expo Go sur votre appareil mobile (optionnel pour tester sur device)

### Lancer le projet

```bash
cd EtnaFlix
npm install
npm start
```

Choisissez ensuite la plateforme cible :

```bash
npm run android   # Android
npm run ios       # iOS
npm run web       # Navigateur
```

---

## Configuration

Le theme et la configuration de l'API se trouvent dans `src/constants/theme.js` :

- **Couleur primaire** : `#6366f1` (indigo)
- **Couleur de fond** : `#0f172a` (bleu nuit)
- **URL de base TMDB** : `https://api.themoviedb.org/3`
- **URL des images** : `https://image.tmdb.org/t/p`

---

## Auteur

Projet realise dans le cadre d'une activite ETNA — groupe goeffi_m 1065575.
