# Verification realisee

Le 2 novembre 2026, sous Linux avec PowerShell 7.4.6 officiel (archive verifiee avec le fichier SHA-256 de la meme publication) : **28 tests reussis, 0 echec**.

Commande : `pwsh -NoProfile -File tests/Test-Repair58TM1.ps1`.

Les tests couvrent les plans sans purge par defaut, les options independantes, le ciblage des processus par session, l'arret avant mutation en cas de strategie bloquante ou manifeste absent, un vrai appel `-WhatIf`, l'ordre sauvegarde/renommage, le refus des liens/jonctions, les perimetres et identites de manifeste, le contenu autorise des sauvegardes `.reg`, les restrictions SCA et une restauration de cache sur des fichiers de test avec preservation du cache regenere.

Les commandes Windows sont simulees dans ces tests. Aucun test fonctionnel Office, RDS, AppX, ACL NTFS, tache planifiee, conteneur FSLogix ou MFA n'a ete execute. L'interface Windows Forms n'a pas ete affichee sur Linux ; sa syntaxe est analysee. La procedure de validation Windows reste dans `VALIDATION.md`.
