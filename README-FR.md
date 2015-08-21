# Explications en français dans le texte

Pour le télécharger, un click-droit sur RAW et le sauvegarder.

Ce fichier permet de valider/d'aider à valider de très nombreux points de checklists qualité : performance, mise en cache, sécurité, noms de domaine avec ou sans www, redirections, etc.

## UTF-8 encoding

Définit l’UTF-8 par défaut sur certains fichiers.

## Password protection

Utile pour restreindre un site en développement.

On pourra ajouter ``` Allow From <your_ip> ``` pour autoriser une IP sur un développement.

Voir http://openweb.eu.org/articles/le-fichier-htaccess pour générer les mots de passe (htpasswd).

## Additionnal charset/types/etc.

Définit ou re-définit bon nombre de types MIME, par exemple très utile pour faire marcher les web fonts comme il faut.

## force download

Si l’on souhaite forcer le téléchargement d’un type de fichier, ajouter la bonne extension.

## for uploadify or upload component

Parfois nécessaire pour uploadify.

## Custom error messages / pages

Obligatoire pour les pages d’erreurs 404/403. 

## File access

Empêche le listing des racines des répertoires.

## prevent accessing to all files excepted those mentionned

Très utile dans un folder de type upload : restreint l’exécution des fichiers non-autorisés.
Ex: si le folder est censé avoir uniquement des jpg, on spécifiera :
<FilesMatch "(?<!\.JPG|\.jpg|\.JPEG|\.jpeg)$">

## prevent executing PHP file in a folder

Utile dans certains répertoire de type upload, pour empêcher un script de se lancer. 
Ne JAMAIS activer ça sur un htaccess global d’un site !

## block access to hidden files & directories

Empêche l’accès aux fichiers cachés du serveur (normalement par défaut, mais on ne sait jamais).

## Suppressing / Forcing the `www.` at the beginning of URLs

Pour ajouter/enlever le www. sur un site. Plusieurs exemples de redirections sont proposées.
Ne JAMAIS utiliser plus d’une option, sinon redirection infinie.

## Compression 

Active la compression sur les fichiers usuels. Obligatoire pour les performances web.

## Security 

Ajoute les entêtes de sécurité (éviter le MIME-Sniffing et les attaques de type ClickJacking et active certaines protections des navigateurs contre le Cross-Site-Scripting). Cf https://securityheaders.io/ 

## Cache

Mise en cache des éléments statiques. Obligatoires pour les performances.

## Redirects

Sections pour les redirections permanentes/temporaires, propose d’autres exemples.
