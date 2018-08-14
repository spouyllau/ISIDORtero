# ISIDORtero
## Expansion de recherche ISIDORE pour Zotero

Le fichier engines.json permet d'ajouter des moteurs de recherche à Zotero afin de rechercher en ligne un document référencé dans sa bibliothèque Zotero. Il est également possible d'étendre la recherche à partir des auteurs, des mots clés du document référencé dans différents moteur de recherche. Dans ce cadre, nous proposons ici le code permettant d'utiliser ISIDORE depuis Zotero.

### Fonctions

L'ajout d'ISIDORE à Zotero permet :

- Mode "global search" permet de rechercher le document dans ISIDORE à partir des mots du titre.
- Mode "first author" permet de rechercher dans ISIDORE sur le premier auteur d'un document.

### Installation :

Fermez votre Zotero, Ouvrir le fichier <Zotero>/locate/engines.json (ex. sous Mac : Users/utilisateur/Zotero/locate) dans un éditeur de texte (Atom, TextEdit, etc.) et ajoutez juste après le premier [ le code json suivant :

`{
  "name": "ISIDORE - global search",
  "alias": "ISIDORE",
  "icon": "https://www.rechercheisidore.fr/favicon.ico",
  "_urlTemplate": "https://www.rechercheisidore.fr/search/?q={z:title}",
  "description": "ISIDORE is an academic search engine for arts and humanities.",
  "hidden": false,
  "_urlParams": [],
  "_urlNamespaces": {
    "rft": "info:ofi/fmt:kev:mtx:journal",
    "z": "http://www.zotero.org/namespaces/openSearch#",
    "": "http://a9.com/-/spec/opensearch/1.1/"
  },
  "_iconSourceURI": "https://www.rechercheisidore.fr/favicon.ico"
},
{
  "name": "ISIDORE - first author",
  "alias": "ISIDORE",
  "icon": "https://www.rechercheisidore.fr/favicon.ico",
  "_urlTemplate": "https://www.rechercheisidore.fr/search/?creator={rft:aulast?}+{rft:aufirst?}",
  "description": "ISIDORE is an academic search engine for arts and humanities.",
  "hidden": false,
  "_urlParams": [],
  "_urlNamespaces": {
    "rft": "info:ofi/fmt:kev:mtx:journal",
    "z": "http://www.zotero.org/namespaces/openSearch#",
    "": "http://a9.com/-/spec/opensearch/1.1/"
  },
  "_iconSourceURI": "https://www.rechercheisidore.fr/favicon.ico"
},`

## Crédits

Auteur : Stéphane Pouyllau -
Remerciements : Laurent Capelli, Adrien Desseigne, Elifsu Sabuncu, Brenton M. Wiernik.
