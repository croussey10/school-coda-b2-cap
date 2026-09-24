# Inventaire des points d'entrée

Le livrable de l'atelier d'analyse. Il dit ce que l'API devra **permettre** — pas comment on
l'écrira.

Une règle : tout ce qui figure ici doit se justifier par la lettre de mission ou par un écran
des maquettes. Si vous ne savez plus d'où vient une ligne, c'est peut-être qu'elle n'en vient
pas. (Seule exception : la section bonus, si vous en ajoutez une.)

---

## Ce que l'utilisateur peut faire

Une action par ligne, en français. Pas encore de chemins.

Accueil :
- Chercher un trajet d'une ville A à une ville B avec la date et le nombre de voyageurs

Résultats :
- Modifier un/des éléments de la recherche du trajet
- Voir les trajets avec l'heure, la ville de départ / de déstination, le temps du trajet, le prix par place
- Cliquer sur un résultat -> "Détail"

Détail :
- Voir le détail du trajets avec l'heure, la ville de départ / de déstination, le temps du trajet, le prix total, la
  franchise de masse, le modele de la catapulte, les consignes d'embarquement
- Modifier le nombre de voyageurs
- Cliquer sur le bouton "Réserver" -> "Connexion"

Connexion :
- Voir le détail du trajets avec l'heure, la ville de départ / de déstination, la date, le prix total
- Se connecter avec mail/mdp
- Cliquer sur le bouton "Se connecter" -> "Panier"
- Cliquer sur le bouton "S'inscrire" -> "Inscription"

Inscription :
- Créer un compte avec les champs suivant : OBLIGATOIRE : email, mdp. FACULTATIF : prénom, nom

Panier :
- Voir une LISTE des trajets mis dans le panier avec leur détail (ville A / B, date, heure de départ, nb de places, prix total, BOUTON DELETE)
- Supprimer un trajet mis dans le panier
- Cliquer sur le bouton "Chercher un autre lancer" -> "Acceuil"
- Cliquer sur le bouton "Payer" -> "Paiement"

Paiement :
- Voir une LISTE des trajets mis dans le panier avec leur détail (ville A / B, date, heure de départ, nb de places, prix total)
- Choisir un moyen de paiement (CB / Bon de transport)
- Cliquer sur le bouton "Payer {{Prix total}} €" -> "Confirmation"

Confirmation :
- Voir un récap du paiement (prix totale, moyen de paiement, nb de billets, date d'achat)
- Voir une LISTE de chacun des billets avec détails (ID unique du billet, date d'achat, détail du trajets (ville A / B, date, heure de départ, prix unité))
- Cliquer sur le bouton "Voir mes billets" -> "Mes billets"
- Cliquer sur le bouton "Retour à l'acceuil" -> "Acceuil"

Mes billets :
- Voir une LISTE de chacun des billets avec détails (ID unique du billet, date d'achat, détail du trajets (ville A / B, date, heure de départ, prix unité))

Dossier :
- Voir son compte (email, prenom, nom, date de création)

## Les points d'entrée

| Ce que ça fait | Chemin proposé | Qui peut l'appeler |
|----------------|----------------|--------------------|
|Liste les villes |GET /cities|TOUT LE MONDE|
|Liste les trajets |POST /trajets |TOUT LE MONDE|
|Détail d'un trajet|GET /trajets/id|TOUT LE MONDE|
|Retirer un trajet|DELETE /trajets/id|TOUT LE MONDE|
|Ajouter un trajet au panier|POST /trajets/id|TOUT LE MONDE|
|Créer un compte|POST /users|TOUT LE MONDE|
|Liste des billets|GET /billets/me|TOUT LE MONDE|
|Faire un payements|POST /orders|CONNECTER|


## Les données qui circulent

Pour chaque point d'entrée : ce qu'il reçoit, ce qu'il renvoie. Nommez les données comme
l'Office les nomme — les traduire en identifiants techniques, c'est le travail de demain.

### Liste les villes
Renvoi la liste des villes

###

## Ce dont on n'est pas sûrs

Les questions que la lettre et les maquettes ne tranchent pas. Une question notée vaut mieux
qu'une réponse inventée.

-
