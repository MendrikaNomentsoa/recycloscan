# ♻️ RecycloScan

> Application web de tri intelligent des déchets par IA — destinée aux écoles et entreprises en Afrique.

![Stack](https://img.shields.io/badge/Backend-Spring%20Boot%204.1-6DB33F?style=flat-square&logo=springboot)
![Stack](https://img.shields.io/badge/Frontend-React%2019-61DAFB?style=flat-square&logo=react)
![Stack](https://img.shields.io/badge/IA-Gemini%20Vision-4285F4?style=flat-square&logo=google)
![Stack](https://img.shields.io/badge/Database-PostgreSQL-336791?style=flat-square&logo=postgresql)

---

## 📦 Repositories

| Projet | Description | Lien |
|---|---|---|
| **recycloscan-backend** | API REST Spring Boot + Gemini Vision | [Voir le repo →](https://github.com/MendrikaNomentsoa/recycloscan-backend) |
| **recycloscan-frontend** | Interface React + WebRTC | [Voir le repo →](https://github.com/MendrikaNomentsoa/recycloscan-frontend) |

---

## 🎯 Concept

L'utilisateur scanne un déchet via sa caméra. Google Gemini Vision identifie l'objet et retourne :
- La **poubelle correcte** (jaune, verte, bleue, marron, grise)
- Le **matériau** (PET, verre, aluminium...)
- Une **explication éducative** sur la recyclabilité
- Une **astuce** adaptée au contexte local africain

---

## ✨ Fonctionnalités

**Scan & IA**
- Capture photo via caméra navigateur (WebRTC)
- Reconnaissance d'image par Google Gemini Vision API
- Fallback sur recherche textuelle
- Explication éducative générée par IA

**Gamification**
- Système de points par scan
- 5 niveaux de progression (Débutant → Champion)
- 8 badges débloquables
- Leaderboard communautaire
- Défis hebdomadaires personnalisés

**Dashboard & Analytics**
- Statistiques personnelles et graphiques interactifs
- Impact environnemental (kg CO₂ économisé, arbres équivalents)
- Activité des 7 derniers jours

**Assistant IA**
- Chat conversationnel avec Gemini sur le recyclage
- Conseils personnalisés selon les habitudes de l'utilisateur
- Adapté au contexte africain

---

## 🛠️ Stack technique

### Backend — [recycloscan-backend](https://github.com/MendrikaNomentsoa/recycloscan-backend)
Java 21 · Spring Boot 4.1 · Spring Security · JWT
Spring Data JPA · PostgreSQL · Google Gemini Vision API

### Frontend — [recycloscan-frontend](https://github.com/MendrikaNomentsoa/recycloscan-frontend)
React 19 · Vite · Tailwind CSS · Recharts · Axios · WebRTC

---

## 🚀 Lancer le projet

### Prérequis
- Java 21
- Node.js 18+
- PostgreSQL
- Clé API Google Gemini ([obtenir ici](https://aistudio.google.com/apikey))

### Backend
```bash
git clone https://github.com/MendrikaNomentsoa/recycloscan-backend.git
cd recycloscan-backend
cp src/main/resources/application-example.properties src/main/resources/application.properties
# Remplir les valeurs dans application.properties
./mvnw spring-boot:run
```

### Frontend
```bash
git clone https://github.com/MendrikaNomentsoa/recycloscan-frontend.git
cd recycloscan-frontend
npm install
npm run dev
```

L'application est accessible sur [http://localhost:5173](http://localhost:5173)

---

## 📁 Architecture
recycloscan-backend/
├── controller/     ← Routes HTTP (Auth, Scan, User, Stats, Eco)

├── service/        ← Logique métier + appels Gemini

├── repository/     ← Accès base de données (Spring Data JPA)

├── entity/         ← Modèles (User, WasteItem, ScanHistory)

├── dto/            ← Objets de transfert (sécurité API)

├── config/         ← JWT, Spring Security, CORS

└── exception/      ← Gestion globale des erreurs

recycloscan-frontend/
├── pages/          ← Dashboard, Home, EcoAssistant, Leaderboard

├── components/     ← Navbar, ScanResult, DetectionCamera

├── api/            ← Axios avec intercepteur JWT

└── context/        ← AuthContext (gestion session)

---

## 👤 Auteur

**RAKOTOARISOA Ny Mendrika Nomentsoa** — [GitHub](https://github.com/MendrikaNomentsoa) 
