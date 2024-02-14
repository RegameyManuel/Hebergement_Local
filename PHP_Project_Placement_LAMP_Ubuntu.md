
# Placement d'un projet PHP avec LAMP sur Ubuntu

Après avoir installé LAMP (Linux, Apache, MySQL, PHP) sur votre système Ubuntu, vous devez placer vos projets PHP dans le répertoire racine web d'Apache pour qu'ils soient accessibles en ligne. Voici où et comment le faire :

## Répertoire Racine Web d'Apache

Le répertoire par défaut pour Apache sur Ubuntu est :

```
/var/www/html
```

## Étapes pour Placer Votre Projet PHP

1. **Ouvrir un terminal** : Utilisez Ctrl+Alt+T pour ouvrir un terminal sur Ubuntu.

2. **Accéder au répertoire racine web d'Apache** :
   ```bash
   cd /var/www/html
   ```

3. **Copier votre projet dans ce répertoire** : Utilisez la commande `cp` pour copier votre projet. Par exemple :
   ```bash
   sudo cp -r ~/monprojet /var/www/html/
   ```

4. **Modifier les permissions** : Ajustez les permissions pour que Apache puisse lire (et écrire si nécessaire) les fichiers de votre projet.
   ```bash
   sudo chown -R www-data:www-data /var/www/html/monprojet
   ```

5. **Accéder à votre projet via un navigateur** : Tapez `http://localhost/monprojet` dans la barre d'adresse de votre navigateur.

## Vérification et Démarrage d'Apache

- Vérifiez l'état d'Apache :
  ```bash
  sudo systemctl status apache2
  ```
- Si Apache n'est pas en cours d'exécution, démarrez-le avec :
  ```bash
  sudo systemctl start apache2
  ```

Ces instructions vous aideront à mettre en ligne votre projet PHP sur un système Ubuntu avec LAMP installé.
