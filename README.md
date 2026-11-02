# MAINTiDOC — Assistant Documentaire Multimodal et Agentique pour la Maintenance

[![Module](https://img.shields.io/badge/Module-IA%20G%C3%A9n%C3%A9rative%20Multimodale-blue)](https://emsi.ma)
[![Promo](https://img.shields.io/badge/EMSI-5IA%20%26%20DATA%202026-green)](#)
[![Statut](https://img.shields.io/badge/Livrable%201-Valid%C3%A9-brightgreen)](#)

Assistant documentaire multimodal et agentique conçu pour les techniciens et responsables de maintenance industrielle et automobile (systèmes FAP et SCR).

---

## 👥 Équipe de Développement (EMSI 2026)
* **CHAOUAY** 
* **REDDAD**  
* **Enseignante :** Prof. Mariam CHERRABI

---

## 📁 Structure du Dépôt

```text
maintidoc/
├── README.md                 # Présentation du projet et guide d'exécution
├── .gitignore                # Exclusion des secrets, venv et caches
├── docker-compose.yml        # Infrastructure (Qdrant, MinIO, PostgreSQL, MLflow)
├── docs/
│   └── diagrammes/           # Sources Mermaid des architectures et flux
│       ├── architecture.mmd  # Schéma par blocs fonctionnels
│       └── flux_requete.mmd  # Diagramme de séquence (parcours d'une requête)
└── corpus/
    ├── inventaire.csv        # Registre normé des 43 documents (20 colonnes)
    ├── prompts_corpus.md     # Journal des prompts IA et analyse critique
    ├── documents/
    │   ├── famille_1/        # 22 fiches PDF techniques FAP
    │   └── famille_2/        # 21 fiches PDF techniques SCR
    └── images/               # 40 photographies et schémas réels indexés
```

---

## 🎯 Périmètre et Caractéristiques

1. **RAG Multimodal :** Indexation de passages textuels et photographies réelles avec recherche hybride dense et visuelle.
2. **Modèle Vision-Langage (VLM) :** Qwen2.5-VL-7B-Instruct pour l'interprétation des voyants et schémas techniques.
3. **Citations Vérifiables :** Chaque réponse générée cite précisément le document, la page et la figure associée.
4. **Outils MCP :** Interaction avec le système d'atelier pour l'historique et la création de tickets d'intervention.
5. **Human-in-the-Loop :** Aucune création de ticket sans validation humaine explicite via jeton sécurisé.
