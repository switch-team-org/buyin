<div align="center">

# BUYIN.CC

**La plateforme e-commerce nouvelle génération pour l'Afrique et au-delà.**

Acheteurs et vendeurs connectés dans un écosystème fluide, intelligent et sécurisé.

[Site Web](https://buyin.cc) · [Signaler un bug](https://github.com/switch-team-org/buyin/issues) · [Demander une feature](https://github.com/switch-team-org/buyin/issues)

</div>

---

## Qu'est-ce que BUYIN.CC ?

BUYIN.CC est une plateforme e-commerce microservices pensée pour les marchés émergents. Elle permet à n'importe quel vendeur de créer sa boutique en ligne en quelques minutes, et aux acheteurs de découvrir des produits via une recherche sémantique alimentée par l'IA.

---

## Fonctionnalités

- Inscription et authentification sécurisée (JWT, OTP, OAuth)
- Profils vendeurs complets (boutique, branding, politiques)
- Catalogue produits avec variantes, stock et images
- Recherche sémantique par image et texte (FashionCLIP + FAISS)
- Génération automatique de descriptions SEO (Flan-T5)
- Panier persistant et gestion des commandes
- Likes, vues, commentaires, notes et wishlist
- Notifications email et SMS en temps réel
- Tableau de bord analytics pour les vendeurs

---

## Architecture

BUYIN.CC est construit sur une architecture microservices. Chaque service est indépendant, déployable séparément, et communique via REST et événements asynchrones (RabbitMQ).

```
Frontend (React 19)
       │
       ▼
BFF Service (Node.js) ── Gateway & Session Auth
       │
       ├── User Service (ASP.NET Core 8)
       ├── Product Catalog Service (Node.js + Prisma)
       ├── AI Service (Python + FastAPI)
       ├── Engagement Service (Node.js)
       ├── Cart Service (Node.js + Redis)
       ├── Order Service (Node.js + Prisma)
       ├── Notification Service (Node.js)
       └── Analytics Service (Node.js)

Infrastructure : PostgreSQL · Redis · RabbitMQ
```

---

## Stack technique

| Couche | Technologies |
|--------|-------------|
| Frontend | React 19, TypeScript, Vite, TanStack Query |
| Gateway | Node.js, Express, TypeScript |
| Auth | ASP.NET Core 8, EF Core, JWT, Redis |
| Catalog | Node.js, Prisma v7, PostgreSQL, S3/R2 |
| IA | Python, FastAPI, PyTorch, FashionCLIP, FAISS |
| Engagement | Node.js, Prisma, Socket.IO |
| Panier | Node.js, Redis |
| Commandes | Node.js, Prisma, PostgreSQL |
| Notifications | Node.js, Nodemailer, Handlebars |
| Analytics | Node.js, Prisma, Prometheus |
| Infra | Docker, Kubernetes, RabbitMQ, GitHub Actions |

---

## Services

| Service | Description | Repo |
|---------|-------------|------|
| front-buyin | Interface utilisateur React | [→](https://github.com/switch-team-org/front-buyin) |
| bff-service | Gateway & session auth | [→](https://github.com/switch-team-org/bff-service) |
| user-service | Auth & profils utilisateurs | [→](https://github.com/switch-team-org/user-service) |
| product-catalog-service | Catalogue produits | [→](https://github.com/switch-team-org/product-catalog-service) |
| ai-service | Embeddings & recherche sémantique | [→](https://github.com/switch-team-org/ia-images-service) |
| engagement-service | Likes, vues, commentaires | [→](https://github.com/switch-team-org/engagement-service) |
| cart-service | Panier d'achat | [→](https://github.com/switch-team-org/cart-service) |
| order-service | Gestion des commandes | [→](https://github.com/switch-team-org/order-service) |
| notification-service | Email & SMS | [→](https://github.com/switch-team-org/notification-service) |
| analytics-service | Métriques & tableaux de bord | [→](https://github.com/switch-team-org/analytics-service) |
| buyin-infra | Kubernetes & CI/CD | [→](https://github.com/switch-team-org/buyin-infra) |

---

## Roadmap

### Phase 1 — Fondations (Complété)
- [x] Authentification & gestion des utilisateurs
- [x] Profils vendeurs
- [x] Catalogue produits avec images S3/R2
- [x] Recherche sémantique IA
- [x] Panier & commandes
- [x] Notifications email/SMS
- [x] Engagement (likes, vues, commentaires)
- [x] Analytics

### Phase 2 — Croissance (En cours)
- [ ] Intégration paiement (Mobile Money, carte)
- [ ] Application mobile (React Native)
- [ ] Programme d'affiliation vendeurs
- [ ] Recommandations personnalisées

### Phase 3 — Scale
- [ ] Marketplace multi-pays
- [ ] Logistique intégrée
- [ ] Dashboard admin avancé
- [ ] API publique pour partenaires

---

## Contribuer

Tu veux contribuer à BUYIN.CC ? Super.

1. Fork le repo du service concerné
2. Crée une branche (`git checkout -b feature/ma-feature`)
3. Commit tes changements (`git commit -m 'feat: ma feature'`)
4. Push (`git push origin feature/ma-feature`)
5. Ouvre une Pull Request

---

## Contact

- Email : team@buyin.cc
- Issues : [GitHub Issues](https://github.com/switch-team-org/buyin/issues)

---

<div align="center">
Construit avec passion par l'équipe Switch
</div>
