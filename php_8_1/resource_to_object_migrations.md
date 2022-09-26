# Resource to object migrations

Dans la continuité des évolutions de php certaines ressources sont converties en objet spécifique

## Fileinfo

Les fonctions telles que finfo_file et finfo_open qui acceptaient et retournaient une ressource utilise maintenant un objet finfo

## Imap

Les fonctions telles que imap_body et imap_open qui acceptaient et retournaient une ressource utilise maintenant un objet IMAPConnection
