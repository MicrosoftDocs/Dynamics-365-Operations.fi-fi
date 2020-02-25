---
title: Ostotilausten tuotepakkausten luominen
description: Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e1fd19c6a27739ce9f57a4ab33f61e6baaeb2e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022385"
---
# <a name="create-product-packages-for-purchase-orders"></a>Ostotilausten tuotepakkausten luominen

[!include [task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa. Ostotilausta käytetään ennalta määritetyn tuotejoukon tilauksen luomisessa. Menettely käyttää esittelytietojen USRT-yritystä.


## <a name="create-a-product-package"></a>Luo tuotepaketti
1. Siirry kohtaan Retail ja Commerce > Varastonhallinta > Täydennys > Tuotepaketit.
2. Valitse Uusi.
3. Kirjoita arvo Paketin numero -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. ValitseLisää.
8. Kirjoita Nimiketunnus-kenttään 0160.
9. Avaa haku valitsemalla Koko-kentässä avattavan valikon painike.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Kirjoita numero Määrä-kenttään.
12. ValitseLisää.
13. Kirjoita Nimiketunnus-kenttään 0160.
14. Avaa haku valitsemalla Variantin numero -kentässä avattavan valikon painike.
15. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
16. Kirjoita numero Määrä-kenttään.
17. ValitseLisää.
18. Kirjoita Nimiketunnus-kenttään 0175.
19. Kirjoita numero Määrä-kenttään.
20. Valitse Tallenna.
21. Sulje sivu.

## <a name="add-package-to-purchase-order"></a>Lisää paketti ostotilaukseen
1. Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
4. Valitse luettelosta toimittaja, jolle aiemmin luotiin tuotepaketti, jos toimittaja valittiin luonnin yhteydessä.
5. Ota käyttöön Yleinen-osan laajennus.
6. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Valitse OK.
11. Ota käyttöön Rivitiedot-osan laajennus.
12. Valitse Tuotepaketit-välilehti.
13. Valitse Ostotilausrivi.
14. Valitse Luo rivit paketista.
15. Etsi ja valitse luettelosta edellisessä vaiheessa luotu tuotepaketti.
16. Syötä Määrä-kenttään numero.
17. Valitse Luo.
18. Valitse Tallenna.

