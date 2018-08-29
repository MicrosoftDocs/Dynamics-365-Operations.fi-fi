---
title: "Myymälän varastonhallinta"
description: "Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="store-inventory-management"></a>Myymälän varastonhallinta

[!include [banner](includes/banner.md)]

Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa.

Organisaation varastoa voi hallita seuraavien asiakirjatyyppien avulla.

## <a name="purchase-orders"></a>Ostotilaukset
Ostotilaukset luodaan pääkonttorilla. Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään Microsoft Dynamics 365 for Retailin Modern POS- tai Cloud POS -sovelluksen Vähittäismyynti ja kauppa -kohdan avulla. Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Retailissa ostotilauksen **Ota vastaan nyt** -kentässä.

## <a name="transfer-orders"></a>Siirtotilaukset
Siirtotilaus voi määrittää, että nimikkeet lähetetään tietystä myymälästä. Tässä tapauksessa siirtotilaus näkyy myymälässä poimintapyyntönä Modern POS- tai Cloud POS -sovelluksessa. Kun pyydetyt määrät on kerätty, ne vahvistetaan ja lähetetään pääkonttoriin. Pääkonttorissa myymälässä kerätyt määrät näytetään Microsoft Dynamics 365 for Retailissa siirtotilauksen **Lähetä nyt** -kentässä. Siirtotilaus voi määrittää, että nimikkeet lähetetään tiettyyn myymälään. Tässä tapauksessa siirtotilaus näkyy myymälässä vastaanottopyyntönä Modern POS- tai Cloud POS -sovelluksessa. Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten. Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin. Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Retailissa siirtotilauksen **Ota vastaan nyt** -kentässä.

## <a name="stock-counts"></a>Varaston inventoinnit
Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa. Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi. Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa. Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla. Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille. Pääkonttorissa inventointi tarkistetaan ja kirjataan.

## <a name="inventory-lookup"></a>Varastohaku
Nykyistä tuotteen määrää useissa myymälöissä ja varastoissa voi tarkastella varaston haku-sivulla. Nykyisen käytettävissä olevan määrän lisäksi luvattavissa oleva määrä (ATP) nähdään yksittäisistä myymälöistä. Voit tehdä tämän valitsemalla ensin myymälän, jonka ATP:tä haluat tarkastella, ja sitten **Näytä myymälän käytettävissä oleva määrä**.





