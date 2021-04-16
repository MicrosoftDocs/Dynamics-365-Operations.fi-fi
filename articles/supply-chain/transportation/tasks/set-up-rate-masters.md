---
title: Määritä päätiedot
description: Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808987"
---
# <a name="set-up-rate-masters"></a>Määritä päätiedot

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten hinnan päätiedot määritetään. Logistiikkapäällikkö määrittää yleensä hinnan päätiedot rahdinkuljettajien kanssa tehtyjen sopimusten perusteella. Tässä skenaariossa määritetään lentoyhtiön hinnan päätiedot. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

## <a name="set-up-break-master"></a>Tauon päätietojen määrittäminen

1. Valitse **Kuljetustenhallinta > Määritys > Luokitus > Tauon päätiedot**. Tauon päätietoja käytetään hinnoittelurakenteen ja sen keskeytyskohtien määrittämisessä. Hinnoittelurakenteessa käytetään fyysisiin dimensioihin perustuvia hinnoittelutasoja.  
1. Valitse **Uusi**.
1. Anna arvo **Tauon päätiedot** -kentässä.
1. Anna **Nimi**-kenttään arvo.
1. Valitse **Tietotyyppi**-kentässä tietotyyppi.
1. Anna **Vertailu**-kentässä pyydetty vertailulaji (operaattorien avulla).
1. Anna **Hajota yksikkö** -kentässä jakoyksikkö.
1. Luo **Tiedot**-osassa hinnoittelurakenteeseen tarvittava määrä jakoja.
1. Valitse **Tallenna**.

## <a name="set-up-rate-master"></a>Hinnan päätietojen määrittäminen

1. Valitse **Kuljetustenhallinta > Asetukset > Luokitus > Hinnan päätiedot**.
1. Valitse **Uusi**.
1. Anna arvo **Hinnan päätiedot** -kentässä.
1. Kirjoita arvo **Nimi**-kenttään.
1. Avaa haku valitsemalla **Luokituksen metatietojen tunnus** -kentässä avattavan valikon painike. Luokituksen metatietojen tunnus määrittää hinnan päätiedoissa tarvittavat tiedot. Se määrittää näitä hinnan päätietoja käyttävän kuljetuksen hallintamoduulin odottamat metatiedot.  
1. Tässä esimerkissä valitaan P2P-asetus. Tämä on jo määritetty esittelytiedoissa.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Valitse **Tallenna**.

## <a name="set-up-rate-base"></a>Hintaperusteen määrittäminen

1. Valitse **Hintaperuste**.
    * Hintaperuste määrittää rahdinkuljettajan hinnan. Sitä voidaan käyttää tariffirakenteen määrittämisessä, koska se muodostaa tauon päätietojen keskeytyskohdissa määritettyjen hintojen rakenteet.  
2. Valitse **Uusi**.
3. Anna arvo **Hintaperuste**-kentässä.
4. Kirjoita arvo **Nimi**-kenttään.
5. Avaa haku valitsemalla **Tauon päätiedot** -kentässä avattavan valikon painike.
    * Tauon päätietoja käytetään hinnoittelurakenteen ja sen keskeytyskohtien määrittämisessä. Hinnoittelurakenteessa käytetään fyysisiin dimensioihin perustuvia hinnoittelutasoja.  
6. Tässä esimerkissä käytetään painoa. Tämä on jo määritetty esittelytiedoissa.
7. Valitse luettelossa valitulla rivillä oleva linkki.
8. Laajenna **Tiedot**-osa.
9. Valitse **Uusi**.
10. Anna **Jättöpaikan postinumero kohteesta** -kentässä 30301.
11. Anna **Jättöpaikan postinumero kohteelle** -kentässä 30318.
12. Anna **Jättömaa/-alue**-kentässä Suomi.
13. Anna **Alle 1,00 kg** -kentässä 100.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1 kilo.  
14. Anna **Alle 5,00 kg** -kentässä 300.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 5 kiloa.  
15. Anna **Alle 20,00 kg** -kentässä 500.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 20 kiloa.  
16. Anna **Alle 100,00 kg** -kentässä 1000.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 100 kiloa.  
17. Anna **Alle 1000,00 kg** -kentässä 3000.
    * Lisää hinta per kilo, jos kuorman kokonaispaino on alle 1000 kiloa.  
18. Valitse **Tallenna**.
19. Sulje sivu.

## <a name="assign-rate-base"></a>Hintaperusteen liittäminen

1. Laajenna **Hintaan perustuvat määritykset** -osa.
2. Valitse **Uusi**.
    * Kaikissa hinnan päätiedoissa voi olla useita hintaan perustuvia määrityksiä. Näin jokaiselle rahdinkuljettajalle voidaan luoda useita eri hintapisteitä kohteista, palveluista ja eri hintaperusteista riippuen. Tässä menettelyssä luodaan vain yksi hintaan perustuvan määritys.  
3. Kirjoita arvo **Nimi**-kenttään.
4. Avaa haku valitsemalla **Hintaperuste**-kentässä avattavan valikon painike.
5. Valitse luettelossa valitulla rivillä oleva linkki.
6. Avaa haku valitsemalla **Palvelu**-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Valitse luettelossa valitulla rivillä oleva linkki.
9. Anna **Noudon postinumero** -kentässä 98052.
    * Määritä postinumero, josta alkaen tämä hintaan perustuva määritys on voimassa.
10. Anna **Noutomaa/-alue**-kentässä Suomi.
11. Valitse **Tallenna**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]