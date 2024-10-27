# Création d'une infra réseau avec ansible
Lobjectif est de reproduire à partir de l'outil ansible et en quelques minutes l'ensemble de l'infrastructure réseau complet qui m'a été demandée de configurez et de managée durant mon premier stage en Août 2024. Pour dévé

## présentation du projet
Ce projet se présente comme une infrastructure simple avec un serveur web, un autre pour apache pour le moment 

## Prérequis
Tout d'abord pour que cela fonctionne il faudrait configurer les machines qui le composerons. L'installation de la dernière version d'ansible sur toutes les machines (il sera parfois nécésaire d'installer un interpréteur python pour les machines clientes puissent comprendre les commandes ansible). 
- En utilisant le node manager ( machine pricipale qui superviseras toutes les autres et qui seras la seul utilisait ) on vas assurer la connection ssh entre lui et les autres machine de production sans cette connection ssh la communication entre les machines est impossible;
- Avec cette même machine en se connecteras en tant qu'admin pour créer le fichier d'inventaire ( qui recense l'emsemble de nos machines de production ) et également les informations nécécaires pour que votre node manager puisse communiquer avec ces machines ( clé ssh, nom de l'utilisateur login de la machines cliente généralement l'admin, et le mot de passe de celui-ci;
- Pour la suite je conseillerais de lancer la commande "ansible -i <nom du fichier d'inventaire> -m ping all" pour vérifier qu'il peut communiquer avec les machines.
