---
title: "Myymälän varaston hallinta"
description: "Tässä artikkelissa kuvataan tyyppisiä asiakirjoja, joiden avulla voit hallita varastoa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Myymälän varaston hallinta

Tässä artikkelissa kuvataan tyyppisiä asiakirjoja, joiden avulla voit hallita varastoa.

Organisaation varastoa voi hallita seuraavien asiakirjatyyppien avulla.

## <a name="purchase-orders"></a>Ostotilaukset
Ostotilaukset luodaan pääkonttorilla. Vähittäismyynti-varaston sisältyy ostotilauksen otsikkoon, jos tilauksen voi vastaanottaa myymälässä Moderni POS (MPOS) tai POS pilven avulla Microsoft Dynamics-365 työvaiheiden - Retail. Kirjoitetut määrät, jotka ovat saaneet myymälässä voi tallentaa paikallisesti muita muokattavaksi. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa, määrät, jotka olivat saaneet myymälässä näkyvät Dynamics työvaiheissa, 365 **nyt tulla** ostotilauksen-kentän.

## <a name="transfer-orders"></a>Siirtotilaukset
Siirtotilaus voi määrittää, että nimikkeet lähetetään tietystä myymälästä. Tällöin siirtotilaus näkyy myymälässä keräyksen MPOS tai pilven POS-pyynnön. Määrät, joita pyydetään kerätään, kun ne on vahvistettu ja lähetetty pääkonttoriin. Pääkonttorissa, määrät, jotka on poimittu myymälässä näkyvät Dynamics työvaiheissa, 365 **Lähetä nyt** kentän siirtotilauksen. Siirtotilaus voi määrittää, että nimikkeet lähetetään tiettyyn myymälään. Tällöin siirtotilaus näkyy myymälän MPOS tai pilven POS pyynnön vastaanottava. Kirjoitetut määrät, jotka ovat saaneet myymälässä voi tallentaa paikallisesti muita muokattavaksi. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa, määrät, jotka olivat saaneet myymälässä näkyvät Dynamics työvaiheissa, 365 **nyt tulla** kentän siirtotilauksen.

## <a name="stock-counts"></a>Varaston inventoinnit
Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi. Pääkonttori Luo inventointiasiakirjan voivat vastaanottaa liikkeestä, jossa todellinen käytettävissä olevan varaston määrä syötetään MPOS tai pilven POS. Ajoittamaton varaston inventoinnit ovat Myymälän toimeksiannosta, ja todellinen käytettävissä olevan varaston määrät päivitetään joko MPOS tai pilven POS. Toisin kuin ajoitetut varaston inventoinnit ajoittamattomia varaston inventointeja ei ole ennalta määritetyn arvoluettelon kohteita. Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille. Pääkonttorissa inventointi tarkistetaan ja kirjataan.




