# RfCat

- d.help() = c'est l'aide relative du dongle
- d.setFreq() = sert a définir une fréquence d'émission pour sûr. Fréquence de réception aussi?? Prend une valeur chiffrée en Hz, genre 433920000 pour 433,92 MHz.
- d.setMdmDRate() = prend une valeur pour définir les symboles par seconde, exemple 9600.
- d.setMdmModulation() = sert a définir le mode de modulation. On a MOD_ASK_OOK, MOD_GFSK, MOD_2FSK, MOD_MSK et je ne sais pas les autres. 
- d.makePktFLEN() = défini une taille de paquets fixes pour l'émission... Pour la réception je ne sais pas a quoi ça sert. La taille est définie en octets. Donc \xDE\xAD\xBE\xEF est de longueur 4 octets ou 24 bits
- d.makePktVLEN() = défini une taille variable pour les paquets mais cela suppose que le premier octet indiqué la taille du paquet.
- d.setMdmSyncWord() = definit un préambule , par exemple un préambule
- d.discover() = ??. Exemples : d.discover(identSyncWord=True) = ??? , d.discover(lowball=1), d.discover(SyncWordMatchList=[0x0c4e, 0xf432]) = écoute pour - des syncwords spécifiques ? 
- d.setMdmDeviatn() = ????
- d.specan(a,b,c) = analyse spectrale a-freq, b-bande?, c-???
- d.RFxmit('blah')
- d.RFlisten() = Crache les data a l'écran .
- d.RFcapture() = crache les données a l'ecran et retourne une liste de paquets.
lowball() = ça a un rapport avec le filtrage je pense mais comportement curieux. Du coup la commande désactivé la plupart des filtres du proc. exemple: d.lowball(0) ou d.lowball()
- d.lowballRestore() = remet ce paramètre dans un mode configurable.
- d.reprClientState() = ????
- d.reprRadioConfig() = montre des infos de config
- d.recvAll() = récupérer les paquets en buffer?
- d.scan(basefreq, inc?, Count?, Delaysec?, Bauds, lowball) = scanne une fréquence particulière sur ces paramètres ?
- d._debug =1 = crache les infos de debug au fil de l'eau.
- d.debug() = Crache des infos de debug chaque seconde.
- d.getFHSSState() = 
- d.setFHSSState(FHSS_STATE_DISCOVER) = 
- d.getMACdata() = Note: print d.reprMACdata()
- d.FHSSxmit() =
-  d.setPktPQT() = sert a définir le packet Preamble Quality Threshold.
