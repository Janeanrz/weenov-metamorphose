# Weenov — page Métamorphose

Page publique statique présentant le travail de transformation de marque réalisé autour de Weenov.

> **Dépôt actuellement public.** Tout son historique et tous les fichiers suivis peuvent être consultés par n’importe qui. Aucun secret, document client confidentiel, donnée RH, fichier contractuel ou source privée ne doit y être ajouté.

## État vérifié au 22 juillet 2026

- Dépôt : `Janeanrz/weenov-metamorphose`
- Visibilité GitHub : publique
- Branche publiée : `main`
- Technologie : page HTML/CSS/JavaScript statique
- Build : aucun build applicatif requis
- Hébergement configuré : GitHub Pages
- Déploiement : automatique à chaque push sur `main`
- Domaine déclaré dans `CNAME` : `weenov.annarozdesign.com`
- Titre HTML : `Métamorphose Weenov`

Le domaine et le workflow sont présents dans le dépôt. Leur état live doit être vérifié dans GitHub Pages et dans un navigateur avant toute annonce publique.

## Finalité

Cette page est une vitrine narrative. Elle doit montrer une transformation de marque validée, sans devenir :

- le site opérationnel de Weenov ;
- le dépôt de l’application Weenov RH ;
- un espace de stockage de documents internes ;
- une source de vérité pour les données ou processus RH ;
- un endroit où conserver des secrets ou accès de déploiement.

Le code applicatif Weenov RH vit dans le dépôt privé `Janeanrz/weenov-rh-app`.

## Structure

```text
weenov-metamorphose/
├── index.html                  # page complète
├── CNAME                        # sous-domaine GitHub Pages
├── .github/workflows/pages.yml  # publication automatique
└── README.md
```

La page principale contient une partie importante de ses styles et ressources directement dans `index.html`. Toute modification doit donc être relue avec attention : un changement local peut affecter l’ensemble de la page.

## Prévisualisation locale

Aucune installation Node n’est requise.

```bash
python -m http.server 8080
```

Sous Windows :

```powershell
py -m http.server 8080
```

Puis ouvrir `http://localhost:8080`.

## Déploiement GitHub Pages

Le workflow `.github/workflows/pages.yml` :

1. se déclenche sur `main` ou manuellement ;
2. publie la racine du dépôt ;
3. utilise l’environnement `github-pages` ;
4. annule un ancien déploiement si un plus récent démarre.

### Procédure sûre

1. créer une branche ;
2. contrôler la page en local ;
3. ouvrir une pull request ;
4. vérifier le diff complet de `index.html` ;
5. confirmer qu’aucune information privée n’est ajoutée ;
6. fusionner dans `main` ;
7. suivre l’Action GitHub Pages ;
8. vérifier le domaine, HTTPS, les liens et l’affichage mobile ;
9. revenir au commit précédent en cas de problème.

## Contrôles avant publication

- identité Weenov exacte et validée ;
- logo et visuels autorisés ;
- tarifs, dates et affirmations à jour ;
- aucune donnée RH ou information client ;
- aucun lien Claude, fichier temporaire ou ressource locale ;
- liens externes fonctionnels ;
- lisibilité mobile et ordinateur ;
- navigation clavier ;
- réduction des animations respectée lorsque prévue ;
- poids de page acceptable malgré les ressources intégrées.

## Domaine

Le fichier `CNAME` déclare :

```text
weenov.annarozdesign.com
```

Avant toute modification DNS :

- identifier la cible actuelle ;
- vérifier le dernier workflow Pages ;
- préparer un retour arrière ;
- confirmer que le sous-domaine ne sert pas un autre projet ;
- vérifier le certificat HTTPS après changement.

## Confidentialité et propriété

Cette page concerne un projet externe à ANNAROZ. La publication doit respecter :

- l’autorisation d’usage de l’identité Weenov ;
- les droits sur les logos, images et textes ;
- la séparation entre portfolio public et informations internes ;
- la confidentialité des échanges, contrats et données RH.

La visibilité publique du dépôt doit rester une décision consciente. Un dépôt public n’est pas adapté à des sources de marque non publiées, des exports clients ou des fichiers de production confidentiels.

## Reprise depuis le portable

1. Installer Git et GitHub CLI.
2. Cloner le dépôt.
3. Lancer un serveur local.
4. Créer une branche avant modification.
5. contrôler la page sur mobile et ordinateur ;
6. fusionner par pull request ;
7. vérifier GitHub Pages et le sous-domaine.

Aucun accès au PC fixe n’est nécessaire pour maintenir cette page.

## Gouvernance

Les décisions transversales ANNAROZ et la méthode de publication sont versionnées dans le dépôt privé `Janeanrz/annaroz-foundation`. Les décisions propres à Weenov doivent rester identifiables et séparées des données internes ANNAROZ.
