---
title: "Myymälän varaston hallinta"
description: "Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>Myymälän varaston hallinta

[!include[banner](includes/banner.md)]


Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa.

Organisaation varastoa voi hallita seuraavien asiakirjatyyppien avulla.

## <a name="purchase-orders"></a>Ostotilaukset
Ostotilaukset luodaan pääkonttorilla. Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään Microsoft Dynamics 365 for Operationsin Modern POS- tai Cloud POS -sovelluksen Vähittäismyynti ja kauppa -kohdan avulla. Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Operationsissa ostotilauksen **Ota vastaan nyt** -kentässä.

## <a name="transfer-orders"></a>Siirtotilaukset
Siirtotilaus voi määrittää, että nimikkeet lähetetään tietystä myymälästä. Tässä tapauksessa siirtotilaus näkyy myymälässä poimintapyyntönä Modern POS- tai Cloud POS -sovelluksessa. Kun pyydetyt määrät on kerätty, ne vahvistetaan ja lähetetään pääkonttoriin. Pääkonttorissa myymälässä kerätyt määrät näytetään Microsoft Dynamics 365 for Operationsissa siirtotilauksen **Lähetä nyt** -kentässä. Siirtotilaus voi määrittää, että nimikkeet lähetetään tiettyyn myymälään. Tässä tapauksessa siirtotilaus näkyy myymälässä vastaanottopyyntönä Modern POS- tai Cloud POS -sovelluksessa. Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Operationsissa siirtotilauksen **Ota vastaan nyt** -kentässä.

## <a name="stock-counts"></a>Varaston inventoinnit
Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi. Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla. Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille. Pääkonttorissa inventointi tarkistetaan ja kirjataan.






