---
layout: default
title: DDoS
parent: Hacking
grand_parent: Outils
nav_order: 6
---

# DDoS
grab une IP puis DDoS (DDoS de 1 à 15Gb/s)
Grabbe l'IP:
Pour attraper l'IP, il suffit de - prendre le lien d'une page que vous voulez envoyer (ex: vidéo youtube),
- raccourcir le lien avec le site 1er site,
- encore raccourcir avec un service de type bit.ly ou autre pour rendre "légit",
- Envoyer le lien final à votre "ami testeur".
L'IP est loggée dans le dashboard.
Le 1er site en question : [https://grabify.link/](https://grabify.link/)
Alternative moins complète mais toujours viable : [iplogger.org](http://iplogger.org/)
  
Le DDos :
Le 2e site :
[https://www.stressthem.to/](https://www.stressthem.to/)
Des nouveaux parce que je suis gentil
[https://str3ssed.co/freestresser.php](https://str3ssed.co/freestresser.php)
[https://instant-stresser.com/#Pricing](https://instant-stresser.com/#Pricing)
[https://stresser.app/](https://stresser.app/)
[https://stresslab.sx/](https://stresslab.sx/)
Pour DDoS, c'est en 2 temps : Lancer un ping via le CMD pour connaître l'état de la connexion puis DDoS.
Le ping nous dira plus tard si le DDoS a fonctionné.
Pour ping, ouvrir le CMD taper la commande :
ping [IP] -t -l 60000
exemple : ping 69.420.93.667 -t -l 60000
Cela va envoyer une requête toutes les secondes pour voir si la connexion de la "victime" est encore active.
Ca passe par votre IP (donc VPN souhaité dans le cas d'une "simulation d'attaque poussée"). <br>
![ip]({{ site.baseurl }}/assets/images/ip.png){: width="300px"}
Pour DDoS : s'inscrire sur le 2e site (lien ci-dessus).
Aller dans Booter Panel et remplir comme suit avec l'IP désirée : <br>
![Booter Panel]({{ site.baseurl }}/assets/images/booter_panel.png){: width="300px"}
Puis "Start Attack".
Le ping affiche maintenant que la connexion n'est plus disponible :<br>
![ip 2]({{ site.baseurl }}/assets/images/ip_2.png){: width="300px"}