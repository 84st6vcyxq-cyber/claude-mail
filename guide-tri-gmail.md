# Guide : trier tout l'historique Gmail en quelques clics

Les libellés existent déjà : **Banque & Finances**, **Administratif**, **Achats & Factures**,
**Emploi**, **Sécurité & Codes**, **Promos**, **Réseaux sociaux**, **Newsletters**.

## Méthode (sur ordinateur, sur mail.google.com)

1. Copie une recherche ci-dessous dans la barre de recherche Gmail, puis appuie sur Entrée.
2. Coche la case « Tout sélectionner » en haut de la liste.
3. Clique sur le lien bleu **« Sélectionner toutes les conversations correspondant à cette recherche »**.
4. Clique sur l'icône **Déplacer vers** (le dossier avec une flèche) et choisis le libellé.
   Cette action ajoute le libellé et sort les mails de la boîte de réception en une seule fois.
   Pour les catégories marquées « garder », utilise plutôt l'icône **Libellés**.
5. Confirme. Gmail peut mettre quelques minutes s'il y a des milliers de mails.

Rien n'est supprimé : tout reste accessible via le libellé ou « Tous les messages ».

## Recherches à coller (dans cet ordre)

### 1. Banque & Finances (libellé, garder dans la boîte)
```
in:inbox (from:creditmutuel.fr OR from:boursobank.com OR from:revolut.com OR from:paypal.com OR from:paypal.fr OR from:binance.com OR from:bitstack-app.com OR from:lydia-app.com OR from:sumeria.eu OR from:coinbase.com)
```

### 2. Administratif (libellé, garder dans la boîte)
```
in:inbox (from:gouv.fr OR from:gov.au OR from:ameli.fr OR from:caf.fr OR from:francetravail.fr OR from:urssaf.fr OR from:service-public.fr)
```

### 3. Achats & Factures (libellé, garder dans la boîte)
```
in:inbox (subject:(facture OR reçu OR receipt OR commande OR livraison OR expédié) -category:promotions)
```

### 4. Sécurité & Codes (Déplacer vers, donc archiver)
```
in:inbox older_than:2d (subject:("Ne pas partager" OR "code de vérification" OR "verification code" OR "alerte de sécurité" OR "security alert" OR "nouvelle connexion" OR "new login") OR from:accounts.google.com)
```

### 5. Emploi (Déplacer vers)
```
in:inbox (from:jobalerts-noreply@linkedin.com OR from:indeed.com OR from:welcometothejungle.com OR from:hellowork.com OR subject:(recrute OR recrutent))
```

### 6. Réseaux sociaux (Déplacer vers)
```
in:inbox (category:social OR from:facebookmail.com OR from:linkedin.com OR from:tiktok.com OR from:instagram.com OR from:twitter.com OR from:x.com OR from:pinterest.com OR from:youtube.com OR from:discord.com)
```

### 7. Promos (Déplacer vers) : c'est le plus gros morceau
```
in:inbox category:promotions
```
puis
```
in:inbox (from:harmonievie.com OR from:fossil.com OR from:thebradery.com OR from:sensiseeds.com OR from:lepetitfumeur.fr OR from:jackery.com OR from:divainparfums.com OR from:cyberghostvpn.com OR from:ef.com OR from:scufgaming.com OR from:bulk.com OR from:uber@uber.com OR from:email.openai.com)
```

### 8. Newsletters (Déplacer vers)
```
in:inbox (unsubscribe OR désinscrire OR désabonner) -label:"Banque & Finances" -label:administratif -label:"Achats & Factures"
```

### 9. Le vieux reste (facultatif, mais c'est le plus efficace)
Une fois les étapes 1 à 8 faites, il reste surtout de vieux mails sans intérêt.
Pour les archiver d'un coup sans rien perdre :
```
in:inbox older_than:6m -is:starred -label:"Banque & Finances" -label:administratif -label:"Achats & Factures"
```
→ Coche tout, sélectionne toutes les conversations, puis clique sur **Archiver**.

### 10. Tout marquer comme lu (facultatif)
```
in:inbox is:unread older_than:1m
```
→ Coche tout, sélectionne toutes les conversations, puis clique sur **Marquer comme lu**.

## Pour que ça reste rangé : créer des filtres

Pour les recherches 4 à 8 : clique sur l'icône de réglages à droite de la barre de recherche,
puis **Créer un filtre**. Coche **Ignorer la boîte de réception**, **Appliquer le libellé** et
**Appliquer également le filtre aux conversations correspondantes**.
Les prochains mails de ce type seront alors classés automatiquement.

Conseil : désabonne-toi des listes les plus envahissantes (Vie & Harmonie envoie environ 5 mails par jour).
Gmail affiche un bouton « Se désabonner » en haut de ces mails.
