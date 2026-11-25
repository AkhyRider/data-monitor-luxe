<p align="center"><img src="visuels/banner.svg" alt="Data Monitor, benchmark des sacs de luxe" width="100%"></p>

> Où un vendeur de sacs de luxe doit-il se placer face à **Chanel, Goyard, Louis Vuitton et Balenciaga** ?
> On a récupéré les prix, tout nettoyé, monté un dashboard Power BI et tiré trois conseils concrets.

**Étude de cas complète et graphiques interactifs :** [portfolio-ay-kh.netlify.app/project-data-monitor](https://portfolio-ay-kh.netlify.app/project-data-monitor.html)

![Dashboard Power BI](visuels/dm-dashboard.webp)

## En chiffres

| 572 | 131 016 | 4 | 2 |
|:---:|:---:|:---:|:---:|
| références produits | avis clients | maisons comparées | sources (Vestiaire Collective, Trustpilot) |

## Méthode

1. **Récupérer (Python).** Un scraper `requests` + `BeautifulSoup` parcourt les pages catégorielles de Vestiaire Collective pour chaque marque : nom, prix, type de sac, lien. Les avis viennent de Trustpilot.
2. **Nettoyer (Power Query).** Dédoublonnage, typologies unifiées (sac à main, rabat, hobo, cabas & bowling), prix aberrants et devises hors euro filtrés : 572 lignes consolidées.
3. **Analyser (Power BI).** Mesures DAX (prix moyen, nombre de modèles, note moyenne pondérée), cartes KPI, graphiques et segments par marque et catégorie.

## Résultats

| Maison | Prix moyen | Note | Avis | Modèles |
|---|---:|---:|---:|---:|
| Chanel | 6 828 € | 4,49 | 9 642 | 123 |
| Goyard | 2 677 € | 4,62 | 13 920 | 88 |
| Louis Vuitton | 2 348 € | 4,59 | 67 151 | 108 |
| Balenciaga | 2 261 € | 4,59 | 40 303 | 253 |

- **Deux mondes de prix :** Chanel seule en ultra-premium, à 2,8 fois la moyenne des trois autres (2 429 €).
- **Un gap catalogue :** 78,5 % des références sont des sacs à main classiques ; rabat, hobo et cabas (21,5 %) ne sont proposés que par Chanel.

## Les trois recommandations

1. **Diversifier** : lancer une capsule de 3 à 5 modèles hobo ou à rabat dans le semestre.
2. **Viser le bon prix** : se positionner entre 2 200 et 2 800 €, avec un sac d'entrée de gamme autour de 2 400 €.
3. **Soigner la note** : auditer les 5 best-sellers et demander un avis automatiquement 15 jours après l'achat, pour viser plus de 4,60/5.

## Livrables

| Fichier | Contenu |
|---|---|
| [`livrables/data-monitor-rapport.pdf`](livrables/data-monitor-rapport.pdf) | Rapport d'analyse (5 pages) |
| [`livrables/data-monitor-slides.pdf`](livrables/data-monitor-slides.pdf) | Slides de soutenance (11 slides) |
| [`livrables/data-monitor-dashboard.pdf`](livrables/data-monitor-dashboard.pdf) | Export du dashboard |
| [`livrables/data-monitor-dashboard.pbix`](livrables/data-monitor-dashboard.pbix) | Fichier Power BI Desktop |

## Équipe

Groupe 11, HETIC : **Aymen Khlifi**, Louis Nourry, Marius Elberg.
