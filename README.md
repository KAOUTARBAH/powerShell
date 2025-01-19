# powerShell
Manipuler les fichiers et dossiers
Copier le code ci-dessous dans la fenêtre script de PowerShell ISE et l'executer (F5) :
Set-Location -Path C:\
#Une écriture possible pour la création d'un dossier
New-Item -ItemType Directory -Path C:\ -Name FolderTest1
#Une autre écriture possible pour la création d'un dossier
New-Item -ItemType Directory -Path C:\FolderTest2
#Création de fichier vide dans le dossier c:\FolderTest
New-Item -ItemType File -Path C:\FolderTest1 -Name File1
New-Item -ItemType File -Path C:\FolderTest1 -Name File2
New-Item -ItemType File -Path C:\FolderTest1 -Name File3
New-Item -ItemType File -Path C:\FolderTest1 -Name File4
New-Item -ItemType File -Path C:\FolderTest1 -Name File5
#Création de fichier vide dans le dossier c:\FolderTest2
$Count = 6
Do
{
    New-Item -ItemType File -Path C:\FolderTest2 -Name "File$Count"
    $Count++
}
While ($Count -lt 11)
Ce code va créer des dossiers et des fichiers:

Les fichiers File1 à File5 sont dans le dossier C:\FolderTest1
Les fichiers File6 à File10 sont dans le dossier C:\FolderTest2
Ta tâche est la suivante:

Mettre les fichiers avec un numéro pair dans un dossier c:\EvenFolder
Mettre les fichiers avec un numéro impair dans un dossier c:\OddFolder
🤓 Pour rappel:

Copy-Item copie un fichier ou un dossier d'un emplacement à un autre
Move-Item déplace un fichier ou un dossier d'un emplacement à un autre
Remove-Item Supprime un fichier ou un dossier
New-Item crée un dossier ou un fichier
Get-ChildItem liste le contenu d'un dossier
Une fois la tâche réalisée pour partager ton résultat :

Récupère l'historique des commandes que tu as tapées avec Get-History > historique.txt
Récupère le contenu des dossiers avec Get-ChildItem -Path *Folder* -Recurse > listing.txt
Partage ces fichiers via une URL, par exemple via un gist, un dépôt github
🧐 Critères d'acceptation
Il devra y avoir 2 fichiers avec les informations suivantes:

Un fichier avec les différentes lignes de commandes
Un fichier avec le contenu de chacun des 2 dossiers EvenFolder et OddFolder, les dossiers FolderTest1 et FolderTest2 n'apparaissant pas parce qu'ils sont vides.
