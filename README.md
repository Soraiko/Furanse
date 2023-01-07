Ce projet consiste à compiler un DLL qui vous permet d'utiliser l'IME japonais de Windows avec la disposition d'un clavier français.
Laissez tomber la fameuse solution d'éditer le registre en remplaçant la valeur "KBDJPN.DLL" par "KBDFR.DLL".
Ma solution conserve la mention "KBDJPN.DLL" et utilise une version modifiée de ce DLL du clavier japonais.
J'utilise pour ce faire un outil officiel de Windows "Microsoft Keyboard Layout Creator (MSKLC)" disponible au téléchargement ci-dessous:
https://www.microsoft.com/en-us/download/details.aspx?id=102134
(Source de mon code disponible pour les sceptiques qui pensent que je vais hacker leur clavier pour dominer le monde)

Pour **COMPILER** mon script (Furanse.klc)
	-Téléchargez l'outil mentionné ci-avant
	-Séléctionnez "File > Load Source File..."
	-Compilez le fichier (cela créera un dossier avec des binaires d'installation, seul le DLL se trouvant dans le dossier amd64 nous intéressera.)
	
Rennomez ce binaire en "KBDJPN.DLL", puis rendez-vous dans le dossier %System32%, faites un backup de votre KDBJPN.DLL et remplacez le par celui-ci.
Pour que le remplacement soit possible, il vous faudra remplacer le propriétaire et les autorisations d'accès au fichier (Propriétés | Sécurité).
Un redémarrage sera necessaire.

Pour INSTALLER DIRECTEMENT (**SANS COMPILER**) le DLL (Disponible en téléchargement sur ce GIT) sautez les 3 étapes de la section explicative précédente et remplacez directement le DLL.
Si vous utilisiez auparavent la fameuse méthode d'édition du registre, n'oubliez pas de restaurer la valeur de "KBDFR.DLL" vers "KBDJPN.DLL" et de redémarrer l'ordinateur.

Grâce à mon nouveau DLL, le raccourcis Alt+Tilde (Tilde étant à l'emplacement du symbole ² sur les clavier français) est à nouveau fonctionnnel pour passer en more Hiragana.
De plus vous pourrez continuer à utiliser le clavier japonais pour écrire en français, tous les accents et combinaisons de touches françaises y sont disponibles.
Un seul bémol: lorsqu' utilisé sur l'exploreur de Windows, il semble se remettre en mode qwerty,(Cela n'arrive pas sur la plupart des autres applications)
Mais cela en vaut quand même la peine car le vrai gros problème était l'impossibilité d'utiliser le raccourcis Alt+Tilde pour passer ne mode Hiragana sans avoir à cliquer à chaque fois sur le "A" en bas de l'écran.
Vous pouvez continuer à revenir en clavier français avec le raccourcis Alt+Shift.
Disons que cela réduira quand même votre frustration pour la plupart des application où vous aurez écrit en oubliant de remettre le clavier en français.