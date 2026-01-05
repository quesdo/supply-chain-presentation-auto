# Supply Chain Virtual Twin Presentation - Mode Automatique

Présentation automatique du Virtual Twin de la Supply Chain avec défilement automatique des slides.

## Fonctionnalités

- **Défilement automatique**: La présentation avance automatiquement avec des timings prédéfinis
- **Un seul clic**: L'utilisateur clique sur "Start" et la présentation se déroule toute seule
- **Synchronisation 3D**: Les objets 3D de la supply chain s'affichent automatiquement via le SDK
- **Timings optimisés**: Chaque slide a une durée adaptée à la quantité de texte

## Structure de la présentation

### Slides avec timings:

1. **Introduction** (6s) - "Virtual Twin of the Supply Chain - Its role is simple:"
2. **SUP 1** (20s) - Anticipation et miroir de l'écosystème supply chain
3. **SUP 2** (15s) - Résultats et virtual twin génératif
4. **SUP 3** (25s) - Scénarios alternatifs et exemple fournisseur A&D
5. **SUP 4** (20s) - Solution en minutes avec le virtual twin génératif
6. **SUP Content** (manuel) - "- even in an unstable world." - Nécessite clic sur "Finish"

**Durée totale automatique**: ~86 secondes

## Objets 3D de la Supply Chain

La présentation contrôle la visibilité des objets suivants via le SDK:
- **Supply Chain Sound** - Son d'ambiance (activé au démarrage)
- **AS IS Supply Chain** - Visible au début, caché à la fin
- **SUP 1, SUP 2, SUP 3, SUP 4** - Composants progressifs
- **SUP Content** - Vue finale complète

## Comportement

1. **Avant le démarrage**:
   - Écran d'intro avec bouton "Start Presentation"
   - Tous les objets SUP sont cachés
   - AS IS Supply Chain est visible

2. **Pendant la présentation**:
   - Le bouton disparaît
   - Les slides défilent automatiquement
   - Chaque objet 3D s'ajoute progressivement
   - Les objets précédents restent visibles

3. **Dernière slide**:
   - Le bouton "Finish" réapparaît
   - L'utilisateur peut terminer manuellement

4. **Écran de fin**:
   - "Thank you - Presentation Complete"
   - Bouton "Restart Presentation" pour recommencer

## Différences avec les autres versions

- **supply-chain-presentation**: Version manuelle - l'utilisateur clique pour avancer
- **supply-chain-presentation-collab**: Version collaborative avec Supabase sync
- **supply-chain-presentation-auto**: Défilement automatique (cette version)

## Utilisation

Intégrer dans un iframe du SDK Creative Experience:

```html
<iframe src="supply-chain-presentation-auto/index.html"></iframe>
```

Les objets 3D doivent être nommés dans le SDK:
- Supply Chain Sound
- AS IS Supply Chain
- SUP 1, SUP 2, SUP 3, SUP 4
- SUP Content

## Personnalisation des timings

Pour ajuster les durées, modifier le tableau `slides` dans [app.js](app.js):

```javascript
{
    text: "Votre texte...",
    media: "SUP 1",
    duration: 15000 // Durée en millisecondes (15s)
}
```

Pour la dernière slide, mettre `duration: 0` pour arrêter l'auto-progression.

## Messages clés

### Objectif de la Supply Chain
- Anticiper, préparer et sécuriser les flux physiques
- Augmenter la marge et le fulfillment
- Minimiser l'impact CO2

### Virtual Twin Génératif
- Génération automatique de scénarios optimisés
- Simulation de Plans B, C, D
- Recalcul des risques, coûts et délais
- Intégration continue des disruptions du monde réel

### Exemple concret
- Fournisseur A&D arrête collaboration en 2 mois
- Solution trouvée en minutes (vs semaines)
- Nouveau scénario de sourcing généré automatiquement
- Meilleur compromis coût-risque proposé
