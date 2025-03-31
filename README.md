# Introduction

Pour pouvoir créer une documentation en **Markdown** puis la convertir en **PDF professionnel**, cette solution présente plusieurs avantages. Le Markdown est un langage simple, lisible et esthétique, qui permet de produire rapidement des documents structurés. C’est un outil pertinent à maîtriser, que ce soit dans le cadre d’études en informatique ou pour des projets personnels.

# Prérequis

Avant de commencer, il est nécessaire d’**installer Pandoc**, compatible avec votre système d’exploitation.

# Commande

Pour convertir vos fichiers (par exemple, une page de garde suivie du contenu principal de votre documentation), utilisez la commande suivante :

```
pandoc "Page de garde.md" "Documentation.md" -o Document.pdf -V lang=fr --pdf-engine=xelatex
```
# Explication de la commande

"Page de garde.md" et "Documentation.md" : Ce sont les fichiers Markdown sources, dans l’ordre dans lequel ils seront fusionnés. Le premier sert généralement de page de couverture, suivi du contenu principal.

`-o Document.pdf ` : Spécifie le fichier de sortie. Ici, le document final généré sera Document.pdf.

`-V lang=fr ` : Définit la langue du document à "fr" (français). Cela influence certains aspects du rendu, comme la césure, la typographie et les métadonnées du PDF.

`--pdf-engine=xelatex ` : Indique à Pandoc d’utiliser XeLaTeX comme moteur de rendu PDF. Ce moteur est recommandé pour une meilleure gestion des polices, des caractères spéciaux, et pour une compatibilité accrue avec les langues non-anglaises.

# Exemple de modification supplémentaire
Si vous souhaitez ajouter une page de fin (par exemple des remerciements), il vous suffit de créer un fichier Markdown dédié, puis de l’ajouter à la commande comme suit : 
`pandoc "Page de garde.md" "Documentation.md" "Remerciements.md" -o Document.pdf -V lang=fr --pdf-engine=xelatex`

