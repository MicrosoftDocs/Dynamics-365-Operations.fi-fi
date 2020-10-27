---
title: Määritä päätiedot
description: Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44eb817bbc6053eeefaef18f9d3be1822bcb057c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981894"
---
# <a name="set-up-rate-masters"></a>Määritä päätiedot

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään. Logistiikkapäällikkö määrittää yleensä hinnan päätiedot rahdinkuljettajien kanssa tehtyjen sopimusten perusteella. Tässä skenaariossa määritetään lentoyhtiön hinnan päätiedot. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="set-up-rate-master"></a>Hinnan päätietojen määrittäminen
1. Valitse Kuljetustenhallinta > Asetukset > Luokitus > Hinnan päätiedot.
2. Valitse Uusi.
3. Syötä Hinnan päätiedot -kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Avaa haku valitsemalla Luokituksen metatietojen tunnus -kentässä avattavan valikon painike.
    * Luokituksen metatietojen tunnus määrittää hinnan päätiedoissa tarvittavat tiedot. Se määrittää näitä hinnan päätietoja käyttävän TMS-laskennan odottamat metatiedot.  
6. Tässä esimerkissä valitaan P2P-asetus.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse Tallenna.

## <a name="set-up-rate-base"></a>Hintaperusteen määrittäminen
1. Valitse Hintaperuste.
    * Hintaperuste määrittää rahdinkuljettajan hinnan. Sitä voidaan käyttää tariffirakenteen määrittämisessä, koska se muodostaa tauon päätietojen keskeytyskohdissa määritettyjen hintojen rakenteet.  
2. Valitse Uusi.
3. Syötä Hintaperuste-kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Avaa haku valitsemalla Tauon päätiedot -kentässä avattavan valikon painike.
    * Tauon päätietoja käytetään hinnoittelurakenteen ja sen keskeytyskohtien määrittämisessä. Hinnoittelurakenteessa käytetään fyysisiin dimensioihin perustuvia hinnoittelutasoja.  
6. Tässä esimerkissä käytetään painoa
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Ota käyttöön Tiedot-osan laajennus.
9. Valitse Uusi.
10. Syötä Jättöpaikan postinumero kohteesta -kenttään 30301.
11. Syötä Jättöpaikan postinumero kohteelle -kenttään 30318.
12. Syötä Jättömaa/-alue-kenttään Suomi.
13. Kirjoita Alle 1,00 kg -kenttään 100.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1 kilo.  
14. Kirjoita < 5,00 kg -kenttään 300.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 5 kiloa.  
15. Kirjoita < 20,00 kg -kenttään 500.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 20 kiloa.  
16. Kirjoita < 100,00 kg -kenttään 1000.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 100 kiloa.  
17. Kirjoita < 1.000,00 kg -kenttään 3000.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1 000 kiloa.  
18. Valitse Tallenna.
19. Sulje sivu.

## <a name="assign-rate-base"></a>Hintaperusteen liittäminen
1. Ota käyttöön Hintaan perustuvat määritykset -osan laajennus.
2. Valitse Uusi.
    * Kaikissa hinnan päätiedoissa voi olla useita hintaan perustuvia määrityksiä. Näin jokaiselle rahdinkuljettajalle voidaan luoda useita eri hintapisteitä kohteista, palveluista ja eri hintaperusteista riippuen. Tässä menettelyssä luodaan vain yksi hintaan perustuvan määritys.  
3. Kirjoita arvo Nimi-kenttään.
4. Avaa haku valitsemalla Hintaperuste-kentässä avattavan valikon painike.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Avaa haku valitsemalla Palvelu-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Kirjoita Noudon postinumero -kenttään 98052.
    * Määritä postinumero, josta alkaen tämä hintaan perustuva määritys on voimassa.    
10. Syötä Noutomaa/-alue-kenttään Suomi.
11. Valitse Tallenna.

