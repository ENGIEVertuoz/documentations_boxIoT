# Plugin luna

# Attention souci de Flashage des Luna

Nous avons eu un retour sur une erreur de flashage de certaines Lunas. (uniquement celles expediées avant 2023)
Nous sommes désolé pour ceci et avons prévenu notre revendeur Domadoo.

Si vous arrivez à vous connecter à votre Jeedom, merci de lancer le plugin Luna (Plugins/Passerelle domotique/luna) et d'aller dans : 
  - Mise à jour du module de Recovery
Puis faire le recovery dans :
  - Recovery (Reset Factory)
Cela mettra a jour votre Box completement.

Si vous n'avez pas d'accés à votre box, merci de laisser appuyé le bouton reset de la box pendant plus de 10 secondes; au relachement de ce dernier, la box devrait clignotée;laissez-la finir le processus. Jeedom devrait redevenir operationnel. Vous pourrez faire la procedure ci-dessus pour une mise à jour complete.

Si elle ne clignote pas : 
 - Veuillez contacter Domadoo via le lien suivant; l'équipe Domadoo vous fournira une étiquette de retour et vous réexpédiera une Luna correctement flashée :
https://www.domadoo.fr/rma

# Bientôt Disponible : Hotspot

> Le plugin luna vous permet de vous connecter depuis votre luna à un réseau Wifi (avec ou sans mot de passe).

Pour ce faire, aller dans le plugin luna, puis sélectionner l’équipement Luna. A cet endroit vous pouvez activer puis sélectionner le wifi que vous souhaitez (2.4Ghz et 5Ghz), puis taper le mot de passe et sauvegarder.

Pour le moment, le plugin prend en compte uniquement les accès avec DHCP.

> Mise à jour du module de Recovery

La mise à jour permet de mettre la dernière image en place sur la Luna; celle-ci utilisera cette image lors d’un recovery (bouton reset de la box ou bouton recovery sur le plugin).
Cliquer sur le bouton recovery; la Luna téléchargera la dernière version de son image et redémarrera, les leds vertes sur le boitier de la Luna vont clignoter. 
Une fois ces dernières fixes, vous pourrez y accéder de nouveau via son adresse IP ou via http://jeedomluna.local; le logiciel de recovery sera à jour.

> Recovery (Reset Factory)

Lors d’un reset factory la box est rétablie en configuration d’usine selon l’image mise a jour via le bouton donné ci-dessus. ATTENTION : il faut faire un backup de votre box avant cette opération car vous allez perdre les données de votre box (excepté backup sur la SD).

> LED

Vous pouvez via la commande de type select changer la couleur et l’animation de la led (peut être éteinte).

> Batterie

Vous pouvez,via deux retours d’informations, avoir le pourcentage de batterie ainsi que le type d’alimentation de votre box. (charging, decharging, Full etc…).

> SD

Permet la gestion (formatage) de la carte micro-SD que vous pouvez ajouter à la box, ainsi que le transfert vers cette carte SD des backups Jeedom.

> Les boutons Alimentation et Reset

- Reset : moins de 1 secondes reboot forcer de la box.
- Reset : plus de 10 secondes Reset Factory de la box.
- Alimentation : plus de 10 secondes arret de la fox forcer avec arret de la batterie (il faut avoir enlever l'alimentation electrique pour le faire)

> Hotspot (ALPHA)

Dans la partie Wifi du plugin vous pouvez cocher la case Hotspot ce qui vous permettra de créer un point d'accès wifi sur votre Box luna. (DNS et forwarding IP (pont entre ethernet et wifi) fonctionnel dessus).
