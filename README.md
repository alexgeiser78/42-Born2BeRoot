# 42-Born2BeRoot

La machine virtuelle:

Une machine virtuelle est un environnement qui fonctionne comme un système informatique virtuel, avec son propre processeur, sa mémoire, son interface réseau et son espace de stockage, mais qui est créé sur un système matériel physique (situé sur site ou hors site). L’hyperviseur est le logiciel qui permet de séparer les ressources de la machine du matériel et de les approvisionner de manière adéquate pour que la machine virtuelle puisse les utiliser. 
Les machines physiques, équipées d'un hyperviseur tel que KVM (Kernel-based Virtual Machine), sont appelées machines hôtes, ordinateurs hôtes, systèmes d'exploitation hôtes ou simplement hôtes.Les nombreuses machines virtuelles qui utilisent les ressources sont des machines invitées, des ordinateurs invités, des systèmes d'exploitation invités ou plus simplement des invités. L'hyperviseur traite les ressources de calcul (processeur, mémoire, stockage) à la manière d'un pool de ressources qui peut être déplacé sans difficulté entre les invités existants ou vers de nouvelles machines virtuelles.
Les machines virtuelles permettent d'exécuter simultanément plusieurs systèmes d'exploitation sur un seul ordinateur, comme une distribution Linux® sur un ordinateur portable sous MacOS. Chacun des systèmes d'exploitation s'exécute sur le matériel hôte comme le ferait n'importe quel autre système d'exploitation ou application. L'expérience de l'utilisateur final émulée au sein de la machine virtuelle est donc quasiment identique à celle offerte par un système d'exploitation exécuté en temps réel sur une machine physique.  
L'usage de machines virtuelles est l'un des principes fondamentaux de la technologie Java. 

Fonctionnement d'une machine virtuelle:

La technologie de virtualisation vous permet de partager un système avec de nombreux environnements virtuels. L'hyperviseur gère le matériel et sépare les ressources physiques des environnements virtuels. Ces ressources sont partitionnées selon les besoins à partir de l'environnement physique et distribuées aux machines virtuelles.
Lors de l'exécution d'une machine virtuelle, si un utilisateur ou un programme lance une instruction qui sollicite des ressources supplémentaires de la part de l'environnement physique, l'hyperviseur planifie la demande auprès des ressources du système physique afin que le système d'exploitation et les applications de la machine virtuelle puissent accéder au pool partagé de ressources physiques.

Types d'hyperviseurs:

Il existe deux types d'hyperviseurs qui peuvent être utilisés pour virtualiser des ressources.

Type 1

Un hyperviseur de type 1 s'installe sur un système bare metal. L'hyperviseur planifie directement les ressources des machines virtuelles sur le matériel.La solution KVM est un hyperviseur de type 1. Elle a été intégrée au noyau Linux en 2007. Si vous utilisez une version récente de Linux, vous bénéficiez donc déjà d'un accès à KVM. 

Type 2

Un hyperviseur de type 2 est hébergé. Les ressources des machines virtuelles sont planifiées au niveau d'un système d'exploitation hôte, lui-même exécuté sur le matériel. VMware Workstation et Oracle VirtualBox sont des exemples d'hyperviseurs de type 2. 

Qu’est-ce qu’un serveur?:

Dispositif informatique qui offre des services  a un ou plusieurs clients. WWW,  mail, partage de périphériques , base de données, contrôle d’accès…Un serveur répond automatiquement a des requêtes provenant d’autres dispositifs informatiques(clients). Les requêtes sont normalisées et se conforment a des protocoles réseaux.

WWW:
Système hypertexte public fonctionnant sur internet. Le Web permet de consulter, avec un navigateur, des pages accessibles sur des sites.

Internet:
Réseau informatique mondial accessible au public. 

HTTP:
Hypertext Transfer Protocol, protocole de communication client-serveur développé pour le www. HTTPS est la variante sécurisée par le chiffrement et l’authentification. Les clients HTTP les plus connus sont les navigateurs web.

TCP:
Transmission Control Protocol. Protocole de transport fiable. TCP découpe le flux d’octet en segments. Il établit la connexion, transfert les données, clos la connection

IP:
Internet Protocol. Famille de protocoles de communication de réseaux informatiques conçus pour entre utilisés sur internet.

HTML:

Hypertext Markup Language. Langage de balisage cousu pour representer les pages web.

Pourquoi utiliser une machine virtuelle ?:

La consolidation du serveur est l'une des principales raisons qui justifient l'utilisation de machines virtuelles. La plupart des systèmes d'exploitation et des applications n'utilisent qu'une petite partie des ressources physiques disponibles lorsqu'ils sont déployés sur un système bare metal. Grâce à la virtualisation de vos serveurs, vous disposez de nombreux serveurs virtuels sur chaque serveur physique, ce qui permet d'optimiser l'utilisation du matériel. 
Vous n'avez pas besoin d'acheter des ressources physiques supplémentaires, notamment des disques durs, et vous réduisez les besoins en matière d'alimentation, d'espace et de refroidissement dans le datacenter. Les machines virtuelles offrent des fonctions de récupération après sinistre supplémentaires parce qu'elles disposent de capacités de basculement et de redondance qu'il n'était auparavant possible d'obtenir qu'avec du matériel supplémentaire.
Une machine virtuelle fournit un environnement isolé du reste du système, donc il ne peut y avoir aucune interférence entre les programmes exécutés au sein d'une machine virtuelle et sur le matériel hôte.
Comme les machines virtuelles sont isolées, elles peuvent être utilisées pour tester de nouvelles applications ou mettre en place un environnement de production. Vous pouvez également exécuter une machine virtuelle réservée à un processus spécifique.

Aide de Oracle VM VirtualBox
https://docs.oracle.com/en/virtualization/virtualbox/
————————————————————————————————————————————————————————————

Déroulement du projet

-Pour réaliser ce projet nous allons nous servir du logiciel de virtualisation VirtualBox qui est présent sur l’ordinateur.

-On ouvre VirtualBox et on clique sur nouveau.

-On donne un nom à notre machine, un emplacement mémoire et on choisit le système qui sera virtualisé et dans le cas présent on nous recommande Linux Debian 

-On nous demande la quantité de ram dont nous avons besoin et VirtualBox nous recommande 1024MB

-On nous demande de choisir une option pour le disque dur et on choisit de créer un nouveau disque dur

-On choisit le type de fichier qu’on veut utiliser pout notre nouveau disque dur, dans ce cas la il s’agira de .VDI, Virtual Disk Image. Format propriétaire de VirtualBox

-On choisit si la memoire sera gérée dynamiquement ou pas et dans ce cas oui, celle-ci s’agrandira jusqu’a atteindre la limite maximale disponible dans la machine virtuelle

-On choisit la taille de la memoire, et comme je suis tenté de me lancer aussi dans les bonus je choisit 30.83 GB

-On appuie sur enter et la machine virtuelle est créée, il faut encore la configurer

-On sélectionne la virtualbox créée et on va dans settings -> storage ->  dans l’image disque du contrôleur IDE on télécharge l’image de Debian et on l’assigne à l’optical drive

-Maintenant on peut starter la machine virtuelle avec la flèche verte

-On peut changer la taille de la fenêtre en cliquant sur l’icône display -> virtual screen 1 -> scale to 200% (autoscaled output)

-On continue l’installation et comme on veut un s’emmerder dans le detail on ne choisit pas l’installation graphique mais la simple installation

-On choisit la langue d’installation et la langue par défaut soit anglais

-On choisit le pays, et comme l’Espagne n’est pas dans les possibilités ca devint le système horaire américain avec la langue du nord de l’Amérique

-Au pas suivant on nous demande de choisir le hostname nom d’hôte qui, comme le donne la donnée de l’exercice est notre login +42 soit ageiser42

Hostname: etiquette attribuée a un appareil connecté a un réseau informatique qui permet de l’identifier par exemple sur internet

-La fenêtre suivante nous demande un domain name mais comme la donnée ne nous demande rien à ce sujet, on écrit rien 

Domain name: ensemble d’ordinateurs relies ensemble et partageant une caractéristique commune

-Il est temps de créer un mot de passe administrateur du root qui doit contenir au moins 7 caractères , une majuscule, une minuscule un nombre et ne pas contenir plus de 3 caractères consécutifs identiques. Je choisis : Born2be42.

-On le réécrit pour la confirmation

-Pas suivant on choisit un nom d’utilisateur different de l’admin user qui était ageiser42, je choisi ageiser 

-Pas suivant aussi ageiser

-On choisit un mot de passe pour notre nouvel utilisateur avec les mêmes règles qu’avant mais au mois 10 caractères ce sera Pleiades42.

-On configure l’heure de la time zone en l’occurence ce sera Madrid

-La fenêtre suivante est pour le partitionment du disque, comme je veux faire les bonus il faut choisir manuel pour pouvoir éditer les partitions une a une

-La fenêtre suivante nous montre nos partitions et points de montage et nous n’avons actuellement aucune partition de faite. On choisit le périphérique sur lequel nous voulons le créer et dans ce cas il n’y a qu’un choix de possible

-On accepte la confirmation suivante qui nous dit que si il y a déjà des partitions sur le périphérique, elles seront supprimées

-Ici apparaît notre table de partition vide, nous allons la configurer et pour ceci la sélectionner

-On crée une nouvelle partition

-On crée la nouvelle partition selon la donnée soit “sda1” 500m

-On choisit le type de partition qui dans ce cas sera primaire vu qu’on voudra y installer l’ OS

Les types de partition:

Primaire: la seule possible pour pouvoir installer un OS, il ne peut y avoir que 4 partitions primaires par disque ou 3 primaires et une étendue

Secondaire/étendue: conçue pour briser la limitation de 4 partitions principales sur un seul disque physique, il ne peut y avoir qu’une seule partition de ce type par disque et n’est utilisé que pour contenir des partitions logiques

Logique: occupe une partie ou la totalité de la partition étendue/primaire, qui a été formatée avec un type de système de fichiers spécifique (dans notre cas, nous utiliserons ext4) et assignée à un lecteur afin que le système d'exploitation reconnaisse les partitions logiques ou votre système de fichiers . Il peut y avoir un maximum de 23 partitions logiques dans une partition étendue, cependant Linux, le système d'exploitation avec lequel nous travaillons actuellement le réduit à 15, plus que suffisant pour mener à bien ce projet.

ext4:

Système de fichier principalement destiné aux systèmes basés sur GNU/LINUX. Voir wikipedia pour plus de détails.

UNIX:

Système d’exploitation qui repose sur un interpreteur ou superviseur (le shell)

Shell Unix:

Interpréteur de commandes destiné aux systèmes d’exploitation Linux

GNU:

Système d’exploitation libre qui reprend les concepts de Unix

Linux:

Système d’exploitation Open Source basé sur Unix

Debian:

Système d’exploitation Linux mis au point et maintenu par la team Debian

-Choisir si l’on veut mettre cette partition au début ou à la fin de l’espace, en l’occurence au début.

-Fenêtre suivante est l’état actuel de notre partition, on modifie le mount point comme demandé dans la donnée, pour ce faire on choisi boot

-On termine cette partition en choisissant : done setting up the partition

-On devrait maintenant voir notre partition apparaitre, maintenant nous devons créer une partition logique avec tout l’espace disque disponible, non montée et chiffrée. Par ce faire, nous sélectionnons l’espace libre où nous voulons le créer

-On cree une nouvelle partition

-On choisit la taille max

-Le type sera logical cette fois

-Dans mount point on sélectionne: do not mount it

-Done setting up the partition

-On configure les volumes cryptés pour pouvoir crypter notre volume, on choisit: configure encrypted volumes

-On accepte la confirmation

-On crée les volumes cryptés

-On choisit la partition à crypter qui en l’occurence est celle qui ne contient pas l’OS

-Done setting up the partition

-Finish

-Nouveau message de confirmation qui nous dit que tout ce qui se trouve dans le dossier sera crypté

-On choisit cancel

-Il y a demande de creation de mot de passe je choisis Pleiades42-

-On répète le meme code

-On configure maintenant le gestionneur de volume logique

-On accepte la confirmation qui nous dit que les changements seront gardés sur le disque

-On crée un groupe de volume, se sont des groupements de partitions 

-Le nom sera LVMGroup comme demandé

-On crée ce groupe avec la partition non os

-Maintenant on crée toutes les partitions logiques 

-Create logical volume

-On choisit le groupe que l’on vient de créer

-On choisit le nom du volume logique, le premier est root donc on tape root

-Comme indiqué dans le sujet, ce volume sera de 10GB

-Même operation pour swap 2.3g / utilisé pour décharger la RAM lorsque celle-ci est pleine

-Même operation pour home 5g / utilisé pour les fichiers utilisateurs

-Même operation pour var 3g  / utilisé pour les fichiers variables, dont la taille augmente ou diminue par exemple 

-Même operation pour srv 3g / utilisé pour les données serveur

-Même operation pour tmp 3g / utilisé pour  les fichiers temporaires qui sont effacé au démarrage

-Même operation pour var-log 4g / utilisé pour les fichiers log

Pour de plus amples informations : https://www.dell.com/support/kbdoc/fr-fr/000131456/types-et-definitions-des-partitions-et-repertoires-linux-ubuntu?lwp=rt

-Finish

-On peut maintenant voir toutes nos partitions et espace libre et les partitions logiques, nous devons les configurer pour sélectionner le système de fichiers que nous voulons et le point de montage indiqué par le sujet. Nous allons dans l’ordre et nous sélectionnons le premier qui apparait qui est home

Point de montage: répertoire à partir duquel sont accessibles les données se trouvant sous forme d’un système de fichiers sur une partition de disque dur ou un périphérique

-On va dans: use as:

-On choisit le système d’archive qui est le plus utilisé avec Linux soit ext4

-Le point de montage sera home comme indiqué dans le sujet

-Done setting up the partition

-Même opération pour root ext4 mount root

-Même opération pour srv ext4 mount srv

*Pour swap ce sera different: use as: swap area

-Done setting up the partition

-Pour tmp même operation que *, ext4, mount tmp

-Même opération pour var ext4 mount var

-Pour var log c’est different: ext4, mount point enter manually, /var/log, done setting up the partition

-Finish partitioning and write changes to disk

-On confirme

-On nous demande si on veut des paquets additionnels, mais non 

-On choisit notre pays, en l’occurence l’Espagne

-On choisit le mirror de notre region deb.debian.org

-On laisse le choix du proxy vide

Proxy: composant logiciel informatique qui joue le rôle d’intermédiaire en se plaçant entre deux hôtes pour faciliter ou surveiller leurs échanges

-On nous demande si les programmeurs de virtual box peuvent se servir de nos informations, on les envoie chier

-On enlève toutes les additions de programme supplémentaires

-Il faut installer grub boot loader qui n’existe pas encore dans ce bordel


Boot loader: logiciel permettant de lancer un ou plusieurs systèmes d’exploitations sur la même machine

GNU GRUB:  https://www.gnu.org/software/grub/

-On choisit le périphérique pour le boot loader ce sera le présélectionne Ata vbox

-On appuie sur continue 

Configuration de la machine virtuelle:

-On nous demande notre code, le code d’encryptage,  qui est le dernier que j’ai cree soit Pleiades42-

-On nous demande d’introduire le nom d’utilisateur et le code mais pas de l’admin soit ageiser avec le code Pleiades42.

-On est enfin prêt à configurer notre machine virtuelle

-Installation de SUDO et configuration des utilisateurs et groupes

SUDO:

Substitute User DO, Super User DO ou Switch User DO. Permet a un administrateur système d’accorder a certains utilisateurs des droits d’utilisation
La commande su[vide]  ou su[root], nous amène au root user et su[ageiser] passe au simple user

-Pour pouvoir installer le sudo on doit commencer par être en utilisateur root. Pour ce faire on entre “su” dans le terminal virtuel et on introduit le code root qui dans mon cas est Born2be42.

-On tape la commande: apt install sudo pour installer les paquets nécessaires

-Une fois que c’est fait on doit redémarrer la machine grace a la commande: sudo reboot

-Une fois redémarré ont réintroduit le code d’encryptage, Pleiades 42-, le nom d’utilisateur ageiser, le code, Pleiades42.

-On se remet en mode superuser, soit su suivi du code Born2be42.

-Pour verifier l’installation correcte de sudo on tape la commande sudo -V. En plus de nous montrer la version de sudo installée, on nous montre aussi les arguments pour la configuration quand s’est créé sudo et les plugins qui montrent des informations plus détaillées. Pour pouvoir lire ce fichier en entier on tape sudo -V > file.txt et ensuite éditer le fichier avec nano file.txt, ou alors on tape sudo -V | more pour pouvoir lire tout le fichier directement dans le terminal virtualbox.

-Ensuite, toujours en étant root user on crée un utilisateur avec notre login avec la commande: sudo adduser ageiser. Comme on a déjà créé un utilisateur à notre nom , celui-ci doit nous retourner que cet utilisateur existe deja.

-Maintenant on doit créer un nouveau groupe appelé user 42. Pour la créer nous tapons la commande : sudo addgroup user42

On obtient le GID qui est le Group ID

Pour verifier que les choses se sont bien passées on utilise la commande: getent group user42

Avec la commande: sudo adduser user group, on inclut les utilisateurs dans le groupe, on doit y inclure sudo et user42, soit: sudo adduser ageiser user42
																		et: sudo adduser ageiser sudo

pour verifier tout le passage sudo, on tape la commande: getent group sudo et getent groupe user42


Installation et configuration de ssh

SSH: Secure Shell, protocole de communication sécurisé. Il impose une clé de chiffrement. Tous les segments TCP seront chiffrés. Sa fonction principale est l’accès à distance à un serveur via un canal sécurisé dans lequel toutes les informations sont cryptées

TCP: Transmission Control Protocol, protocole de transport fiable.

Shell: interface système. Couche logicielle qui fournit l’interface utilisateur d’un système d’exploitation. Interface informatique qui coordonne les interactions homme-machine

-Commençons par mettre à jour le système avec la commande: sudo apt update

-ensuite on installe l’outil principal pour l’accès (remote) avec le protocole ssh en utilisant openssh.  La commande pour télécharger OPENSSH est :

sudo apt install openssh-server, on écrit: y, à la demande de confirmation

-Pour verifier que l’installation des services ssh s’est bien passée nous utilisons la commande: sudo service ssh status

-Une fois l’installation terminée, il s’est créé quelques fichiers que nous devons configurer. Pour ça nous utiliserons nano qui est pré installé contrairement à vim. En étant utilisateur root, nous commencerons par éditer le fichier sshd_config avec cette commande: sudo nano /etc/ssh/sshd_config 

-Les étoiles en début de ligne sont des lignes commentées, les lignes que nous allons modifier devront être décommentées

-Nous modifions le port qui doit être 4242 plutôt que 22, le permit root login doit être permit root login no, ctrl x, y et enter pour sauvegarder les changements

-Maintenant on édite le fichier ssh_config avec la commande: nano /etc/ssh/ssh_config, on modifie aussi le port en 4242, ctrl x, y, enter

-Pour finir on doit réinitialiser le service ssh pour que les modifications soient actualises. On écrit la commande: sudo service ssh restart et on vérifie notre statut actuel avec la commande sudo service ssh status, on regarde si les serveurs listening sont calés sur le port 4242

Installation et configuration de UFW

UFW: uncomplicated Firewall, est un programme informatique pour gérer un pare-feu netfilter

Pare-feu: logiciel ou matériel permettant de faire respecter la politique de sécurité du réseau. Définition des types de communications autorisés sur ce réseau informatique. Surveillance et contrôle des applications et flux de données.

Netfilter: framework implémentant un firewall au sein du noyau Linux

Framework:  environnement de développement. Ensemble coherent de composants logiciels structurels qui sert a créer les fondations ainsi que les grandes lignes d’un logiciel, c’est a dire une architecture.

-Premiere chose a faire, installer ufw avec la commande: sudo apt install ufw, confirmation avec y

-Une fois installé, nous devons l’activer, pour ça nous utilisons la commande suivante: sudo ufw enable, il nous retournera que le firewall est actif

-Maintenant, ce que nous devons faire est de faire en sorte que notre pare-feu autorise les connexions effectuées via le port 4242. Nous le ferons avec la commande suivante: sudo ufw allow 4242

-Pour terminer  nous testons que nous avons correctement configuré le ufw en regardant l’état de notre pare-feu et que les connections se passant via le port 4242 sont autorisées. Commande: sudo ufw status

Configurer un code fort pour sudo

-Se rendre dans le fichier racine: cd .. cd ..

-On cree un fichier dans le chemin /etc/sudoers.d/de mon fichier. Je l’appelle sudo_config parce que la configuration du mot de passe sera stocké dns ce fichier. La commande est : touch /etc/sudoers.d/sudo_config

-On doit créer le repertoire sudo dans le chemin /var/log parce que chaque commande que nous exécutons avec sudo, tant avec input que output doit rester stockée dans ce repertoire. Commande mkdir /var/log/sudo

Nous devons éditer le fichier créé. Commande: nano /etc/sudoers.d/sudo_config

-On tape dans ce fichier, suivant la demande de l’exercice:

Defaults  passwd_tries=3 // 3 tentatives possibles de faux code

Defaults  badpass_message=“wrong password” // message personnalisé pour un mauvais code sudo

Defaults  logfile="/var/log/sudo/sudo_config”// chaque action utilisant sudo sera archivée dans ce fichier

Defaults  log_input, log_output // les input et output seront archivées dans le fichier suivant

Defaults  iolog_dir="/var/log/sudo" //fichier in out

Defaults  requiretty //activation du mode tty, assistance particulière pour raison de sécurité

Defaults  secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin" // le chemin 		utilisé par sudo doit être restraint

-Ctrl x, y, enter

Configuration de la politique de code forte


-Le premier pas est d’editer le fichier login.defs. commande: sudo -On change le pass_max_days a 30, le code ne doit être valable que 30 jours

-On change aussi pass_min_days à 2, nombre de jours permis avant de modifier un code

-On quitte et sauve

-Pour pouvoir continuer avec la configuration, on doit installer des paquets supplémentaires avec la commande: sudo apt install libpam-pwquality, y

-Le pas suivant est d’éditer un autre fichier. Commande: nano /etc/pam.d/common-password, après retry=3, 

-on rajoute minlen=10 quantité minimale de caractères du code

-ucredit=-1 doit contenir au minimum un caractère majuscule

-dcredit=-1 doit contenir au moins un numero

-maxrepeat=3 il ne doit pas contenir plus de 3 memes caractères suivis  

-reject username, ne peut contenir le nom d’utilisateur

-difok=7, doit contenir au moins 7 caractères qui ne font pas partie de l’ancien code

-enforce_for_root nous implémentons ceci pour l’utilisateur root

-Ctrl x, y

Se connecter via SSH

-Pour se connecter par ssh on doit fermer la machine, ouvrir virtual box et aller sur configuration

-On va dans l’onglet network, réglages avancés, port forwarding

-Ajouter, en haut a droite

-Host port et guest port doivent être sur 4242, ok, ok

-Pour pouvoir nous connecter à la machine virtuelle depuis la machine réelle, nous rallumons la machine virtuelle, nous devons ouvrir un terminal sur la machine réelle et écrire : ssh ageiser@localhost -p 4242. Il nous demandera le mot de passe Pleiades42. su et une fois entré, le login apparaitra en vert et cela signifiera que nous sommes connectés  

Script:

Script, programme informatique en langage interprété. Séquence de commande gardée dans un fichier qui, quand il s’exécute, exécute la fonction de chaque commande

-Architecture. Pour pouvoir voir l’architecture de l’os on peut taper la commande: uname -a

-Pour afficher le nombre de processeurs physiques, on utilise le fichier /proc/cpuinfo qui fournit des informations sur le processeur, type, marque etc, nous utilisons la commande: grep “physical id” /proc/cpuinfo | wc -l. Avec la commande grep (recherche), nous recherchons dans le fichier physical id et avec w -l on compte les lignes du résultat de grep. Nous le faisons car la façon de quantifier les processeurs n’est pas courante. Si il n’y a pas de processeurs, il marquera 0 et si il y a un processeur ou plus il affichera toutes les informations. De cette façon, nous compterons simplement les lignes qu’il y a car c’est plus simple de quantifier de cette façon 

-Pour montrer le nombre de processeur virtuel c’est similaire au point précédent avec la commande: grep processor /proc/cpuinfo | wc -l

-Pour montrer la memoire ram nous utiliserons la commande: free pour voir sur le moment les infos de la ram. Free --help nous donne des infos sur cette commande. Nous utilisons la commande free --mega  parce que dans le sujet c’est demandé.

-Une fois fait cette commande, on doit filtrer les informations reçues parce qu’on pas besoin de tout, le premier point utile est la memoire utilisée, pour ça on utilise la commande: awk. permet de filter les information qu’on cherche dans un fichier pour finir nous comparons si le premier mot d’un file est égale à MEM, nous afficherons le troisième mot de la ligne qui est la memoire utilisée. La commande complete est: free —mega | awk ‘$1 == “Mem:” {print $3}’. Dans le script, la valeur de retour de cette commande est assignée à une variable qui nous concatène avec les autres variables pour que tout reste égal comme le spécifie le sujet

-Pour obtenir la memoire totale, on affiche la deuxième colonne. Commande: free —mega | aww ‘$1 ==“Mem:” {print $2}’

-Pour la partie ultime de la ram on doit calculer le % de memoire utilisée. La commande est aussi similaire aux précédentes ne modifiant que la façon dont les informations doivent être affichées. Comme l'opération pour obtenir le pourcentage n'est pas exacte, elle peut nous donner de nombreuses décimales et seulement 2 apparaissent dans le sujet, nous ferons donc de même, c'est pourquoi nous utilisons %.2f pour que seules 2 décimales soient affichées. Pour afficher un %, vous devez mettre %%. L'intégralité de la commande: free --mega | awk '$1 == "Mémo :" {printf("(%.2f%%)\n", $3/$2*100)}'.

Memoire disque

-Pour pouvoir voir la mémoire disque libre et utilisée on se sert de la commande df qui signifie disk filesystem, utilisée pour obtenir un resumé complet de l’utilisation du disque. Le sujet indique que la mémoire utilisée est en MB donc on utilise le flag -m. Ensuite on fait un grep pour nous montrer seulement les lignes qui contienne “/dev/“ et ensuite un autre grep avec le flag -v pour exclure les lignes contenant “/boot”. Enfin la commande awk, et on additionne la valeur du troisième mot de chaque ligne et afficher le résultat final de la somme. La commande entière est: df -m | grep "/dev/" | grep -v "/boot" | awk '{memory_use += $3} END {print memory_use}'

-Pour obtenir l’espace total, nous utilisons une commande similaire. Les uniques différences sont que nous additionnerons les valeurs de $2 plutôt que $3 et la deuxième différence est que nous voulons la valeur en GB. Pour ça nous devons diviser le numéro par 1024 et enlever les décimales. Commande: df -m | grep "/dev/" | grep -v "/boot" | awk '{memory_result += $2} END {printf (“%.0fGb\n”), memory_result/1024}’

-Pour finir on doit montrer un pourcentage de la memoire utilisée. Pour ca encore quelque chose de similaire. Cette fois-ci on veut deux variables, une pour la memoire utilisée et l’autre pour la totale. Nous utiliserons une operation pour obtenir le % soit use/total*100 et le résultat de cette operation on l’affichera selon le sujet, entre parenthèse et avec le symbole %. La commande: df -m | grep "/dev/" | grep -v "/boot" | awk '{use += $3} {total += $2} END {printf("(%d%%)\n"), use/total*100}'

Pourcentage de cpu utilise

-Nous utilisons la commande vmstat pour ça, cela montre les statistiques système. Dans mon cas je mettrai un intervalle de 1 a 4 secondes. On donne aussi la commande tail -1 qui nous affichera que la dernière ligne donc pour les 4 lignes générées on n’affichera que la dernière. On ne veut que le mot 15 qui est l’utilisation de la mémoire disponible.  La commande entière est : vmstat 1 4 | tail -1 | awk '{print %15}’. Le résultat de cette commande est seulement une partie du résultat final parce qu’il faut encore faire une opération dans le script pour que ça se passe bien. Ce que nous aurons à faire est de soustraire de 100 le montant que notre commande nous a renvoyé, nous imprimerons le résultat de cette opération avec une décimale et un % à la fin et l'opération serait effectuée

Dernier démarrage

Pour voir l’heure et la date de notre dernier démarrage nous utilisons la commande: who avec le flag -b qui nous montrera la durée du dernier démarrage du système. Nous filtrons les informations avec awk. On affiche la ligne 3 et 4 avec un espace entre deux la commande entière est la suivante: who -b | awk '$1 == "system" {print $3 " " $4}'

Utilisation de LVM

LVM, logical volume management, logiciel de gestion de l’utilisation des espaces de stockage d’un ordinateur

Pour verifier que LVM est actif, on utilise la commande lsblk qui nous donnera des informations sur toutes les mémoires de l’ordi: SSD, disque dur…

On commence par un if qui nous donnera un retour en yes or no. Basiquement la condition que nous cherchons est de conter le nombre de ligne ou apparait LVM et si il y en a plus que 0 on retourne yes, si 0 no. La commande est : if [ $(lsblk | grep "lvm" | wc -l) -gt 0 ]; then echo yes; else echo no; fi

Connections TCP

Pour voir le nombre de connection tcp établi, on utilise la commande ss qui se substitue a netstat qui est obsolète. On filtre avec le flag -ta pour ne montrer que les connections tcp. On fait une recherche avec wc -l pour citer le nombre de ligne. La commande est:  ss -ta | grep ESTAB | wc -l

Nombre d’utilisateur

Avec la commande user, cela affichera le nombre d’utilisateur existant. On ajoute le flag wc -w pour compter la quantité de mot qu’il y a en sortie de commande. La commande entière est: users | wc -w

Adresse IP et MAC

Adresse IP: numero d’identification attribué de façon provisoire ou permanente à chaque périphérique relié à un réseau informatique qui utilise l’Internet Protocol

Adresse MAC: Media Access Control, ou adresse physique est un identifiant physique stocké dans une carte réseau. 

Pour obtenir l’adresse du Host, on utilise la commande hostname -I et pour obtenir l’adresse MAC la commande ip link. Comme il apparait plus d’une interface, on utilise la commande grep pour chercher ce que l’on souhaite et ainsi pouvoir afficher seulement ce qu’on nous demande. Commande : ip link | grep "link/ether" | awk '{print $2}' , de cette bacon on affichera que l’adresse MAC

Nombre de commandes exécutées avec SUDO

-On utilise pour ça la commande: journalctl qui est un outil qui se charge de collecter et gérer les registres systèmes. On ajoute  _comm=sudo pour filtrer les entrees. Dans notre cas comm qui fait reference à un script executable. On refiltre avec un grep COMMAND pour les fois où on commence et fini une cession il y a des infos dont on se fout. Un wc -l pour sortir des lignes numérotées. La commande entière est :  journalctl _COMM=sudo | grep COMMAND | wc -l. Pour verifier que que ca fonctionne correctement on envie la commande dans le terminal, on fait une commande incluant sudo et on refait la commande et ca devrait avoir incrémenté le nombre d’execution de sudo.

Script final:

#!/bin/bash

# ARCH
arch=$(uname -a)

# CPU PHYSICAL
cpuf=$(grep "physical id" /proc/cpuinfo | wc -l)

# CPU VIRTUAL
cpuv=$(grep "processor" /proc/cpuinfo | wc -l)

# RAM
ram_total=$(free --mega | awk '$1 == "Mem:" {print $2}') mega parce que mega bit
ram_use=$(free --mega | awk '$1 == "Mem:" {print $3}')
ram_percent=$(free --mega | awk '$1 == "Mem:" {printf("%.2f"), $3/$2*100}')

# DISK
disk_total=$(df -m | grep "/dev/" | grep -v "/boot" | awk '{disk_t += $2} END {printf ("%.1fGb\n"), disk_t/1024}')
disk_use=$(df -m | grep "/dev/" | grep -v "/boot" | awk '{disk_u += $3} END {print disk_u}')
disk_percent=$(df -m | grep "/dev/" | grep -v "/boot" | awk '{disk_u += $3} {disk_t+= $2} END {printf("%d"), disk_u/disk_t*100}')

# CPU LOAD
cpul=$(vmstat 1 2 | tail -1 | awk '{printf $15}')
cpu_op=$(expr 100 - $cpul)
cpu_fin=$(printf "%.1f" $cpu_op)

# LAST BOOT
lb=$(who -b | awk '$1 == "system" {print $3 " " $4}')

# LVM USE
lvmu=$(if [ $(lsblk | grep "lvm" | wc -l) -gt 0 ]; then echo yes; else echo no; fi)

# TCP CONNEXIONS
tcpc=$(ss -ta | grep ESTAB | wc -l)

# USER LOG
ulog=$(users | wc -w)

# NETWORK
ip=$(hostname -I)
mac=$(ip link | grep "link/ether" | awk '{print $2}')

# SUDO
cmnd=$(journalctl _COMM=sudo | grep COMMAND | wc -l)

wall "	Architecture: $arch
	CPU physical: $cpuf
	vCPU: $cpuv
	Memory Usage: $ram_use/${ram_total}MB ($ram_percent%)
	Disk Usage: $disk_use/${disk_total} ($disk_percent%)
	CPU load: $cpu_fin%
	Last boot: $lb
	LVM use: $lvmu
	Connections TCP: $tcpc ESTABLISHED
	User log: $ulog
	Network: IP $ip ($mac)
	Sudo: $cmnd cmd"

Crontab


Gestionnaire de processus en arrière plan, les processus seront exécutés au moment programmé dans Crontab

-Pour configurer correctement crontab on doit éditer son fichier ave la commande: sudo crontab -u root -e, on choisit l’éditeur et comme j‘ai tout fait avec nano, je continue

-On doit ajouter une ligne de commande qui est */10 * * * * sh /home/ageiser/monitoring.sh. c’est une commande qui s’exécutera toutes les 10 minutes

Les paramètres de Crontab: 	m-> correspond au nombre de minutes ou va s’exécuter le script
					h -> correspond à l’heure où doit s’exécuter le script
					dom correspond au jour du mois
					mon le mois
					dow le jour de la semaine de 1 a 7
					user defini l’utilisateur qui va executer le script
					command -> route du script à exécuter 

Signature.txt

Pour obtenir la signature, la premiere chose à faire est éteindre la machine virtuelle, car à chaque fois qu’on l’allume ou qu’on fait une modification, la signature changera

Le pas suivant est de se retrouver avec le terminal standard dans le dossier dans lequel on a notre fichier .vdi de notre machine virtuelle dans sgoinfre

Avec la commande shasum Born2BeRoot.vdi ca nous donnera la signature. Cette signature nous l’ajouterons a notre fichier signature.txt pour plus tard mettre le fichier dans le repertoire de l’intra.  On réouvre la machine. La signature change. Pour les corrections, se souvenir de cloner la machine pour ne pas craindre que la signature change Attention, étape non terminée

Shasum est une commande qui permet de verifier l’intégrité d’un fichier en faisant la somme du contrôle du hash SHA-1 d’un fichier

Bonus:

Lighttpd:

Lighttpd est un serveur web désigné pour être rapide sûr et flexible. Optimisé pour les environnements où la vitesse est importante. Il consomme moins de CPU et de Ram que les autres serveurs

-On installe le package lighttpd avec la commande: sudo apt install lighttpd

-On permet les connections via le port 80 avec la commande sudo ufw allow 80

-On vérifie que ça roule avec la commande sudo ufw status

-On ajoute la règle du port 80 comme on l’a fait dans virtual box pour le port 4242

MariaDB:

MariaDB est une base de donnée. Utilisée à des fins de stockage de données, de commerce électronique, de fonctions au niveau de l’entreprise et les applications de tenue de registre.

-On installe les paquets avec la commande: sudo apt install mariadb-server

-Étant donné que la configuration par défaut laisse votre installation MariaDB non sécurisée, nous utiliserons un script fourni par le package mariadb-server pour restreindre l'accès au serveur et supprimer les comptes inutilisés. Nous allons exécuter le script avec la commande suivante: sudo mysql_secure_installation. Une fois exécuté, le script nous posera une série de questions, notamment si nous voulons passer à l'authentification par socket Unix. Puisque nous avons déjà un compte root protégé nous écrirons Non

-Change root password: n, on ne veut pas changer. Mariadb n’est pas vraiment root puisqu’on lui donne des permissions utilisateurs

-Remove anonymous users: y, par défaut il y a un utilisateur anonyme dans mariaDB. On supprime ce user anonyme vu qu‘on gère tous les details

-Disallow root login remotely: y, on désactive la connection root à distance, nous empêchons qu’on modifie notre code. On ne peut se connecter que depuis localhost

-Remove test database and access to it? : y 

-Reload privilege tables now? Y 

Phpmyadmin:

Phpmyadmin est une application web qui permet de gérer des bases de données de manière simple et avec une interface conviviale

On installe le paquet avec la commande: sudo apt install php_cgi php_mysql phpmyadmin

on tape mariadb

GRANT ALL PRIVILEGES ON * . * TO ‘phpmyadmin ‘@‘ localhost’; 

SHOW DATABASES

Exit

-Toute cette étape peut aussi se faire depuis un navigateur en tapant localhost dans la barre d’adresse

Wordpress:

Content management system. Système de gestion de contenu axe sur la creation de tout type de page web

-Commande: sudo apt install wget zip

-cd /var/www/

-sudo wget https://fr.wordpress.org/latest-fr_FR.zip

-sudo unzip latest-fr_FR.zip

-sudo mv html/ html_old/

-sudo mv Wordpress/ html

-sudo chmod -R 755 html

LiteSpeed:

Logiciel de serveur Web propriétaire. C’est le quatrième serveur web le plus populaire et est utilisé par 10% des sites web.

-On commence par mettre a jour.  	sudo apt update
						sudo apt upgrade

-Par faut, OpenLiteSpeed est disponible dans le référentiel de base Debian 11. On doit donc exécuter une commande pour ajouter le référentiel OPENLITESPEED à mon système Debian. wget -O - http://rpms.litespeedtech.com/debian/enable_lst_debian_repo.sh | sudo bash

-On refait une mise à jour sudo apt update

-sudo apt install openlitespeed

-Le code de base pour OpenLiteSpeed es 123456. On la change pour quelque chose de plus sûr avec la commande : sudo /usr/local/lsws/admin/misc/admpass.sh

-Administrator: ageiser, password Pleiades42,

-Nous configurons le firewall pour autoriser les connections via les ports 8088 et 7080

-Commande: sudo ufw allow 8088/tcp

-sudo ufw allow 7080/tcp

-sudo ufw reload

-Dans la fenêtre de virtual box on ajoute les deux ports

-Une fois terminé, on peut se connecter 

-Dans le moteur de recherche de notre navigateur on tape localhost:7080 en donnant nos identifiants de connexion on doit avoir accès a tout

————————————————————————————————————————————————————————————

Corrections:

-dupliquer la machine virtuelle sinon c’est le merdier

-Alex présent

-signature.txt à giter a la racine de mon machin git

-Verifier que signature.txt de mon git est le même que mon .vdi qui se trouve a sgoinfre/Perso/ageiser/Born2BeRoot/Born2BeRoot.vdi

-taper la commande shasum Born2BeRoot.vdi pour afficher la signature

-démarrer la machine virtuelle clonée

Partie obligatoire:

-Comment fonctionne une machine virtuelle?

C’est un programme qui simule un OS et qui peut executer des programmes comme si c’était un ordinateur réel.

-Pourquoi choisir Debian?

Premièrement parce que Debian est chaudement recommandé, ensuite j’ai un système linux chez moi donc ca m’était utile. Rocky est plus dédié aux entreprises

-difference en rocky et Debian?

https://sourceforge.net/software/compare/Debian-vs-Rocky-Linux/

-La finalité d’une machine virtuelle?

Son objectif est de fournir un environnement d'exécution indépendant de la plate-forme matérielle et système d'exploitation.

-En choisissant Debian, quelle difference entre apt, aptitude de APPArmor. Pendant l’evaluation le script doit s’afficher toutes les 10 minutes. Ses actions seront vérifiées plus tard

aptitude est une version améliorée de apt qui gère mieux les dépendances des paquets. Aptitude include plus d’options que apt ce sont deux lignes de commande. On connais surtout apt-get. APT = Advanced Packaging Tool.

Apparmor est une application de sécurité système. Permet de restreindre les capacités d’un programme 

Simple setup:

-On démarre la machine virtuelle et comme elle nous propose pas d’interface graphique c’est qu’on l’a programmée sans, on peut aussi taper la commande: ls /usr/bin/*session. Si /usr/bin/dbus-run-session s’affiche c’est que je n’ai pas utilise de méthode graphique

On tape le code Pleiades42-

user login : ageiser, code: Pleiades42.

Pour voir les règles des codes, on se met en mode root soit su root, Born2be42. On tape nano /etc/login.defs

On modifie un autre fichier : nano /etc/pam.d/common-password

A la premiere ligne non commentée on a fait des modifications

-verifier que le service UFW est actif: sudo ufw status

-verifier que le service ssh est actif : sudo service ssh status

-verifier que le système choisi est rocky ou Debian: uname -v ou uname --kernel-version

User:

-verifier que l’utilisateur cree est bien xxx42 et qu’il appartient au groupe sudo et user42 

getent group sudo, getent commande get entries pour une grande base de données 

getent group user42

-créer un nouvel utilisateur et montrer la politique de code forte créée 

sudo adduser xxx  // sudo deluser xxx

Essayer jusqu’à ce que le code fonctionne

Ajouter un groupe evaluating sudo addgroup evaluating  // sudo delgroup evaluating

Ajouter le nouvel utilisateur a ce groupe sudo adduser xxx evaluating

Verifier ce qu’on vient de faire avec getent group evaluating


Hostname and partitions:

-Verifier que le hostname de la machine est un login correct de 42, donc pour moi ageiser42

hostname

-modifier le hostname pour le remplacer par celui de l’utilisateur

sudo nano /etc/hostname (student42)

-Modifier notre login par le nouveau

sudo nano /etc/hosts

-Redémarrer la machine

sudo reboot

Une fois redémarré et avoir indique notre code Pleiades42-, on constate que le user42 est different

-on reme le host nameoriginal

-montrer les partitionsa

lsblk, verifier que ca correspond a la donnée

Sudo:

-verifier que sudo est bien installé

sudo -V

-assigner un nouvel utilisateur au groupe sudo

sudo adduser xxx sudo // sudo deluser xxx sudo

getent group sudo

-montrer les règles sudo imposées dans le sujet

nano /etc/sudoers.d/sudo_config

-montrer que le chemin /var/log/sudo existe, qu’il contient au moins un fichier, on devrait y voir un historique des commandes utilisées avec sudo

cd /var/log/sudo

cat sudo_config

Faire une commande sudo et verifier que la liste est mise a jour

sudo nano hello

cat sudo_config

UFW:

-Verifier que le programme UFW est installe dans la machine virtuelle et verifier que ca marche correctement

dpkg -s ufw

sudo service ufw status

-Liste des règles actives avec UFW

sudo ufw status numbered

-Ajoute un port et enlève le 

sudo ufw allow 8080

sudo ufw status numbered

sudo ufw delete <num_rule>

sudo ufw status numbered

SSH:

-Verifier que le service ssh est installe et que ca tourne seulement sur le port 4242

which ssh

sudo service ssh status

-Utilise ssh pour commencer une nouvelle session avec le nouvel utilisateur cree, verifier qu’on ne peut pas utiliser ssh avec l’utilisateur root

Ouvrir un terminal standard 

ssh root@localhost -p 4242, ne doit pas fonctionner

ssh ageiser@localhost -p 4242, doit fonctionner Pleiades42.

ssh xxx@localhost -p 4242 doit fonctionner aussi

Script monitoring:

-Expliquer le script

Voir plus haut

-Qu’est ce que cron?

Utilitaire permettant d’accomplir des taches quand on le souhaite

-Changer le temps du script de 10 minutes a 1 minutes, 

sudo crontab -u root -e, on change 10 -> 1

stopper le script quand le serveur a démarré sans modifier le script lui-même.

sudo /etc/init.d/cron stop

sudo /etc/init.d/cron start

Bonus:

-Montrer les partitions créées et verifier que ca correspond à la donnée

lsblk

-configurer worldpress

Taper localhost dans le navigateur 














