# publik-org-templates

Contient des modèles de collectivités pour https://github.com/Vayel/publik-docker.

Chaque modèle est un dossier pouvant comporter les fichiers suivants :

## `hobo-recipe.json.template`

Se référer à l'exemple à la racine de ce dépôt. Si ce fichier n'est pas présent
dans le dossier du modèle, celui à la racine est utilisé.

## `wcs-env.sh.template`

Se référer à l'exemple à la racine de ce dépôt. Si ce fichier n'est pas présent
dans le dossier du modèle, celui à la racine est utilisé.

## `user-portal.json.template`

Le portail citoyens exporté au format JSON (`https://citoyens.XXX/manage/site-export`).
Ce fichier peut être édité pour y ajouter les variables d'environnement suivantes,
qui seront substituées lors de la création de la collectivité :

* `${SLUG}`
* `${TITLE}`


## `agent-portal.json.template`

Le portail agents exporté au format JSON (`https://agents.XXX/manage/site-export`).
Ce fichier peut être édité pour y ajouter les variables d'environnement suivantes,
qui seront substituées lors de la création de la collectivité :

* `${SLUG}`
* `${TITLE}`

Par exemple, si vous ajoutez la liste des démarches à traiter, le JSON obtenu contiendra
une ligne du type `"wcs_site": "wcs-<SLUG_COLLECTIVITE>",`. En rem^plaçant cette ligne
par `"wcs_site": "wcs-${SLUG}",`, elle comportera bien le slug de la collectivité
nouvellement créée et non pas celui présent lors de l'export.

## `forms.zip`

Les formulaires exportés depuis `https://demarches.XXX/backoffice/settings/export`.

## `categories.zip`

Les catégories exportées depuis `https://demarches.XXX/backoffice/settings/export`.
