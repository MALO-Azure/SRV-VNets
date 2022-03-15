# Déploiement

Ce répertoire contient plusieurs fichiers qui permettront de déployer une machine virtuelle de type Debian avec des paramètres spécifiques :
* Le fichier `VNet.json` = Il est le fichier principal sous format JSON où se trouvent toutes les informations de la future ressource (à savoir la plage d'adresse, le masque, les sous-réseaux...).
* Le fichier `network-deployment.yml` = Qui est le fichier de déploiement de la ressource sur Azure.

Pour déployer la ressource, il vous suffit d'apporter une modification au fichier principal `network-deployment.yml`, situé dans le dossier `.github/workflow`, pour déclencher le workflow et créer la ressource sur Azure. Le déclencheur est mis sur `delete` pour éviter de déployer la ressource à chaque modification. Il suffit de moidifier ce déclencheur et de le mettre sur push pour déployer la ressource.
