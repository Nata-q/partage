
1. `New-item -path C:\ -name Documents_Entreprise -itemtype Directory` pour créer le dossier à la racine.
2. Tapper dans powershell :
	- `new-item -path C:\Documents_Entreprise -name RH -itemtype Directory`(crée le dossier Rh).
	- `new-item -path C:\Documents_Entreprise -name Direction -itemtype Directory`(crée le dossier Direction).
	- `new-item -path C:\Documents_Entreprise -name Comptabilité -itemtype Directory`(crée le dossier Comptabilité).
3. Pour créer les groupes dans l'AD on tappe : `Get-ADgroup -identity "Direction"`
`Get-ADgroup -identity "Comptabilité"`
`Get-ADgroup -identity "RH"`
4. Ouvrir le gestionnaire de serveur, pis cliquer sur "Services de fichiers et de stockage" > "Partages".
5. Clique droit sur nouveau partage ->Partage SMB-Rapide->choisir le dossier Documents_Entreprise ->Nommer le partage ==Docs== ->Configurer ensuite les permissions NTFS comme ceci:
	- ajouter le groupe Direction et cocher lecture et écriture.
	- ajouter le groupe Comptabilité et cocher lecture et écriture.
	- ajouter le groupe RH et cocher lecture et écriture.
6. pour chaque dossier RH, Direction et Comptabilité, clique droit, propriété. Puis ensuite dans l'onglet partage, selectionner partage et ajouter le groupe correspondant au dossier en vérifiant bien que lecture et écriture soit seulement cochés.

